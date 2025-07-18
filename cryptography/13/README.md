# 🧠 Challenge: easy-rot  
**Kategori:** cryptography  
**CTF:** picoCTF 2025  
**Flag:** picoCTF{not_too_bad_of_a_problem}

---

## 📜 Deskripsi Soal  
**Hint:** Cryptography can be easy, do you know what ROT13 is?  

**Pesan terenkripsi:**  
cvpbPGS{abg_gbb_onq_bs_n_ceboyrz}

---

## 🔍 Langkah Penyelesaian  
1. Soal mengarahkan kita ke **ROT13**, yaitu Caesar cipher khusus dengan rotasi 13 huruf.  
   - A → N, B → O, C → P, ..., N → A, O → B, ..., Z → M  
2. Terapkan ROT13 pada bagian `{abg_gbb_onq_bs_n_ceboyrz}`:
   - abg → not  
   - gbb → too  
   - onq → bad  
   - bs → of  
   - n → a  
   - ceboyrz → problem  
3. Hasil konversi:  
   `picoCTF{not_too_bad_of_a_problem}`

---

## 🧠 Pembelajaran  
- **ROT13** adalah varian Caesar cipher yang menggeser huruf sejauh 13 posisi, bersifat *self-inverse* (diekstrak 2x hasilnya balik ke awal).  
- Karena alfabet Inggris memiliki 26 huruf, maka ROT13 adalah metode simetris: ROT13(ROT13(x)) = x.  
- Cipher ini sering digunakan di forum atau tantangan CTF sebagai obfuscation ringan.  
- Tools online seperti [rot13.com](https://rot13.com/) atau skrip Python dapat membantu:  
  ```python
  import codecs
  print(codecs.decode("cvpbPGS{abg_gbb_onq_bs_n_ceboyrz}", "rot_13"))
