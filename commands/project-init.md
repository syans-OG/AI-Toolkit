---
description: Nyalakan proyek baru dari ide mentah hingga rencana + setup dasar terverifikasi
agent: plan
---

`project-init` menuntun pemula membuat proyek dari nol dengan alur yang mencegah:
- premature implementation (langsung coding tanpa paham)
- hidden assumptions
- over-engineering (YAGNI)
- melewatkan quality gate

## Urutan Wajib

### 1️⃣ Uji Ide
Lakukan sesi singkat `/grill-me` pada ide: $ARGUMENTS
- Tanya 4-5 pertanyaan tajam: untuk siapa, masalah apa, kenapa tidak yang lebih sederhana, risiko terbesar.
- Beri flag: ide **CLEAR** atau **PERLU PERUBAHAN**.

### 2️⃣ Klarifikasi Kebutuhan
Aktifkan pola skill `brainstorming` tetapi versi ringkas (jangan tanya 1-per-1 terlalu lama):
- Tanyakan sekali, dalam SATU pesan: tujuan, target user, constraint, success criteria, non-goals.
- Ajukan asumsi default untuk yang belum dijawab, tandai `[ASUMSI]`.
- **Jangan lanjut sampai user konfirmasi atau koreksi.**

### 3️⃣ Rencana (wajib disetujui dulu)
Buata rencana bertahap:
- Fase 1: dilevery MVP terkecil yang bernilai
- Fase 2+: fitur inti, edge cases, polish, optimasi
- Untuk tiap fase: file yang akan diubah, ketergantungan antar langkah, estimasi kompleksitas, risiko.
- Exchange Contract: **JANGAN menulis kode atau mengubah file sampai user mengetik "yes" / "lanjut" / setuju.**

### 4️⃣ Setup Dasar (hanya setelah persetujuan)
Setelah user setuju rencana:
- Buat struktur folder/wajib (config, source, dsb.) seminimal mungkin.
- Proyek web → baca `skill react-nextjs-development`, `vite-patterns`, `tailwind-patterns` bila relevan.
- Siapkan alat validasi dasar (`lint`, `typecheck`) sesuai stack.
- **Buat `AGENTS.md`** di root proyek berisi: overview proyek, stack yang dipakai, perintah (install/dev/build/lint/test), struktur folder, dan konvensi penting. Ini membuat session opencode berikutnya langsung paham proyek tanpa menebak.
- **Buat `README.md` profesional** dengan skill `create-readme` (tanya dulu ke user apakah diminta).

### 5️⃣ Cetak Checklist Quality Gate
Di akhir, cetak checklist yang harus dijalankan user (atau minta dijalankan):
```
1. /code-review       — kualitas + security kode
2. /a11y-audit        — aksesibilitas UI (web/native)
3. /seo-audit         — SEO (bila web publik)
4. /security-scan     — bila menyimpan data/login
5. /simplify-code     — bersihkan setelah fitur beres
6. /hunt-bugs         — buru silent failure sebelum rilis
```
Ingatkan: jalankan saat fitur selesai, bukan menunggu seluruh proyek rampung.

## Aturan Krusial
- Kalau user tidak tahu/ragu di langkah 1-2 → bantu dengan pertanyaan pemandu, jangan diam.
- Landasan: `lean-build`, `karpathy-guidelines` (surgical, YAGNI, sukses terukur).
- Prioritas output: file + alur yang **jelas dieksekusi** — bukan presentasi panjang.