## Cover

<h3 align="center">
    <b>Praktikum Keamanan Jaringan</b><br>
    Security Misconfiguration
</h3>
<br>
<p align="center">
  <img src="../image/Logo_PENS.png" alt="Size Limit CLI" width="300">
</p>
<br>
<p align="center">
    Dosen Pembimbing:<br>
    Ferry Astika Saputra, S.T., M.Sc.
</p>
<br>
<p align="center">
    Disusun Oleh:<br>
    Septiana Dyah Anissawati (3122640031)
</p>
<br>
<p align="center">
    <b>
        KELAS D4 LJ IT B <br>
        JURUSAN D4 LJ TEKNIK INFORMATIKA B<br>
        DEPARTEMEN TEKNIK INFORMATIKA DAN KOMPUTER <br> 
        POLITEKNIK ELEKTRONIKA NEGERI SURABAYA <br>
        2023
    </b>
</p>
<br>


## Laporan

## Security Misconfiguration

Security Misconfiguration adalah salah satu dari sepuluh risiko keamanan yang terdapat dalam OWASP Top 10. Security misconfiguration terjadi ketika sistem atau aplikasi diatur secara salah atau tidak aman, sehingga memberikan kesempatan bagi penyerang untuk menemukan celah dan menyerang sistem atau aplikasi tersebut.

Ketika pengembang tidak mengikuti dokumentasi sebuah library, framework atau komponen aplikasi lainnya, tidak menerapkan standart konfigurasi yang ada, akan membuat aplikasi memiliki beberapa celah yang akan dimanfaatkan attacker.

Ada beberapa hal yang menyebabkan sering terjadi akibat dari miskonfigurasi:

    1. HTTP Only
    2. Query Builder
    3. X-Frame-options
    4. Content-Security Policy
    5. CORS
    6. Acces Control
    7. dll….

Berikut adalah contoh Security Misconfiguration dalam aplikasi website OWASP Juice Shop:

### A. Error Handling
Memunculkan error, namun error yang ditampilkan tidak dikemas secara konsisten.

1. Buka Aplikasi Burp Suite

    ![Screenshot](../image/task-6/1.png)

2. Membuka browser dan masuk ke halaman utama web OWASP Juice Shop

    ![Screenshot](../image/task-6/2.png)

3. Buka kembali burp suite, cari request baru /rest/product/search

    ![Screenshot](../image/task-6/3.png)

4. Masukkan payload /rest/product/search ke repeater lalu ubah endpoint menjadi text random kemudian send

    ![Screenshot](../image/task-6/4.png)

     ![Screenshot](../image/task-6/5.png)

    Ada response error 500 atau internal server error dimana pesan error sangat panjang dan tidak rapi.

### B. Deprecated Interface
Menggunakan antarmuka B2B kuno yang tidak dinonaktifkan dengan benar

1. Pada halaman utama, klik menu sidebar dan pilih Complaint

    ![Screenshot](../image/task-6/6.png)

2. Mengisi form dan masukkan file dengan format .xml

    ![Screenshot](../image/task-6/7.png)

3. Hasil

    ![Screenshot](../image/task-6/8.png)

4. Melihat proxy pesan error pada burp suite

    ![Screenshot](../image/task-6/9.png)