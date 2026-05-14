# Domain Model

## Product

Product adalah barang atau jasa yang dijual oleh UMKM.

### Fields

- `id`
- `name`
- `description`
- `sku`
- `sellingPrice`
- `costPrice`
- `stock`
- `minimumStock`
- `active`
- `createdAt`
- `updatedAt`

### Rules

- `name` is required.
- `sku` is optional in the early phase.
- `sellingPrice` is required and must be greater than or equal to 0.
- `costPrice` is optional in the early phase.
- `stock` defaults to 0 and must be greater than or equal to 0.
- `minimumStock` defaults to 0 and must be greater than or equal to 0.
- `active` defaults to true.

## Inventory

Inventory adalah area sistem yang mengatur jumlah stok product.

### Rules

- Stock represents how many units are available to sell.
- Stock movement records why stock changed.
- Stock can decrease because of a sale.
- Stock can increase because of restocking later.
- Manual stock correction is out of scope for the first MVP.

## Sale

Sale adalah transaksi penjualan.

### Fields

- `id`
- `invoiceNumber`
- `paymentMethod`
- `status`
- `totalAmount`
- `createdAt`
- `updatedAt`

### Rules

- Sale contains one or more sale items.
- Sale total is calculated from all sale items.
- Sale reduces product stock.
- Sale cannot be created if product is inactive.
- Sale cannot be created if stock is insufficient.
- Cancel sale is not implemented in the first sales sprint.

## Sale Item

Sale Item adalah satu baris product di dalam transaksi penjualan.

### Fields

- `id`
- `productId`
- `productName`
- `quantity`
- `unitPrice`
- `subtotal`

### Rules

- Sale item must reference a product.
- `quantity` must be greater than 0.
- `unitPrice` uses product selling price at transaction time.
- `subtotal` is calculated from `quantity * unitPrice`.

## Payment Method

Payment Method adalah metode pembayaran transaksi.

### Initial Values

- `CASH`
- `QRIS`
- `TRANSFER`

## Sale Status

Sale Status adalah status transaksi penjualan.

### Initial Values

- `COMPLETED`
- `CANCELLED`

## User

User adalah akun yang memakai sistem.

### Roles

- `OWNER`
- `STAFF`

### OWNER

Pemilik usaha.

Can:

- manage product
- manage sales
- view report
- manage staff later

### STAFF

Pegawai operasional.

Can:

- create sale
- view product
- update stock later

### Authentication Rules

- Register starts with OWNER account.
- Login returns JWT access token later.
- Password must have at least 8 characters.
- Email must be unique.
- Password must be stored as hash.
- Password must never be returned in API response.

## Report

Report adalah ringkasan data bisnis seperti total penjualan, jumlah product, dan revenue sederhana.

### Initial Reports

- total sales amount
- product count
- sales count

