# Algorithma Checkout Tokopedia

## Algorithma Descriptive

1. Mulai
2. Pilih produk
3. Jika ingin Masukan produk ke keranjang jika ingin membeli banyak produk berbeda
4. jika tidak masuk ke laman form pembayaran 
5. atur alamat penerima
6. pilih metode pengiriman
7. pilih metode pembayaran
8. lakukan pembayaran
9. setelah pembayaran pesanan akan diproses
10. Selesai

## Flowchart Checkout Tokopedia
```mermaid
flowchart TD

start@{"shape": circle, "label": "Mulai"}
inputProduct@{"shape": lean-l, "label": "Input: produk"}
isAddToCart@{"shape": diamond, "label": addToCart === true}
isAddToCartTrue@{"shape": rectangle, "label": Cart += produk}
setPayment@{"shape": lean-l, "label": "Input: metodePembayaran, alamat, metodePengiriman"}
setOrder@{"shape": lean-l, "label": "Output: #quot;Pesanan Dibuat Menunggu Pembayaran#quot;"}
isPayment@{"shape": diamond, "label": isPaid === True}
isPaymentTrue@{"shape": lean-l, "label": "Output: #quot;Pesanan Diproses#quot;"}
stop@{"shape": dbl-circ, "label": "Selesai"}

start-->inputProduct-->isAddToCart--True-->isAddToCartTrue-->setPayment-->setOrder-->isPayment--True-->isPaymentTrue-->stop

isAddToCart--False-->setPayment
isPayment--False-->setOrder
```