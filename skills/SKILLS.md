# Katalog Skill (82)

Referensi daftar skill yang terpasang di `~/.agents/skills/`. Dipakai untuk memilih skill yang relevan sebelum mengerjakan tugas non-trivial. Setiap sesi, cukup baca bagian yang relevan — jangan muat semuanya.

## Alur Kerja & Metodologi
- **brainstorming** — rancang ide/masukan sebelum kerja kreatif (fitur, komponen, arsitektur).
- **ponytail** — paksa solusi paling sederhana (YAGNI, library/vakum standar dulu).
- **lean-build** — hindari overbuilding; buat seperlunya dengan batas berhenti yang jelas.
- **karpathy-guidelines** — aturan kurangi kesalahan umum LLM saat menulis/mereview kode.
- **clean-code** — standar kode ringkas, langsung, tanpa komentar berlebih.
- **writing-plans** — susun rencana implementasi sebelum memulai tugas multi-langkah.
- **executing-plans** — jalankan rencana implementasi yang sudah ada.
- **tdd** — test dulu, baru implementasi (red-green-refactor).
- **migration** — transisi schema/data/API yang reversible dan bisa rollback.
- **safe-refactor** — restrukturisasi kode tanpa mengubah perilaku.
- **surgical-patch** — perbaiki bug di lapisan paling sempit tanpa mengganggu sekitarnya.
- **benchmark** — ukur baseline performa, deteksi regresi, bandingkan stack.
- **performance-optimizer** — temukan & perbaiki bottleneck (diukur sebelum/sesudah).
- **diagnosing-bugs** — loop diagnosis bug keras & regresi performa.
- **systematic-debugging** — tangani bug/gagal test secara sistematis sebelum fix.
- **investigate-first** — diagnosa kegagalan ambigu sebelum mengedit apa pun.
- **code-review** — review perubahan berdasar 2 sumbu: standar repo & sesuai spec.
- **verification-before-completion** — buktikan (jalankan verifikasi) sebelum klaim "sudah selesai".
- **verify-and-stop** — buktikan hasil sesuai syarat tanpa melebihi scope.
- **verification-loop** — sistem verifikasi menyeluruh sebelum mengklaim selesai.
- **handoff** — tulis ringkasan session yang ringkas & terbaca agent lain.
- **domain-modeling** — bangun model domain, CONTEXT.md, catatan ADR.
- **to-spec** — ubah pembahasan sesi menjadi spec di issue tracker.
- **to-tickets** — pecah rencana/spec menjadi tickets ber-urutan.
- **codebase-onboarding** — buat panduan arsitektur & CLAUDE.md untuk repo asing.
- **create-readme** — buat README.md proyek.

## Kualitas & Keamanan Kode
- **typescript-expert** — keahlian TypeScript/JS (type-level, build, migrasi, debugging).
- **api-security-best-practices** — desain API aman: auth, validasi, rate limit.
- **backend-architect** — desain backend skalabel (API, microservices).
- **backend-dev-guidelines** — aturan senior backend (routes, services, prisma).
- **backend-security-coder** — keamanan backend: validasi input, auth, review keamanan.
- **frontend-security-coder** — keamanan frontend: cegah XSS, sanitasi output.
- **security-scanning-security-dependencies** — scan dependensi, SBOM, supply-chain.

## Frontend & UI/UX
- **frontend-design** — UI yang rapi, tidak generic, dengan identitas visual.
- **design-taste-frontend** — interfacing dengan taste desain tinggi (warna, layout, motion).
- **impeccable** — desain/audit/poles UI: hierarki, aksesibilitas, tipografi, anti-pattern.
- **anti-ui-slop** — cegah UI generik; bangun kontrak desain + finish gate.
- **ui-ux-pro-max** — intelligence desain UI/UX (50 gaya, palet, font pairings).
- **apple-design** — gaya desain Apple: gesture, spring, material, hierarki.
- **accessibility** — WCAG 2.2 AA: keyboard, kontras, screen reader.
- **prototype** — bangun beberapa versi UI & pilih yang pas dari preview.
- **pick-ui-library** — pilih library UI yang tepat untuk tugas tertentu.
- **virtual-lists** — render daftar besar (windowing) tanpa jank.
- **animate** — buat animasi web yang terarah & berasa benar.
- **animate-expo** — animasi React Native/Expo (Reanimated, gesture, haptics).
- **logo-designer** — desain logo & iterasi pakai SVG.
- **logo-generator** — optimasi penempatan/tautan logo di website.
- **seo** — audit SEO teknis, on-page, schema, sitemap, Core Web Vitals.

## Framework Frontend
- **react-nextjs-development** — React & Next.js 14+ (App Router, Server Components, TS, Tailwind).
- **react-patterns** — pola React modern: hooks, komposisi, performa, TS.
- **react-performance** — 70+ aturan optimasi performa React/Next.js (Vercel).
- **react-state-management** — state management: Redux Toolkit, Zustand, Jotai, React Query.
- **react-ui-patterns** — pola UI React: loading, error, data fetching.
- **zustand-patterns** — referensi Zustand 5.x (slices, middleware, persistence).
- **nextjs-best-practices** — prinsip App Router, data fetching, routing.
- **tailwind-patterns** — Tailwind CSS v4 (CSS-first, container queries, design tokens).
- **vite-patterns** — konfigurasi Vite: plugins, HMR, env, proxy, build.
- **vercel-deployment** — deploy ke Vercel dengan Next.js.
- **vercel-react-best-practices** — guideline performa React dari Vercel Engineering.

## Desktop (Tauri)
- **tauri-v2** — pengembangan app desktop/mobile Tauri v2 (Rust backend, IPC, capabilities).
- **customizing-tauri-windows** — kustomisasi window Tauri: titlebar, menu, drag region.
- **tauri-app-window-state** — persist ukuran & posisi window (plugin window-state).

## Dokumen & Laporan
- **docx** — buat/baca/edit dokumen Word (.docx/.dotx) dengan format profesional.
- **pptx** — buat/baca/edit presentasi PowerPoint (.pptx).
- **pdf** — baca, gabung, tanda, isi form, OCR PDF, dll.

## Gaya Komunikasi & Prosa
- **i-have-adhd** — gaya jawaban ADHD-friendly: mulai dari tindakan, langkah bernomor (aktif sampai "stop adhd mode").
- **humanizer** — tulis ulang teks yang terdengar AI menjadi natural.
- **stop-slop** — hilangkan pola tulisan khas AI (triad, dashes berlebihan, dll).
- **token-budget-advisor** — pilih kedalaman jawaban sesuai budget token yang diminta.

## Operasional & Git
- **terminal-ops** — jalankan/verifikasi perintah di repo dengan bukti eksekusi.
- **terminal-screenshot** — render output CLI berwarna ke PNG untuk verifikasi visual.
- **screenshot** — ambil tangkapan layar desktop/window/region.
- **file-organizer** — rapikan file/folder: cari duplikat, saran struktur baru.
- **lint-and-validate** — quality control otomatis setelah setiap perubahan kode.
- **context-budget** — audit konsumsi context window (agents, skills, MCP).
- **git-pushing** — stage, commit konvensional, dan push ke remote.
- **pre-push-github** — cek keamanan sebelum push (build, secret, test).

## Router & Meta
- **setup** — router skill opencode: tentukan skill minimal untuk tugas lintas domain.
- **find-skills** — cari & pasang skill baru untuk kebutuhan tertentu.
- **writing-skills** — panduan membuat/mengedit/verifikasi skill.
- **writing-for-agents** — tulis dokumen untuk agent (AGENTS.md, CLAUDE.md, skill).
- **customize-opencode** — konfigurasi opencode sendiri (opencode.json, plugin, MCP).
- **prompt-optimizer** — optimalkan prompt menjadi siap-pakai.