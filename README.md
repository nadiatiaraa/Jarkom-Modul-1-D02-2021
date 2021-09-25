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

<img width="796" src="https://github.com/nadiatiaraa/Jarkom-Modul-1-D02-2021/blob/main/Screenshot%20Hasil/3.2.png">

# Soal No. 4
Temukan paket mysql yang mengandung perintah query select!

Pada soal ini, hal yang dilakukan yaitu dengan menggunakan display filter ``mysql.query and frame matches "select"``, kemudian akan terdapat beberapa file mySQL yang ditemukan

<img width="796" src="https://github.com/nadiatiaraa/Jarkom-Modul-1-D02-2021/blob/main/Screenshot%20Hasil/4.1.png">
Lalu jika dibuka, akan diperoleh sebagi berikut:

<img width="700" alt="Screen Shot 2021-09-22 at 09 31 47" src="https://user-images.githubusercontent.com/72669398/134274222-3982f87f-7900-4ea7-8c1a-f194014bef4a.png">

# Soal No. 5
Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap! 

Berdasarkan soal no 4 sebelumnya, setelah menemukan file mySQL tersebut, maka diperoleh ``username : akakanomi`` dan ``password : pemisahl4autan`` seperti gambar di bawah ini:

<img width="702" alt="Screen Shot 2021-09-22 at 09 32 18" src="https://user-images.githubusercontent.com/72669398/134274274-b5246ea0-fc9e-4e5a-9b1a-c3c3dbfd8280.png">

Kemudian, dapat melakukan login ke ``portal.ichimarumaru.tech`` dengan menggunakan username dan password tersebut. Sehingga diperoleh :

<img width="797" alt="Screen Shot 2021-09-22 at 09 32 36" src="https://user-images.githubusercontent.com/72669398/134274302-ab27c0ef-3839-493e-bcce-b5f843fa297f.png">

# Soal No. 6
Cari username dan password ketika melakukan login ke FTP Server!<br>
Jawaban :<br>
Dengan menggunakan display filter  ``ftp.request.command == USER or ftp.request.command == PASS``

![image](https://user-images.githubusercontent.com/83162422/134706096-265e48d0-2b21-49b8-b3f3-050d400ae4d9.png)

# Soal No. 7
Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")<br>
Jawaban :<br>
Dengan menggunakan display filter  ``ftp-data and frame contains "Real.pdf"`` diperoleh :

![image](https://user-images.githubusercontent.com/83162422/134706145-7497f8bb-87b1-4037-81c8-f116ab04d2d5.png)

# Soal No. 8
Cari paket yang menunjukan pengambilan file dari FTP tersebut!<br>
Jawaban :<br>
Dengan menggunakan display filter  ``ftp contains “RETR”``

![image](https://user-images.githubusercontent.com/83162422/134706200-3974f8da-9e05-49c5-ab9d-313feb215b08.png)

# Soal No. 9
Dari paket-paket yang menuju FTP terdapat indikasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!<br>
Jawaban :<br>
Dengan menggunakan display filter  ``ftp-data.command contains "secret.zip"``, lalu klik kanan >> follow >> TCP Stream >> Show data as raw >> Save as.

![image](https://user-images.githubusercontent.com/83162422/134706279-d0c0b180-c44a-4d4c-8c00-0160907e7b30.png)

File berisi file lain yaitu Wanted.pdf yang terkunci.

![image](https://user-images.githubusercontent.com/83162422/134706343-ca30f472-07f7-4e81-ac53-9e2b4424f932.png)

# Soal No. 10
Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!<br>
Jawaban :<br>
Dengan menggunakan display filter  ``ftp-data.command contains "history.txt"``, lalu klik kanan >> follow >> TCP Stream.

![image](https://user-images.githubusercontent.com/83162422/134759878-118956ae-2c2e-420a-9c53-71a65cfa2fd9.png)

ditemukan bahwa key ada pada bukanapaapa.txt, lakukan hal yang sama pada bukanapaapa.txt, menggunakan display filter  ``ftp-data.command contains "bukanapaapa.txt"``, ditemukan password sebagai berikut :

![image](https://user-images.githubusercontent.com/83162422/134706455-f3ac1feb-9285-42da-82ea-200f62d8066b.png)

Setelah file dibuka dengan password, berikut merupakan isi file Wanted.pdf yang terdapat pada secret.zip.

![image](https://user-images.githubusercontent.com/83162422/134706512-30602c92-4181-47d2-a8b8-526bb115345a.png)

# Soal No. 11
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!<br>

Karena yang diminta menampilkan paket yang hanya berasal dari port 80, maka melakukan capture filter `src port 80`

![image](https://github.com/nadiatiaraa/Jarkom-Modul-1-D02-2021/blob/main/Screenshot%20Hasil/soal%2011.1.png)
![image](https://github.com/nadiatiaraa/Jarkom-Modul-1-D02-2021/blob/main/Screenshot%20Hasil/soal%2011.2.png)

# Revisi No. 11
Berdasarkan hasil sebelumnya dimana ```src port 80``` kosong, ketika dicoba mengakses web ```http://monta.if.its.ac.id/``` menghasilkan sebagai berikut :
<img width="1440" alt="Screen Shot 2021-09-25 at 17 32 37" src="https://user-images.githubusercontent.com/72669398/134768394-597bddb4-5e65-4b3d-832a-49ea2052eeb4.png">

# Soal No. 12
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!<br>

Karena yang diminta menampilkan paket yang hanya mengandung port 21, maka melakukan capture filter  `port 21`

![image](https://github.com/nadiatiaraa/Jarkom-Modul-1-D02-2021/blob/main/Screenshot%20Hasil/soal%2012.1.png)
![image](https://github.com/nadiatiaraa/Jarkom-Modul-1-D02-2021/blob/main/Screenshot%20Hasil/soal%2012.2.png)

# Revisi No. 12
Berdasarkan hasil yang ditampilkan di atas ``port 21`` saat dibuka kosong, maka untuk mengetes dilakukan tes menggunakan ftp://ftp.adobe.com pada browser. Kemudian terdapat perintah untuk masuk seperti berikut :

<img width="437" alt="Screen Shot 2021-09-25 at 16 45 12" src="https://user-images.githubusercontent.com/72669398/134767071-a2e12bb4-c2d8-4f87-be1b-662d6fcc8868.png">

Kemudian, terdapat folder ftp.adobe.com seperti dibawah ini :

<img width="1440" alt="Screen Shot 2021-09-25 at 16 41 34" src="https://user-images.githubusercontent.com/72669398/134767077-9e805cdd-7675-4782-8c86-d00c2877141c.png">

Lalu, menghasilkan sebagai berikut :

<img width="1440" alt="Screen Shot 2021-09-25 at 16 41 08" src="https://user-images.githubusercontent.com/72669398/134767078-5931a8cc-558f-4b46-8617-68bf64a5bb78.png">

# Soal No. 13
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!<br>

Karena yang diminta menampilkan paket yang hanya menuju port 443, maka melakukan capture filter  `dst port 443`

![image](https://github.com/nadiatiaraa/Jarkom-Modul-1-D02-2021/blob/main/Screenshot%20Hasil/soal%2013.1.png)
![image](https://github.com/nadiatiaraa/Jarkom-Modul-1-D02-2021/blob/main/Screenshot%20Hasil/soal%2013.2.png)

# Soal No. 14
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!<br>

Karena diminta untuk mengambil paket yang menuju ke kemenag.go.id maka capture filter yang digunakan untuk mendapatkan paket tersebut yaitu `dst host kemenag.go.id`

![image](https://github.com/nadiatiaraa/Jarkom-Modul-1-D02-2021/blob/main/Screenshot%20Hasil/soal%2014.1.png)
![image](https://github.com/nadiatiaraa/Jarkom-Modul-1-D02-2021/blob/main/Screenshot%20Hasil/soal%2014.2.png)
# Soal No. 15
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!<br>

Karena diminta untuk menggunakan ip kami, maka kami harus mencari terlebih dahulu ip kami, lalu didapat ipnya yaitu `192.168.1.6`, lalu untuk mengambil paket yang berasal dari ip kami dengan filter `src host 192.168.1.6`

![image](https://github.com/nadiatiaraa/Jarkom-Modul-1-D02-2021/blob/main/Screenshot%20Hasil/soal%2015.1.png)
![image](https://github.com/nadiatiaraa/Jarkom-Modul-1-D02-2021/blob/main/Screenshot%20Hasil/soal%2015.2.png)

# Kendala Pengerjaan

