# Evidence Henry Performance Review

Dokumen ini menjadi sumber bukti untuk deck `Annual Performance Review 2026`. Semua klaim diambil dari metadata commit Henry pada repo lokal yang diberi izin baca.

## Batas Analisis

- Mode akses: read-only.
- Repo sumber tidak dimodifikasi.
- Secret tidak dibaca atau ditampilkan.
- Filter author: `Henry\|henry\|Hype AMD` untuk mencakup variasi `Henryyr`, `henryyr`, `henry`, dan `Hype AMD`.
- Pola perintah read-only: `$env:GIT_MASTER='1'; git log --author='Henry\|henry\|Hype AMD' ...`.

## Ringkasan Repo

| Repo | Scope Henry | Rentang | Stack | Area dominan |
|---|---:|---|---|---|
| `Blip-Apps/SelfOrder_backend` | 404 commit total, 295 non-merge | filter `2026-01-01..2026-09-30`, commit efektif `2026-01-02..2026-09-14` | TypeScript, NestJS, Fastify, TypeORM, PostgreSQL, Redis, Socket.IO, S3, Docker | `apps/api/src/domains`, `libs/common/src`, `apps/api/src/socket`, `libs/database/src`, `apps/job/src/carts` |
| `Blip-Apps/blip-dashboard-backend` | 747 commit total, 596 non-merge | `2025-07-10..2026-08-28` | TypeScript, NestJS, Fastify, TypeORM, PostgreSQL, Redis, Socket.IO, S3, Jest, Docker | `apps/api/src/domains`, `apps/api/src/socket`, `libs/upload`, `libs/common`, `apps/job` |
| `Blip-Apps/netapps-backend` | 53 commit total, 32 non-merge | `2026-09-17..2026-10-12` | TypeScript, NestJS, Fastify, TypeORM, PostgreSQL, Redis, Socket.IO, payment/reporting integrations, Docker | `apps/api/src/domains`, report services, pre-sales, partner homepass |
| `Blip-Apps/netapps-mobile` | 316 commit total, 271 non-merge | `2026-02-24..2026-05-11` | Flutter, Dart, BLoC, Dio, get_it, localization, secure storage, socket.io client | `lib/core/widgets/component`, `lib/pages`, `lib/l10n`, auth/profile/tagihan/notifikasi |

Catatan: `SelfOrder_backend` dan `blip-dashboard-backend` punya lineage/riwayat yang saling tumpang tindih. Angka commit keduanya tidak boleh dijumlahkan sebagai total kontribusi unik.

## Bukti Per Repo

### SelfOrder Backend

- Rentang yang dipakai untuk SelfOrder sesuai koreksi user: 1 Januari sampai akhir September 2026. Karena September tidak memiliki tanggal 31, filter dijalankan sampai `2026-09-30 23:59:59`.
- Hasil filter: 404 commit Henry, 295 non-merge, tanggal efektif `2026-01-02..2026-09-14`.
- Top paths: `apps/api/src/domains` (1361), `libs/common/src` (93), `apps/api/src/socket` (74), `libs/database/src` (37), `apps/job/src/carts` (27), `libs/upload/src` (17), `libs/auth-token/src` (13).
- Bukti hash: `8360d330` realtime metrics aggregation + order concurrency hardening; `76c4ddcb` create user and property from Nonton login; `e2a216c8` media URL generation + remove Nginx proxy; `32235849` media properties update fix; `95c03be7` seeder cleanup + origin field; `b9549c43` slow ms/user + dashboard fix; `e6de0b07` optimization.

### Blip Dashboard Backend

- Bukti kontribusi: content article/career, role/permission, media upload, logging/error reporting, WebSocket role logging, Swagger DTO examples, doc node refactor.
- Bukti hash: `7f19080`, `4dc3743`, `1e5060a`, `bcbc472`, `3c2c189`, `4c37df5`, `3b38145`, `8629869`.
- Area teknis: `apps/api/src/domains`, `apps/api/src/socket`, `libs/upload/src/upload.service.ts`, `libs/common/src/logger`, `libs/common/src/interceptor`.

### NetApps Backend

- Bukti kontribusi: Partner Homepass, pre-sales/order mapper, customer segment/network reports, invoice/order reports, filter/status/activation date fixes, unit tests report services.
- Bukti hash: `3ab1177`, `e8d9630`, `003e115`, `35a667b`, `b3cab12`, `d6cbb09`, `484c227`, `65e3b5b`, `cfaf976`, `8196f94`, `25e91c3`, `95ead54`, `f95f76b`.
- Area teknis: `apps/api/src/domains`, `libs/database/src/tenants`, `apps/job/src/job.module.ts`.

### NetApps Mobile

- Bukti kontribusi: reusable UI component system, login/OTP/password flows dengan BLoC/API, localization, profile, notification, home/tagihan/transaction pages, skeleton/loading/no-connection states.
- Bukti hash: `2787e18`, `30be807`, `049561a`, `d31c766`, `9e4d600`, `6d5b355`, `1536bf0`, `79dcb92`, `8b894a1`, `d794bb6`, `fb3055f`, `b0d756b`, `e5faa51`, `13cef2b`, `804dda4`.
- Area teknis: `lib/core/widgets/component`, `lib/pages`, `lib/pages/auth/bloc`, `lib/pages/beranda/bloc`, `lib/l10n`, `lib/utils`.

## Aturan Narasi Deck

- Klaim harus menyebut kontribusi berbasis commit, bukan outcome bisnis yang tidak terbukti.
- Hindari klaim absolut seperti `100%`, `nol`, `permanen`, `bebas error`, `hilang total`, atau angka operasional tanpa bukti.
- Bedakan kontribusi backend, mobile, dan shared codebase lineage.
