# Annual Performance Review 2026 — Henry Yusuf Rizaldy

Deck editorial 12 slide untuk merangkum kontribusi Henry pada empat area produk: SelfOrder, NetApps Backend, NetApps Mobile, dan Blip Dashboard.

## Jalankan
Buka `index.html` langsung di browser (tanpa server, tanpa npm, tanpa fetch). Koneksi internet diperlukan untuk Tailwind CDN dan Google Fonts. Semua slide dimuat dalam satu file; navigasi dengan tombol panah atau tombol bawah tanpa reload. Tekan **F** untuk fullscreen (tetap aktif saat berpindah slide).

## Struktur

- `index.html` — deck lengkap: cover + slide 02–12 dalam satu file (navigasi tanpa reload)
- `assets/css/style.css` — seluruh gaya visual
- `assets/js/navigation.js` — navigasi hash (`#N`) tanpa reload, fullscreen, dan bilah progres
- `print.html` — semua slide digabung untuk cetak PDF (Ctrl+P → landscape, background graphics on)
- `EVIDENCE.md` — sumber bukti commit, rentang analisis, hash representatif, dan catatan lineage (internal; tidak ditampilkan di deck)

## Susunan slide

| Slide | Isi |
| --- | --- |
| 01 | Cover |
| 02 | Ringkasan empat area produk |
| 03–04 | SelfOrder — lingkup pekerjaan, lalu kendala/solusi/dampak |
| 05–06 | NetApps Backend — lingkup pekerjaan, lalu kendala/solusi/manfaat |
| 07–08 | NetApps Mobile — lingkup pekerjaan, lalu kendala/solusi/manfaat |
| 09–10 | Blip Dashboard — lingkup pekerjaan, lalu kendala/solusi/manfaat |
| 11 | Standar kualitas kerja |
| 12 | Kesimpulan & rencana 2027 |

## Bukti

Deck ditulis untuk audiens non-teknis: tidak menampilkan nama repo, jumlah commit, hash, atau jalur kode. Semua itu disimpan di `EVIDENCE.md` sebagai sumber internal. SelfOrder dibatasi ke periode Januari–September 2026 sesuai instruksi. `SelfOrder_backend` dan `blip-dashboard-backend` memiliki lineage yang saling tumpang tindih, sehingga angka commit keduanya tidak dijumlahkan sebagai kontribusi unik.
