# Algorithma Checkout Tokopedia

## Algorithma Descriptive

1. Mulai
2. membuka laman produk yang diinginkan
3. tekan tombol beli sekarang
4. pastikan pengguna sudah login
5. jika ya munculkan popup untuk masukan variasi dan kuantitas produk yang diinginkan kemudian konfirmasi untuk masuk laman pembayaran 
6. jika tidak arahkan ke laman login
7. pilih alamat
8. pilih metode pengiriman
9. pilih metode pembayaran
11. konfirmasi pembelian dengan klik tombol bayar sekarang
10. lakukan pembayaran dengan metode yang dipilih
11. jika pembayaran berhasil maka pesanan diteruskan ke penjual untuk dikirim
12. jika pembayaran tidak berhasil maka kirim notifikasi pembelian gagal dan lakukan refund
13. Selesai

## Flowchart Checkout Tokopedia
```mermaid
flowchart TD

start@{"shape": circle, "label": "Mulai"}
home@{"shape": rectangle, "label": "Masuk Halaman Beranda Tokopedia"}
toProduct@{"shape": rectangle, "label": "Membuka laman produk yang diinginkan"}
ctaBuyNow@{"shape": lean-l, "label": "Input: #quot;Tekan Tombol Tombol Beli Sekarang#quot;"}
isLogin@{"shape": diamond, "label": "userLogin == True"}
outputFalseIsLogin@{"shape": rectangle, "label": "Arahkan untuk login atau daftar!"}
outputTrueIsLogin@{"shape": rectangle, "label": "Munculkan Popup untuk memilih variasi dan kuantitas"}
ctaConfirm@{"shape": lean-l, "label": "Input: #quot;Tekan Tombol Lanjutkan ke Pembayaran#quot;"}
toPayment@{"shape": rectangle, "label": "Menuju Laman Pembayaran"}
paymentPage@{"shape": lean-l, "label": "Input: #quot;Atur#quot; alamat, Metode Pengiriman, Metode Pembayaran"}
confirmPayment@{"shape": lean-l, "label": "Input: #quot;Tekan Tombol Bayar Sekarang#quot;"}
doPayment@{"shape": lean-l, "label": "Input: #quot;lakukan pembayaran dengan metode yang dipilih#quot;"}
isPaymentSuccess@{"shape": diamond, "label": "payment == #quot;success#quot;"}
outputPaymentSuccess@{"shape": lean-l, "label": "Output: #quot;Pembayaran berhasil pesanan diteruskan ke penjual untuk diproses#quot;"}
outputPaymentFailed@{"shape": lean-l, "label": "Output: #quot;Pembayaran gagal atau habis waktu apabila sudah melakukan pembayaran maka akan di refund#quot;"}
stop@{"shape": dbl-circ, "label": "Selesai"}


start-->home-->toProduct-->ctaBuyNow-->isLogin--True-->outputTrueIsLogin-->ctaConfirm-->toPayment-->paymentPage-->confirmPayment-->doPayment-->isPaymentSuccess--True-->outputPaymentSuccess-->stop

isLogin--False-->outputFalseIsLogin-->stop
isPaymentSuccess-->False-->outputPaymentFailed-->stop
```