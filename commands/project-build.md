---
description: Eksekusi rencana yang sudah disetujui menjadi kode nyata, fase demi fase, di agent build
agent: build
---

`/project-build` mengeksekusi rencana dari `/project-init` (atau `/brainstorm`) menjadi implementasi nyata di agent `build`.

## Persiapan (harus jelas sebelum mulai)

1. **Tentukan sumber rencana**: cari file rencana/plan di proyek (mis. `PLAN.md`, `design.md`) ATAU pakai `$ARGUMENTS` sebagai penjelasan fase yang dikerjakan.
2. **Kutip ulang singkat** di awal: fase mana yang dikerjakan sekarang, file apa saja yang akan tersentuh, dan batas lingkup (jangan melebihi fase ini).
3. **Jika proyek sudah berisi kode** → gunakan skill `codebase-onboarding` untuk memahami struktur sebelum mengubah apa pun.
4. Kalau rencana belum ada → berhenti dan sarankan user menjalankan `/project-init` atau `/brainstorm` dulu. **Jangan mengarang rencana baru yang besar.**

## Mode Eksekusi (agent build)

- Bekerja sebagai agent `build` dengan akses tulis penuh.
- **Exchange Contract**: patuhi rencana yang disetujui. Tidak menambah fitur/spek baru di luar rencana — laporkan saja jika ketemu kebutuhan baru.

## Urutan Per Fase

Untuk setiap fase dalam rencana:
1. **Baca kode yang terkait** sebelum mengubah (pahami pola yang ada).
2. **Implementasikan sesuai langkah rencana** — satu langkah lalu verifikasi, jangan sekaligus.
3. **Verifikasi teknis setelah tiap langkah**:
   - Jalankan typecheck (`npx tsc --noEmit` bila TS)
   - Jalankan lint/format sesuai stack
   - Jalankan test bila ada (`npm test` / `npx vitest`, dst.)
   - Pastikan tidak ada error baru — kalau ada, perbaiki sebelum lanjut.
4. **Ringkas progres** singkat: file yang diubah + status verifikasi.

Saat semua fase selesai → cetak checklist final:
```
1. /code-review       — review kualitas + security
2. /a11y-audit        — aksesibilitas UI
3. /seo-audit         — SEO (bila web publik)
4. /security-scan     — bila menyimpan data/login
5. /simplify-code     — bersihkan kode
6. /hunt-bugs         — cari silent failure
7. git-pushing        — commit + push bila siap
```

## Aturan Krusial
- **Satu fase dulu, konfirmasi user** sebelum lanjut ke fase berikutnya (kecuali user bilang "lanjut semua").
- Jangan refactor berlebihan di luar lingkup fase (Surgical). 
- Tulis kode sesuai standar skill `clean-code`: ringkas, langsung, tanpa over-engineering, tanpa komentar yang tidak perlu.
- Jangan menambah dependensi tanpa alasan — rujuk `lean-build` / `ponytail` (YAGNI).
- Semua perbaikan harus bisa diverifikasi (typecheck/lint/test).

## Fokus yang sedang dikerjakan
$ARGUMENTS