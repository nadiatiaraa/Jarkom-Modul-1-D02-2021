# Jarkom-Modul-1-D02-2021

# Praktikum 1 Jarkom

**Nama Anggota Kelompok D2 :** 
- Sabrina Lydia Simanjuntak (05111940000107)
- Zulfayanti Sofia Solichin (05111940000189)
- Nadia Tiara Febriana (05111940000217)

# Soal No. 1
Sebutkan webserver yang digunakan pada "ichimarumaru.tech"! 

Pada soal ini, Webserver dapat dilihat dengan menggunakan display filter ```http.host == ichimarimaru.tech```, lalu ``klik kanan -> follow -> HTTP Stream``, lalu akan muncul windows seperti di bawah. Dan terlihat bahwa webserver yang digunakan ialah ``nginx/1.18.0 (Ubuntu).``
 
<img width="794" alt="Screen Shot 2021-09-22 at 09 29 29" src="https://user-images.githubusercontent.com/72669398/134274048-480b1bde-5df4-4d33-b752-d423a54a2b9b.png">

# Soal No. 2
Temukan paket dari web-web yang menggunakan basic authentication method! 

Untuk menemukan paket web yang menggunakan basic authentication method yaitu dengan menggunakan display filter ``http.authbasic`` .

<img width="714" alt="Screen Shot 2021-09-22 at 09 29 45" src="https://user-images.githubusercontent.com/72669398/134274070-d3f50a78-6165-4fc3-a6f9-0dc22bdeabdc.png">

# Soal No. 3
Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng! 

Pada soal no 3 ini, hal yang dilakukan yaitu menggunakan display filter ``http.host == basic.ichimarumaru.tech && http.authbasic`` untuk melakukan filter wibsite dari ``basic.ichimarumaru.tech`` dan juga menggunakan filter tambahan berupa ``http.authbasic``.
Di bagian credentials dari packet pertama, diperoleh username dan password sebagai berikut (di credentials) :

<img width="799" alt="Screen Shot 2021-09-22 at 09 30 05" src="https://user-images.githubusercontent.com/72669398/134274099-1ade4244-4001-4b4c-b88f-3f88706f4a8c.png">

Kemudian, dapat Login ke ``basic.ichimarumaru.tech`` dengan menggunakan username dan password pada gambar di atas, dan diperoleh:

<img width="796" alt="Screen Shot 2021-09-22 at 09 31 00" src="https://user-images.githubusercontent.com/72669398/134274201-e26975cc-74a0-4bb4-8213-46a88ccd30e9.png">

# Soal No. 4
Temukan paket mysql yang mengandung perintah query select!

Pada soal ini, hal yang dilakukan yaitu dengan menggunakan display filter ``mySQL``, kemudian save as file mySQL yang ditemukan dan dibuka, sehingga diperoleh sebagi berikut:

<img width="700" alt="Screen Shot 2021-09-22 at 09 31 47" src="https://user-images.githubusercontent.com/72669398/134274222-3982f87f-7900-4ea7-8c1a-f194014bef4a.png">

# Soal No. 5
Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap! 

Berdasarkan soal no 4 sebelumnya, setelah menemukan file mySQL tersebut, maka diperoleh ``username : akakanomi`` dan ``password : pemisahl4autan`` seperti gambar di bawah ini:

<img width="702" alt="Screen Shot 2021-09-22 at 09 32 18" src="https://user-images.githubusercontent.com/72669398/134274274-b5246ea0-fc9e-4e5a-9b1a-c3c3dbfd8280.png">

Kemudian, dapat melakukan login ke ``portal.ichimarumaru.tech`` dengan menggunakan username dan password tersebut. Sehingga diperoleh :

<img width="797" alt="Screen Shot 2021-09-22 at 09 32 36" src="https://user-images.githubusercontent.com/72669398/134274302-ab27c0ef-3839-493e-bcce-b5f843fa297f.png">

# Soal No. 6

# Soal No. 7

# Soal No. 8

# Soal No. 9

# Soal No. 10

# Soal No. 11

# Soal No. 12

# Soal No. 13

# Soal No. 14

# Soal No. 15

# Kendala Pengerjaan

