# 🧠 Challenge: thenumbers  
**Kategori:** cryptography  
**CTF:** picoCTF 2025  
**Flag:** picoCTF{thenumbersmason}

---

## 📜 Deskripsi Soal  
**Hint:** The flag is in the format `PICOCTF{}`  

**Pesan terenkripsi:**  
16 9 3 15 3 20 6 { 20 8 5 14 21 13 2 5 18 19 13 1 19 15 14 }

---

## 🔍 Langkah Penyelesaian  
1. Soal memberikan deretan angka yang mengindikasikan penggunaan cipher huruf-ke-angka (A1Z26 cipher).  
   Contoh: A = 1, B = 2, ..., Z = 26  
2. Pisahkan bagian dalam kurung kurawal `{ ... }` karena itu isi dari flag.  
3. Konversi angka-angka berikut menjadi huruf:  
20 8 5 14 21 13 2 5 18 19 13 1 19 15 14
menjadi:
T H E N U M B E R S M A S O N
4. Gabungkan hasil menjadi:  
picoCTF{thenumbersmason}

---

## 🧠 Pembelajaran  
- A1Z26 cipher adalah metode substitusi dasar yang mengganti huruf dengan nomor posisinya dalam alfabet.  
- Cipher seperti ini sering digunakan sebagai langkah awal dalam tantangan CTF untuk mengenalkan pola enkripsi sederhana.  
- Tools online untuk konversi A1Z26 dapat mempercepat decoding, atau cukup menggunakan skrip Python sederhana.  
- Mengenali pola angka dan mengenal cipher-cipher klasik adalah keterampilan penting di kategori kriptografi dasar.

---

