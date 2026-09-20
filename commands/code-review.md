---
description: Review code for quality, security, and maintainability
agent: code-reviewer
subtask: true
---

Jalankan review kode dengan subagent `code-reviewer` sesuai skill `code-review`.

## Tugas

1. Setelah menganalisis perubahan, terapkan checklist di skill `code-review`.
2. Baca seluruh file yang berubah, bukan hanya diff.
3. Hanya laporkan temuan yang benar-benar nyata (>80% yakin), dengan file + nomor baris.
4. Beri laporan terstruktur (CRITICAL/HIGH/MEDIUM/LOW) + ringkasan verdict.

## Target
$ARGUMENTS

**IMPORTANT**: Jangan setujui kode yang memiliki isu keamanan.