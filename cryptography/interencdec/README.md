# 🧠 Challenge: hashcrack  
**Kategori:** cryptography  
**CTF:** picoCTF 2025  
**Flag** picoCTF{caesar_d3cr9pt3d_890d2379}

---

## 📜 Deskripsi Soal  
Can you get the real meaning from this file?  

Download the file here:  
[https://artifacts.picoctf.net/c_titan/111/enc_flag](https://artifacts.picoctf.net/c_titan/111/enc_flag)

---

## 🔍 Langkah Penyelesaian  
1. Download file `enc_flag` dari link yang diberikan.  
2. Lakukan decode Base64 pertama kali pada isi file.  
3. Hasil decode pertama masih mengandung karakter `b` (representasi bytes), hilangkan karakter tersebut agar menjadi string murni.  
4. Lakukan decode Base64 kedua kali pada string hasil pembersihan tadi.  
5. Setelah itu, hasilnya adalah teks yang dienkripsi menggunakan Caesar cipher.  
6. Lakukan brute force Caesar cipher dengan mencoba semua kemungkinan pergeseran huruf hingga menemukan teks yang terbaca.  
7. Dapatkan flag:
picoCTF{caesar_d3cr9pt3d_890d2379}
8. Selamat, kamu berhasil menyelesaikan challenge ini!

---

## 🧠 Pembelajaran  
- Base64 encoding dapat dilakukan bertingkat sehingga perlu decode berulang kali.  
- Representasi bytes pada Python kadang muncul dalam bentuk string dengan prefix `b'...'` yang perlu diproses agar menjadi string murni.  
- Caesar cipher adalah cipher klasik yang mudah dipecahkan dengan brute force mencoba semua kemungkinan pergeseran.  
- Menggabungkan beberapa teknik encoding/enkripsi dalam satu challenge meningkatkan kompleksitas dan memerlukan pemahaman berbagai metode.

---

