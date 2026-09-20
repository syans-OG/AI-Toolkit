# KITAB — Koleksi Skills, Agents & Commands

Kumpulan **skills, agents, dan commands** untuk AI coding assistant (opencode / Claude Code) yang bisa langsung dipasang di mesinmu. Dikurasi dari setup pribadi dan siap dibagikan.

## Struktur Repo

```
KITAB/
├── skills/          # 77 skill (folder berisi SKILL.md + pendukungnya)
├── agents/          # 6 subagent (format .md)
├── commands/        # 10 command slash (format .md)
└── README.md
```

## Cara Install

### Skills
```bash
# Windows
copy /Y skills\* %USERPROFILE%\.agents\skills\

# macOS / Linux
cp -r skills/* ~/.agents/skills/
```

### Agents & Commands
```bash
# Salin ke folder config opencode
copy /Y agents\* %USERPROFILE%\.config\opencode\agents\
copy /Y commands\* %USERPROFILE%\.config\opencode\commands\
```

Setelah dipasang, skills bisa dipanggil otomatis oleh agent, commands bisa dijalankan dengan `/nama-command`, dan agents tersedia sebagai subagent.

---

## Daftar Skills per Kategori

### 🎨 Frontend & UI/UX Design
| Skill | Fungsi |
|---|---|
| `anti-ui-slop` | Mencegah UI generik; grounding desain pada jutaan screenshot web/iOS nyata |
| `apple-design` | Prinsip desain ala Apple: motion fisik, spring, material translucency, typography |
| `design-taste-frontend` | Landing page/branding yang tidak terlihat templated |
| `frontend-design` | Membangun UI produksi dengan estetika dan identitas visual yang disengaja |
| `impeccable` | Semua kebutuhan frontend: audit UX, visual hierarchy, theming, aksesibilitas |
| `ui-ux-pro-max` | 50 style, 21 palet, 50 pasangan font, 9 stack teknologi |
| `prototype` | Membuat beberapa versi UI sekaligus untuk dipilih secara live |
| `pick-ui-library` | Rekomendasi library frontend yang tepat per kebutuhan (charts, form, dll) |
| `accessibility` | Membangun & audit UI sesuai WCAG 2.2 Level AA |
| `animate` | Animasi web dari nol: tujuan, kurva, durasi, dan transisi yang tepat |
| `animate-expo` | Animasi React Native/Expo: Reanimated, Gesture Handler |

### ⚛️ React, Next.js & TypeScript
| Skill | Fungsi |
|---|---|
| `react-nextjs-development` | React & Next.js 14+ App Router, Server Components, TypeScript, Tailwind |
| `nextjs-best-practices` | Prinsip App Router: Server Components, data fetching, routing |
| `react-patterns` | Pola React modern: hooks, composition, performance, TypeScript |
| `react-performance` | 70+ aturan optimasi React/Next.js dari Vercel Engineering |
| `react-state-management` | Redux Toolkit, Zustand, Jotai, React Query |
| `react-ui-patterns` | Pola loading state, error handling, dan data fetching |
| `vercel-react-best-practices` | Panduan performance React/Next.js dari Vercel |
| `zustand-patterns` | Zustand 5.x: slices, middleware, persist, selectors |
| `tailwind-patterns` | Tailwind CSS v4: CSS-first config, container queries, design tokens |
| `vite-patterns` | Vite: config, plugins, HMR, env, proxy, SSR, library mode |
| `virtual-lists` | Windowing untuk render list/table ribuan baris tanpa jank |
| `typescript-expert` | Type-level programming, build performance, migrasi TS |
| `vercel-deployment` | Deploy Next.js ke Vercel |

### 🛡️ Backend & Keamanan
| Skill | Fungsi |
|---|---|
| `api-security-best-practices` | Design API aman: auth, input validation, rate limiting |
| `backend-architect` | Arsitektur backend scalable: API design, microservices, distribusi |
| `backend-dev-guidelines` | Backend produksi: routes, controllers, services, repositories, Prisma |
| `backend-security-coder` | Keamanan backend: input validation, auth, API security |
| `frontend-security-coder` | Keamanan frontend: XSS prevention, sanitasi output |
| `security-scanning-security-dependencies` | Scan dependency vuln, SBOM, supply chain security |

### 🧱 Prinsip Pengembangan & Arsitektur
| Skill | Fungsi |
|---|---|
| `brainstorming` | Mengubah ide mentah jadi desain tervalidasi |
| `clean-code` | Standar coding pragmatis: ringkas, langsung, tanpa over-engineering |
| `lean-build` | Membangun fitur dengan scope ketat dan stop condition jelas |
| `ponytail` | Solusi paling malas yang benar-benar bekerja (YAGNI) |
| `karpathy-guidelines` | Aturan perilaku untuk hindari kesalahan umum LLM coding |
| `tdd` | Test-driven development: red-green-refactor |
| `migration` | Migrasi schema/data/API yang reversible dan aman |
| `domain-modeling` | Mempertajam domain model proyek & mendokumentasikan ADR |
| `code-review` | Review kode dari dua sisi: standards dan spec |
| `safe-refactor` | Restrukturisasi kode tanpa mengubah perilaku |
| `surgical-patch` | Memperbaiki bug di lapisan paling sempit yang bertanggung jawab |

### 🐛 Debugging & Investigasi
| Skill | Fungsi |
|---|---|
| `systematic-debugging` | Alur debugging sistematis sebelum mengusulkan fix |
| `diagnosing-bugs` | Loop diagnosis untuk bug sulit & regresi performa |
| `investigate-first` | Diagnosis kegagalan ambigu sebelum mengedit kode |

### ✅ Verifikasi & Kualitas
| Skill | Fungsi |
|---|---|
| `benchmark` | Baseline performa, deteksi regresi, perbandingan stack |
| `performance-optimizer` | Identifikasi & perbaiki bottleneck, diukur sebelum/sesudah |
| `lint-and-validate` | QC otomatis: lint, format, types, static analysis |
| `verification-loop` | Verifikasi menyeluruh pekerjaan sebelum diklaim selesai |
| `verify-and-stop` | Buktikan pekerjaan memenuhi kriteria tanpa menambah scope |
| `terminal-ops` | Workflow eksekusi repo berbasis bukti yang terverifikasi |
| `terminal-screenshot` | Render output CLI berwarna ke PNG untuk verifikasi visual |

### 📄 Dokumen & Media
| Skill | Fungsi |
|---|---|
| `create-readme` | Membuat README.md untuk proyek |
| `docx` | Membuat/read/edit file Word (.docx, .dotx) |
| `pdf` | Baca, gabung, split, isi form, OCR file PDF |
| `pptx` | Buat/edit presentasi PowerPoint |
| `logo-designer` | Desain & iterasi logo berbasis SVG |
| `logo-generator` | Optimasi penempatan logo, branding header, favicon |
| `humanizer` | Menulis ulang teks agar tidak terdengar seperti AI |
| `stop-slop` | Menghilangkan pola tulisan AI dari prosa |
| `writing-for-agents` | Menulis dokumen untuk agent (SKILL.md, AGENTS.md) |
| `screenshot` | Screenshot desktop/window/region untuk verifikasi visual |

### 🌿 Git & Workflow
| Skill | Fungsi |
|---|---|
| `git-pushing` | Stage, commit conventional, dan push ke remote |
| `pre-push-github` | Cek keamanan sebelum push: build, secret, test |
| `to-spec` | Mengubah percakapan menjadi spec & publish ke issue tracker |
| `to-tickets` | Memecah plan menjadi tracer-bullet tickets |
| `handoff` | Menulis session handoff yang ringkas dan berbasis bukti |
| `file-organizer` | Merapikan file/folder, deteksi duplikat, struktur baru |

### 🖥️ Tauri / Desktop
| Skill | Fungsi |
|---|---|
| `tauri-v2` | Tauri v2+: Rust commands, IPC, capabilities, deploy |
| `customizing-tauri-windows` | Kustomisasi window Tauri: titlebar, drag regions, menu |
| `tauri-app-window-state` | Plugin window-state Tauri v2 untuk persist ukuran & posisi |

### 🔍 SEO
| Skill | Fungsi |
|---|---|
| `seo` | Audit & implementasi SEO: technical, on-page, schema, Core Web Vitals |

### 🧠 Meta — Kelola AI Tooling
| Skill | Fungsi |
|---|---|
| `setup` | Router untuk memilih skill yang tepat lintas domain |
| `find-skills` | Menemukan & menginstal skill yang tersedia |
| `codebase-onboarding` | Analisis codebase asing & buat panduan onboarding |
| `prompt-optimizer` | Menganalisis & mengoptimalkan prompt |
| `context-budget` | Audit pemakaian context window (bloat agents/skills/rules) |
| `token-budget-advisor` | Mengontrol panjang jawaban sesuai budget token |

---

## Daftar Agents

| Agent | Mode | Fungsi |
|---|---|---|
| `a11y-architect` | subagent | Audit & desain aksesibilitas WCAG 2.2 (Web & Native) |
| `code-reviewer` | subagent | Review kode: quality, security, maintainability |
| `code-simplifier` | subagent | Sederhanakan kode tanpa mengubah perilaku |
| `security-reviewer` | subagent | Deteksi secret, SSRF, injection, OWASP Top 10 |
| `seo-specialist` | subagent | Technical SEO, schema, on-page, Core Web Vitals |
| `silent-failure-hunter` | subagent | Cari error tertelan, failure senyap, fallback buruk |

## Daftar Commands

| Command | Agent | Fungsi |
|---|---|---|
| `/a11y-audit` | a11y-architect | Audit aksesibilitas UI sesuai WCAG 2.2 |
| `/brainstorm` | plan | Sesi brainstorming terstruktur untuk validasi ide |
| `/code-review` | code-reviewer | Review kode untuk quality, security, maintainability |
| `/grill-me` | plan | Uji ke-keras ide dengan pertanyaan tajam |
| `/hunt-bugs` | silent-failure-hunter | Cari bug tersembunyi & kegagalan senyap |
| `/project-build` | build | Eksekusi rencana disetujui menjadi kode nyata per fase |
| `/project-init` | plan | Nyalakan proyek baru: ide → rencana + setup terverifikasi |
| `/security-scan` | security-reviewer | Audit keamanan: secret, OWASP, dependency |
| `/seo-audit` | seo-specialist | Audit & perbaikan SEO |
| `/simplify-code` | code-simplifier | Bersihkan & sederhanakan kode |

---

## Lisensi

Silakan gunakan, salin, dan modifikasi. Kredit dihargai tapi tidak wajib.