# DOKUMENTASI PEMANFAATAN AI DAN CODING
## NumerasiQuest — Game Petualangan Numerasi Kelas VI SD

> File ini merupakan **lampiran wajib** sesuai ketentuan lomba:
> *"Karya inovasi pembelajaran wajib memanfaatkan teknologi AI, Coding, atau
> integrasi keduanya (melampirkan storyboard, deskripsi prompt, atau algoritma
> coding yang digunakan)."*
>
> NumerasiQuest mengintegrasikan **KEDUANYA**:
> - **AI** → generator soal numerasi di setiap pulau (deskripsi prompt di Bagian A)
> - **Coding** → game web interaktif HTML/JavaScript yang dimainkan siswa (algoritma di Bagian B)

---

## A. Deskripsi Prompt AI (Generator Soal per Pulau)

Soal-soal pada game NumerasiQuest digenerate dengan Kecerdasan Buatan
(ChatGPT/Google Gemini) menggunakan 6 prompt berikut, satu untuk setiap
tingkat pulau, dari pemahaman dasar hingga HOTS.

### Prompt 1 — Pulau Pemahaman (Pulau 1)
```
Buat 3 soal pilihan ganda numerasi tingkat "pemahaman" untuk siswa kelas 6 SD
tentang mengidentifikasi informasi penting dari soal bertabel/data. Setiap soal
memiliki 4 opsi jawaban (1 benar), disertai kunci jawaban dan satu kalimat
petunjuk (hint) untuk membantu siswa yang tersesat.
```

### Prompt 2 — Pulau Strategi (Pulau 2)
```
Buat 3 soal pilihan ganda numerasi kelas 6 SD dengan tema "strategi":
beri konteks cerita, siswa harus menentukan operasi hitung yang tepat
(tambah/kurang/kali/bagi) untuk menyelesaikannya. Sertakan 4 opsi jawaban
per soal, kunci jawaban, dan hint singkat.
```

### Prompt 3 — Pulau Hitung Cepat (Pulau 3)
```
Buat 3 soal hitung cepat penjumlahan, perkalian, dan pembagian bilangan
bulat untuk kelas 6 SD (level TKA). 4 opsi jawaban per soal dengan pengecoh
(wrong answers) yang plausible, kunci jawaban, dan hint berupa cara kerja.
```

### Prompt 4 — Pulau Soal Cerita (Pulau 4)
```
Buat 3 soal cerita numerasi kontekstual kehidupan sehari-hari untuk kelas 6 SD
(toko, pengumpulan uang, perjalanan jarak-kecepatan). Setiap soal 4 opsi
jawaban, kunci, dan hint.
```

### Prompt 5 — Pulau Tantangan HOTS (Pulau 5)
```
Buat 3 soal numerasi HOTS (berpikir tingkat tinggi) untuk kelas 6 SD:
diskon/persentase, perencanaan tabungan multi-langkah, dan masalah volume.
4 opsi jawaban per soal, kunci, dan hint bertahap.
```

### Prompt 6 — Pulau Juara (Pulau 6)
```
Buat 3 soal numerasi tingkat tertinggi untuk persiapan TKA kelas 6 SD:
bunga sederhana bank, waktu-tempat-kecepatan multi-langkah, dan
modal-keuntungan usaha. 4 opsi jawaban, kunci, dan hint bertahap.
```

**Alur pemanfaatan AI dalam pembelajaran:**
1. Guru menjalankan prompt di atas → menghasilkan bank soal + kunci + hint.
2. Hasil AI ditinjau & divalidasi guru (pikretisasi ke kondisi sekolah).
3. Soal dimasukkan ke dalam game NumerasiQuest (file `numerasiquest.html`).
4. Siswa memainkan game di kelas → AI secara tidak langsung menjadi
   "naskah" soal setiap petualangan siswa.

**Storyboard pemanfaatan AI (ringkas):**
```
[Prompt 1-6 ke AI]  →  [Bank soal + kunci + hint]  →  [Validasi Guru]
                                                          ↓
[Siswa main game di kelas]  ←  [Soal di-load ke game HTML]
```

---

## B. Algoritma Coding (Game Web NumerasiQuest)

Game berupa **satu file HTML standalone** (`numerasiquest.html`) —
bisa dibuka langsung di browser Chromebook/HP/PC tanpa install
aplikasi dan tanpa internet. Struktur algoritmanya:

| Komponen | Peran dalam game |
|---|---|
| **Data `PULAU[]`** | Struktur 6 pulau: nama, warna, misi, 3 soal, 4 opsi, kunci, hint |
| **`campurPulau()`** | Mengacak urutan opsi jawaban per pulau (algoritma Fisher-Yates) agar susunan soal berbeda setiap kali main |
| **`mulai()` → `loadPulau()` → `loadSoal()`** | Alur utama: input nama → mulai pulau 1 → tampilkan soal → cek jawaban |
| **`jawab(i, btn)`** | Jika benar → kunci pulau → tombol lanjut. Jika salah → kunci opsi, tampilkan hint |
| **`tick()` (timer)** | Hitung mundur 3 menit per pulau; habis → layar "waktu habis" + tombol coba lagi |
| **`drawMinimap()`** | Peta mini 6 pulau di atas layar; pulau selesai ditandai ✓, pulau aktif disorot |
| **`finish()`** | Di pulau 6 selesai → tampilkan sertifikat Pendekar Numerasi + total waktu + tombol cetak |

---

## C. Cara Memainkan (untuk lampiran)

1. Buka file `numerasiquest.html` dengan browser apa pun.
2. Siswa menuliskan nama → klik **Mulai Petualangan**.
3. Kerjakan 3 misi di tiap pulau (waktu 3 menit per pulau).
4. Muncul jawaban benar → lanjut pulau berikutnya.
5. Di Pulau Juara (6), siswa memperoleh **Sertifikat Pendekar Numerasi**
   yang bisa dicetak.

---

## D. Catatan Implementasi di Kelas (diisi guru)

- **Hari/tanggal pelaksanaan:** ........................
- **Nama kelas & jumlah siswa:** ........................
- **Alat:** Chromebook/HP + layar interaktif (papan digital)
- **Foto/Video dokumentasi:** tersimpan di Google Drive
  (tautan tercantum di laporan utama, akses: Publik – Editor)
