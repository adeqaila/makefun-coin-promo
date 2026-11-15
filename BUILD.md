# BUILD — Bounty ($BNTY) — makefun-coin-promo-01

Dibangun 15 Nov 2026 ~13:06–13:08 WIB (SETELAH buka 13:00 WIB). Semua file baru
di folder ini; tidak ada file/repo/transkrip pra-buka yang dipakai.

## Koin

- **Nama:** Bounty
- **Ticker:** $BNTY
- **Konsep:** Bounty adalah agen AI yang tidak pernah tidur — dia tinggal di
  make.fun, memburu bounty berbayar, membangun program, ikut kompetisi, dan
  membawa pulang hadiahnya. Koin ini BUKAN tempelan: koinnya adalah karakternya
  sendiri, robot pemburu bounty berk topi koboi yang memeluk koin emas bintang
  yang baru dia kumpulkan. Nama, ticker, logo, dan cerita saling nyambung;
  beli $BNTY = mendukung perburuan itu.
- **Website koin (wajib):** https://make.fun/bounty/makefun-coin-promo-01

## Logo

- **Path:** `~/workspace/makefun-coin-promo/build/logo.png`
- **Ukuran:** 673.256 byte (< 5 MiB ✅), 1600×1600 px = 2,56 megapiksel (< 16 MP ✅)
- **Asli buatan sendiri** (media generation, bukan unduh/copy): satu subjek bold
  (robot pemburu bounty + koin emas), outline kuat, kontras tinggi (teal/oranye
  di navy gelap), background polos, terbaca di thumbnail 512px.

## Deskripsi pump.fun (lengkap, di `DESCRIPTION.txt`)

> 🤖 Bounty never sleeps. He's an AI agent who hunts bounties on make.fun —
> building programs, entering paid competitions, and bringing the prize home.
> Every $BNTY holder backs the hunt.
>
> This coin was made for the make.fun bounty "Launch a coin that sells
> make.fun": https://make.fun/bounty/makefun-coin-promo-01
>
> make.fun is a site where people and their AI agents build programs, enter
> them in paid competitions (bounties) and are scored and ranked in the open.
> Think of it as the arena where agents prove they can actually build — and get
> paid for it.
>
> Bounty is the mascot of that arena: part builder, part bounty hunter, all
> hustle. He doesn't sleep, he doesn't quit, and he always collects. If agents
> are going to take over the leaderboard, you might as well hold the coin of
> the one hunting it.
>
> Website: https://make.fun/bounty/makefun-coin-promo-01

Baris pertama hook, memuat link penuh bounty, menyebut bounty ini, menjelaskan
make.fun. Website saat launch WAJIB
https://make.fun/bounty/makefun-coin-promo-01.

## Verifikasi main.ts

```
mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts
```

- Exit code 0, tanpa output (sesuai ekspektasi), `out/LAUNCH.json` terbentuk
  dan identik dengan `LAUNCH.json`. Node v24.22.1. Folder `out/` sudah
  dihapus setelah tes.
- `LAUNCH.json` masih berisi placeholder jelas (mint & create_signature AKAN
  diisi parent SETELAH launch on-chain). Tidak ada nilai dummy yang mirip mint
  asli. JSON valid.

## File di build/

- `main.ts` — Node 22 stdlib only, hanya menyalin LAUNCH.json ke /output
  (berbasis starter resmi kit)
- `LAUNCH.json` — placeholder, menunggu launch
- `logo.png` — logo asli (673.256 byte)
- `README.md` — konsep, nama/ticker, deskripsi, website, instruksi run
- `DESCRIPTION.txt` — deskripsi pump.fun lengkap, siap copy-paste saat launch
- `LICENSE` — MIT
- `BUILD.md` — file ini

## Yang BELUM dilakukan (tugas parent)

- Launch koin di pump.fun (butuh SOL di wallet ter-link + signing terverifikasi
  oleh parent — TIDAK dilakukan subagent ini).
- Isi mint + create_signature ke `LAUNCH.json` setelah launch.
- Buat repo GitHub publik baru (pasca-buka), push, upload logo, set About.
- Submit slot 1 (setelah `check` lokal lolos).
