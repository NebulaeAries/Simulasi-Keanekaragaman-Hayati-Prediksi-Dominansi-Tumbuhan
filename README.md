# Dinamika Dominansi: LKM Keanekaragaman Hayati

Website statis (satu file `index.html`, tanpa backend) untuk LKM prediksi dominansi tumbuhan.
Alur per kasus:

1. **Pilih kasus** (Kasus 1, 2, 3)
2. **Pengamatan**: siswa menghitung jumlah tumbuhan, lalu klik *Periksa jawaban*. Kalau satu kolom waktu benar semua, ikon muncul di kotak putih; kalau ada yang salah, angkanya jadi merah dan ikon tidak muncul. Ada 5 nyawa; tiap pemeriksaan yang masih salah mengurangi 1 nyawa. **Kalau nyawa habis**, jawaban yang benar otomatis diisikan (kotak kuning) dan siswa bisa lanjut ke halaman berikutnya.
3. **Pencocokan**: geser baris kolom *Tumbuhan dan Karakteristik* serta *Respons* agar cocok dengan *Laju Penggandaan*. Sama seperti di atas: 5 nyawa, dan kalau habis kartu otomatis disusun sesuai jawaban yang benar lalu siswa bisa lanjut.
4. **Simulasi**: pemandangan animasi yang hidup. Tumbuhan muncul satu per satu dengan efek tumbuh, bergoyang pelan, dan makin besar kalau makin dominan. Latarnya sesuai tema tiap kasus dan ikut bergerak: kebun berpagar dengan tanah kapur beralur, waduk dengan tanggul, alang-alang tepi, riak dan gelembung (Hydrilla digambar terendam di bawah permukaan), serta lereng gunung berapi dengan kawah menyala, lava, asap, dan abu. Tumbuhan ditaruh di tanah atau air, bukan di langit, dan yang di depan tampak lebih besar, penanda tumbuhan paling dominan (dengan efek kedip saat dominansi berpindah), bar persentase, grafik jumlah terhadap waktu, tombol kecepatan (0,5×, 1×, 2×), dan slider waktu. Kalau perangkat memakai mode *reduce motion*, animasi otomatis dimatikan dan siswa memutarnya manual.

## Cara upload ke GitHub dan jadi live (GitHub Pages)

1. Buka <https://github.com> → **New repository**. Beri nama (misal `dinamika-dominansi`), pilih **Public**, klik **Create repository**.
2. Di halaman repo, klik **Add file → Upload files**, tarik `index.html` (dan folder `images/` kalau pakai foto), lalu **Commit changes**.
   `index.html` harus ada di folder paling luar repo, jangan di dalam subfolder.
3. Buka **Settings → Pages**. Di bagian *Build and deployment*, pilih **Source: Deploy from a branch**, branch **main**, folder **/(root)**, klik **Save**.
4. Tunggu 1 sampai 2 menit. Alamat websitenya muncul di halaman yang sama:
   `https://USERNAME.github.io/NAMA-REPO/`

Setiap kali kamu upload ulang `index.html` ke repo, website otomatis ikut ter-update.

## Ganti gambar kartu kasus dengan foto

Kartu di halaman awal memakai ilustrasi bawaan. Untuk memakai foto sendiri, taruh file di folder `images/` dengan nama persis:

- `images/kasus1.jpg`
- `images/kasus2.jpg`
- `images/kasus3.jpg`

Kalau file-nya ada, otomatis dipakai dan memenuhi kotak kartu (bagian pinggir yang melebihi kotak dipotong). Kalau fotonya punya tepi transparan, tepi itu otomatis dibuang saat website dibuka lewat GitHub Pages. Kalau file-nya tidak ada, ilustrasi bawaan tetap tampil.

## Ubah isi soal

Semua isi LKM (latar, tumbuhan, laju penggandaan, angka kunci jawaban) ada di bagian `SCENARIOS` di dalam `index.html`. Cari komentar `DATA: ubah isi LKM di sini`.

- `initial`: jumlah awal tiap tumbuhan
- `key`: kunci jawaban `[[waktu ke-2], [waktu ke-3]]`
- `plants`: urutan tumbuhan, warna, bentuk ikon, karakteristik, respons

## Catatan

- Kunci jawaban ada di dalam kode `index.html`, jadi siswa yang membuka *View source* bisa melihatnya.
- Tambahkan `?guru` di akhir alamat (misal `.../index.html?guru`) untuk membuka semua halaman tanpa harus menyelesaikan soal, berguna untuk pratinjau guru.

};
```

Anggota boleh ditambah atau dikurangi, tinggal tambah atau hapus barisnya. Isi `id` dengan NIM (atau kosongkan kalau tidak mau ditampilkan).
