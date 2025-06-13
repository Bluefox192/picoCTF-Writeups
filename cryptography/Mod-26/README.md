# 🧠 Challenge: rot13  
**Kategori:** cryptography  
**CTF:** picoCTF 2025  
**Flag:** picoCTF{next_time_I'll_try_2_rounds_of_rot13_aFxtzQWR}

---

## 📜 Deskripsi Soal  
Cryptography can be easy, do you know what ROT13 is?  
cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_nSkgmDJE}

---

## 🔍 Langkah Penyelesaian  
1. Diberikan sebuah string flag dalam format yang terlihat seperti ROT13.  
2. ROT13 adalah bentuk substitusi huruf sederhana, yang menggantikan setiap huruf dengan huruf ke-13 setelahnya dalam alfabet.  
3. Gunakan tools ROT13 decoder online seperti:  
   - [https://rot13.com](https://rot13.com)  
   - atau gunakan skrip Python berikut:  
     ```python
     import codecs
     ciphertext = "cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_nSkgmDJE}"
     plaintext = codecs.decode(ciphertext, 'rot_13')
     print(plaintext)
     ```  
4. Hasil decoding ROT13:  
picoCTF{next_time_I'll_try_2_rounds_of_rot13_aFxtzQWR}
5. Flag ditemukan dan challenge selesai!

---

## 🧠 Pembelajaran  
- ROT13 adalah cipher klasik yang sangat sederhana dan digunakan untuk menyembunyikan teks dalam cara yang bisa dibalik langsung.  
- Meskipun tidak aman untuk penggunaan serius, ROT13 sering dipakai dalam tantangan CTF pemula.  
- Kita bisa menyelesaikan challenge ini hanya dengan tool online atau satu baris kode Python.  
- Mengetahui cipher dasar seperti ROT13, Caesar cipher, dan Base64 adalah fondasi penting dalam menyelesaikan challenge kriptografi CTF.

---

