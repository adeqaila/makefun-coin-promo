# Bounty ($BNTY) — the AI bounty hunter of make.fun

Entry for the make.fun bounty **"Launch a coin that sells make.fun"**
(`makefun-coin-promo-01`): https://make.fun/bounty/makefun-coin-promo-01

## The concept

**Bounty** is an AI agent who never sleeps. He lives on make.fun, hunts paid
bounties, builds programs, enters the competitions, and brings the prize home.
The coin isn't a logo slapped on a generic token — the coin *is* the character:
a cheerful little robot bounty hunter in a cowboy hat, clutching the gold star
coin he just collected. Buy $BNTY and you back the hunt.

- **Name:** Bounty
- **Ticker:** $BNTY
- **Logo:** `logo.png` — original artwork, one bold subject (the robot hunter +
  his gold coin), strong outline, high contrast, plain dark-navy background,
  readable at pump.fun thumbnail size (1600×1600, 2.56 MP, 673,256 bytes).
- **Website (required):** https://make.fun/bounty/makefun-coin-promo-01

## What is make.fun?

make.fun is a site where people and their AI agents build programs, enter them
in paid competitions (bounties) and are scored and ranked in the open. It's the
arena where agents prove they can actually build — and get paid for it. Bounty
is the mascot of that arena.

## Pump.fun description

The exact description to use at launch is in `DESCRIPTION.txt` (first line is
the hook, it contains the full bounty URL, says the coin is for this bounty,
and explains make.fun). The website field at launch must be
`https://make.fun/bounty/makefun-coin-promo-01`.

## The program (`main.ts`)

Node 22, standard library only, no network, no wall clock, no files outside
the repository. It copies `LAUNCH.json` to the output directory — that is all
it does. The coin itself is the entry; the judge sees the coin as pump.fun
shows it (logo, name, ticker, description, links).

Run the way the grader does:

```sh
mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts
```

It prints nothing on success and writes `out/LAUNCH.json`.

## LAUNCH.json

Placeholders until the coin is launched on pump.fun from the wallet linked to
the make.fun account. After launch, fill in the real mint address and the
signature of the transaction that created the coin:

```json
{
  "mint": "<the coin's mint, base58, 32 to 44 characters>",
  "create_signature": "<the create transaction's signature, base58, 64 to 88 characters>"
}
```

## License

MIT — see `LICENSE`.
