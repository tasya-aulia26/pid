# Cara Memakai NumerasiQuest — Versi PID (Papan Interaktif Digital)

## Struktur folder
```
PID/
├── numerasiquest.html   ← file game (ini yang di-open)
└── img/
    ├── judul.jpg          (layar awal)
    ├── peta.jpg           (peta 6 pulau — tombol muncul di atas layer ini)
    ├── level1.jpg         (Pulau Pemahaman — 3 soal, 5 menit)
    ├── level2.jpg         (Pulau Strategi — 2 soal, 4 menit)
    ├── level3.jpg         (Pulau Hitung Cepat — 2 soal, 3 menit)
    ├── level5.jpg         (Pulau Soal Cerita — 4 soal, 4 menit)
    ├── evaluasi.jpg       (Tantangan HOTS — 5 soal, 10 menit)
    └── kesimpulan.jpg     (layar sertifikat juara)
```
> Penting: simpan folder `img` **menempel** dengan `numerasiquest.html` (jangan dipisah),
> karena game membaca gambar dengan nama relatif `img/...`

## Cara menjalankan di PID
1. Salin seluruh folder `PID` ke komputer/flashdisk yang tersambung PID.
2. Buka **browser Chrome/Edge** di PID → buka `numerasiquest.html`.
3. Tekan **F11** (fullscreen) — game otomatis menyesuaikan layar 16:9 apa pun resolusinya.
4. Siswa menuliskan nama → **Mulai Petualangan**.

## Alur main (sesuai layer Anda)
1. **Layar judul** (layer "Petualangan Numerasi Kelas VI") → input nama + tombol MULAI
2. **Layar peta** (layer "Peta Petualangan fredrikstad") → 6 tombol pulau ikut
   posisi aslinya di layer; pulau berikutnya terbuka setelah pulau sebelumnya selesai
3. **Klik pulau** → layar level dengan layer aslinya sebagai latar, panel misi di kanan:
   soal → 4 opsi A–D (tombol besar, mudah dijangkau PID) → benar/konfeti → lanjut
4. **Pulau Juara** (🏆) terbuka setelah semua selesai → **Sertifikat Pendekar Numerasi**
   + tombol **Cetak Sertifikat** (laser/PID)

## Tombol & aturan skor
| Tombol | Fungsi |
|---|---|
| 🗺️ Peta | kembali ke peta (waktu pulau berhenti, bisa lanjut lagi) |
| ↻ Reset (Tutor) | mengulang permainan dari awal (untuk guru berganti kelompok) |
| Skor | soal langsung benar = 30 poin, benar setelah salah dulu = 15 poin. Maksimal 480 |
| Timer | sesuai info misi di layer: L1 5 mnt, L2 4 mnt, L3 3 mnt, L4 4 mnt, Evaluasi 10 mnt. Habis → lanjut tetap, tanpa sanksi |

## Catatan soal di layer
- Opsi soal Evaluasi no. 5 di layer aslinya tertulis "C. Seni" (duplikat B) — di game
  sudah diperbaiki menjadi **C. Olahraga** (jawaban benar sesuai kunci).
- Soal & kunci jawaban mengikuti persis layer Anda; petunjuk (hint) adalah
  "Langkah Penyelesaian" yang ada di layer.

## Dokumen pendukung lomba (di folder atas)
- `PROMPT-AI-dan-CODING.md` — lampiran wajib: 6 prompt AI + algoritma coding
- `AKTIVITAS-DEEP-LEARNING.md` — aktivitas "Dari Pemain Menjadi Pencipta Pulau"
