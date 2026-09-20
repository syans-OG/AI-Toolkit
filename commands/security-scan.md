---
description: Audit keamanan proyek (deteksi secret, OWASP Top 10, dependency)
agent: security-reviewer
subtask: true
---

Jalankan audit keamanan dengan subagent `security-reviewer`.

## Tugas

1. Ikuti langkah-langkah skill `api-security-best-practices` dan checklist OWASP Top 10.
2. Cari hardcoded secrets (API key, password, token) di seluruh kode.
3. Audit area berisiko: autentikasi, endpoint API, query DB, upload, webhook, payment.
4. Periksa dependency rentan bila ada `package.json`.
5. Bedakan temuan nyata vs false positive (`.env.example`, test credentials publik).
6. Beri daftar perbaikan prioritas + kode aman sebagai gantinya.

## Target
$ARGUMENTS

**Ingat**: jangan pernah mengungkap data sensitif atau secret dalam laporan.