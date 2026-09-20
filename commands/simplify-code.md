---
description: Sederhanakan dan bersihkan kode yang rumit tanpa mengubah perilaku
agent: code-simplifier
subtask: true
---

Jalankan penyederhanaan kode dengan subagent `code-simplifier`.

## Tugas

1. Baca file yang baru berubah.
2. Terapkan prinsip skill `clean-code` & `ponytail`: jangan over-engineering, jangan menambah comment yang tidak perlu.
3. Sederhanakan struktur (deep nesting → early returns), perbaiki readability (nama deskriptif, hindari nested ternary).
4. Hapus dead code, `console.log`, kode ter-comment, logika duplikat.
5. **Krusial**: pertahankan perilaku persis. Verifikasi tidak ada perubahan behavior setelah perbaikan.

## Target
$ARGUMENTS