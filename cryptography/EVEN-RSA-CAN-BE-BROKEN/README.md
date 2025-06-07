cat <<EOF > cryptography/EVEN-RSA-CAN-BE-BROKEN/README.md
# 🧠 Challenge: EVEN RSA CAN BE BROKEN

**Kategori:** cryptography  
**CTF:** picoCTF 2025  
**Flag:** \`picoCTF{tw0_1$_pr!m378257f39}\`

---

## 📜 Deskripsi Soal

> This service provides you an encrypted flag. Can you decrypt it with just N & e?  
Connect to the program with netcat:  
\`\`\`bash  
\$ nc verbal-sleep.picoctf.net 51624  
\`\`\`  
The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_vulnerable_rsa/source.py)

---

## 🔍 Langkah Penyelesaian

1. Jalankan perintah:
   \`\`\`bash
   nc verbal-sleep.picoctf.net 51624
   \`\`\`
   untuk mendapatkan `N`, `e`, dan `ciphertext`.

2. Setelah dianalisis, ternyata nilai `N` adalah hasil dari `2 × p`, artinya RSA ini sangat lemah karena salah satu faktornya adalah bilangan kecil (`2`).

3. Dengan menggunakan library `Crypto.Util.number`, kita dapat menghitung `phi`, `d`, lalu mendekripsi ciphertext dengan:
   \`\`\`python
   from Crypto.Util.number import inverse, long_to_bytes

   N = ...
   e = ...
   c = ...

   p = N // 2
   q = 2
   phi = (p - 1) * (q - 1)
   d = inverse(e, phi)
   m = pow(c, d, N)
   print(long_to_bytes(m).decode())
   \`\`\`

4. Flag berhasil didekripsi!

---

## 🧠 Pembelajaran

- RSA bisa dipecahkan jika bilangan `N` merupakan hasil dari bilangan prima yang terlalu kecil atau tidak acak.
- Faktor `2` sebagai salah satu komponen kunci membuat RSA rentan terhadap faktorisasi cepat (dengan `N // 2` saja).
- Gunakan bilangan prima besar dan aman untuk membuat kunci RSA.
- Dalam implementasi nyata, sangat penting untuk memastikan proses pembangkitan kunci tidak cacat atau terlalu sederhana.

EOF
