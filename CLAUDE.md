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

Belum ada kode. Perbarui bagian ini setelah kode dari PC masuk: stack yang dipakai,
cara install, cara menjalankan, dan cara menjalankan test.

## Status terakhir

<!-- Perbarui di akhir setiap sesi. Format: tanggal, perangkat, apa yang dikerjakan, langkah berikutnya. -->

- 2026-10-24 (HP): Repo dibuat dan CLAUDE.md ditambahkan. Berikutnya: push kode dari PC ke repo ini.
