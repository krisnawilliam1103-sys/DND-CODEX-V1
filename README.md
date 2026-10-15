# D&D Codex V1 — The Grimoire

Prototype katalog Dungeons & Dragons SRD 5.2.1 dengan antarmuka dark fantasy dan label navigasi bahasa Indonesia.

## Fitur yang sudah berfungsi
- Pencarian lokal pada nama, kategori, sumber, dan isi teks.
- 13 kategori konten; filter kategori, pengurutan A–Z/Z–A, dan muat lebih banyak.
- Panel detail untuk setiap entri.
- Simpan favorit pada browser (localStorage), serta salin nama entri.
- Responsif untuk layar HP dan desktop.
- Data katalog dipisahkan di `data/catalog.json`; berkas sumber Markdown ada di `sources/`.
- Tidak membutuhkan Node.js, database, akun, atau API key untuk prototype ini.

## Menjalankan di komputer
Pastikan Python 3 terpasang. Dari folder `dnd-codex-v1`, jalankan:

```bash
python -m http.server 8080
```

Lalu buka `http://localhost:8080`.

## Menjalankan di Android (Termux)
1. Ekstrak ZIP proyek.
2. Masuk ke folder proyek, misalnya `cd /sdcard/Download/dnd-codex-v1`.
3. Jika Python belum tersedia, jalankan `pkg install python`.
4. Jalankan `python -m http.server 8080`.
5. Buka `http://127.0.0.1:8080` di browser HP yang sama.

Untuk akses teman dari internet, unggah folder ini ke hosting static yang mendukung file HTML/CSS/JS. Untuk sementara ini prototipe baca-saja; favorit disimpan per browser, bukan dibagikan ke semua pengguna.

## Struktur folder
- `index.html` — halaman utama.
- `assets/style.css` — tampilan dan layout responsif.
- `assets/app.js` — pencarian, filter, detail, sort, favorit.
- `data/catalog.json` — indeks terstruktur 2.863 bagian yang diambil dari file SRD.
- `sources/*.md` — sumber Markdown asli yang ikut disertakan untuk audit dan pengembangan lanjutan.
- `SOURCES.md` — atribusi sumber dan lisensi.

## Status terjemahan
Ini merupakan prototype fungsional, bukan terjemahan penuh. Antarmuka dan nama kategori sudah berbahasa Indonesia, tetapi deskripsi aturan dan konten masih memakai teks sumber bahasa Inggris. Terjemahkan data secara bertahap dengan menjaga `id`, `source`, serta nama asli untuk mendukung pencarian dwibahasa.
