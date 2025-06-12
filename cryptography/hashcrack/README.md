# 🧠 Challenge: hashcrack

**Kategori:** cryptography  
**CTF:** picoCTF 2025
**Flag:** `picoCTF{UseStr0nG_h@shEs_&PaSswDs!_36a1cf73}`

---

## 📜 Deskripsi Soal

> A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server? Access the server using nc verbal-sleep.picoctf.net 61522

---

## 🔍 Langkah Penyelesaian


1. Hubungkan ke server dengan menggunakan netcat menggunakan perintah "nc verbal-sleep.picoctf.net 61522"
2. Identifikasi setiap hash yang diberikan dan decrypt sesuai dengan jenis hash
3. Dan selamat anda berhasil.


---

## 🧠 Pembelajaran

- MD5 dan SHA-1 tidak lagi aman digunakan untuk keperluan keamanan modern
- SHA-256 lebih kuat, namun tetap dapt dipecahkan bila digunakna tanpa salt dan dengan password lemah
- Gunakan hashing yang aman untuk password seperti bcrypt, scrypt, dan argon2
- Selalu kombinasikan dengan salt unik unutk tiap pengguna.
