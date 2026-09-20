---
description: Cari bug tersembunyi, error tertelan, dan kegagalan senyap
agent: silent-failure-hunter
subtask: true
---

Jalankan perburuan silent failure dengan subagent `silent-failure-hunter`.

## Tugas

1. Telusuri kode dengan pola-pola skill `diagnosing-bugs` & `investigate-first`.
2. Buru: empty catch, error dikonversi ke null tanpa konteks, logging kurang konteks, fallback berbahaya (`.catch(() => [])`), kehilangan stack trace, missing async handling, tidak ada timeout/rollback.
3. Untuk setiap temuan, beri: lokasi, severity, masalah, dampak, serta perbaikan yang diusulkan.
4. Verifikasi setiap dugaan dengan bukti (ikuti alur pemanggilan), bukan asumsi.

## Target
$ARGUMENTS