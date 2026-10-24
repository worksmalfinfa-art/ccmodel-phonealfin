# CLAUDE.md

Panduan untuk Claude saat bekerja di repo ini.

## Bahasa

- Jawab dan jelaskan dalam Bahasa Indonesia.
- Nama variabel, fungsi, dan pesan commit boleh dalam Bahasa Inggris.

## Kerja lintas perangkat (PC dan HP)

Repo ini dikerjakan dari dua tempat:

- **PC**: Claude Code lokal di komputer.
- **HP**: sesi cloud Claude Code (claude.ai/code atau aplikasi Claude). Container-nya
  sementara; apa pun yang belum di-push akan hilang saat sesi berakhir.

GitHub (`origin`) adalah satu-satunya sumber kebenaran. Aturannya:

1. **Sebelum mulai**: `git fetch origin` lalu `git pull` branch yang sedang dikerjakan,
   supaya perubahan dari perangkat lain ikut masuk.
2. **Sebelum berhenti**: commit dan push semua pekerjaan, walaupun belum selesai
   (pakai awalan `wip:` di pesan commit). Jangan tinggalkan perubahan yang belum di-push.
3. Baca dan perbarui bagian **Status terakhir** di bawah setiap kali selesai sesi,
   supaya sesi berikutnya (di perangkat mana pun) tahu harus lanjut dari mana.
4. Jangan pernah commit rahasia (API key, token, `.env`). Simpan di environment
   variable masing-masing perangkat.

## Tampilan di HP

- Artifact dan halaman HTML harus nyaman dibaca di layar HP: margin samping 16px,
  tanpa scroll horizontal, dan mendukung tema terang/gelap.
- Jawaban di chat ringkas; hindari tabel yang terlalu lebar.

## Struktur proyek

- `artifacts/radar-prospek.html`: tools pencari prospek (CCTV, komputer, hardware) dari
  media sosial. HTML + JS tunggal tanpa build. Dipublikasikan sebagai Artifact:
  https://claude.ai/artifact/GsxcJgVvH3UuGv6V1Y21gq. Data prospek dan profil usaha
  tersimpan di database Artifact (koleksi `leads`, dokumen `config/profil`), jadi sama di HP
  dan PC. Untuk mengubah halaman: edit file ini lalu publish ulang ke URL yang sama.
- Belum ada kode dari PC. Perbarui bagian ini setelah kode masuk: stack, cara install,
  cara menjalankan, dan cara menjalankan test.

## Status terakhir

<!-- Perbarui di akhir setiap sesi. Format: tanggal, perangkat, apa yang dikerjakan, langkah berikutnya. -->

- 2026-10-24 (HP): Repo dibuat dan CLAUDE.md ditambahkan. Artifact tes
  `artifacts/uji-layar-hp.html` dibuka di HP, semua pemeriksaan lulus.
  Berikutnya: push kode dari PC ke repo ini.
- 2026-10-24 (HP): Membuat tools Radar Prospek (`artifacts/radar-prospek.html`): generator
  pencarian per platform, penilai postingan (kata kunci + analisa Claude), daftar prospek
  dengan status dan follow-up, template pesan WA. Diisi 3 prospek contoh (id `contoh-*`).
  Berikutnya: isi profil usaha, hapus data contoh, coba pakai 1 minggu lalu sesuaikan
  kata kunci di `RULES`/`PRODUK` sesuai hasil nyata.
