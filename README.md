# CommonRate

**Conditional group checkout for one fixed-fee expert session.**

CommonRate helps a small, already wallet-native group model one shared USDC fee, a maximum deposit per paid unit, and a fixed allocation of unused deposits. Optional sponsorship reduces participants' successful-round costs. The organizer has no discretionary withdrawal role. The group and provider arrange the actual session offchain.

- [Open the public app](https://commonrate-arc-lab.woodsyowlet258.chatgpt.site/)
- [Get the complete source archive](CommonRate-Source-r6-2026-10-22.zip)
- [Publication scope and provenance](PUBLICATION.md)
- [Archive SHA-256](SOURCE_ARCHIVE.sha256)

## Source layout and local setup

The complete 173-file reproducible source package is **inside the ZIP**, under `commonrate-source/`. It is not unpacked at this repository's root. The archive includes application and contract source, tests, pinned dependencies/configuration, build instructions, integrity records, and third-party notices.

Download the ZIP, verify it against `SOURCE_ARCHIVE.sha256`, then unzip it into a new directory. Start with the extracted `commonrate-source/README.md` and `commonrate-source/docs/BUILD.md`. Use the documented Bun 1.3.14 and Foundry v1.7.1 toolchains. From the extracted source directory:

```sh
bun install --frozen-lockfile
bun run dev
```

The documented app verification command is `bun run check`; the original contract suite is `bun run contracts:test`. These checks do not deploy or transact. Do not run deployment helpers or add broadcast flags as part of a routine build/test run.

## Evidence and limits

Recorded checks for this unchanged runtime passed **372 app tests with 2,765 assertions**, type checking, non-fixing lint, and a production build. The original Solidity suite passed **26 tests**, including 512 conservation fuzz runs. See the archived `docs/VERIFICATION.md` for dates, exact scope, separate historical evidence, and remaining limitations. Publishing this archive is not a new test run or a security audit.

Sandbox is the default and simulates outcomes without a wallet, token movement, or a real booking. The separately selected Live pilot is experimental and user-operated. Public Arc network metadata reads have been observed, but **no CommonRate Mainnet campaign deployment or wallet transaction proof is claimed**. Actual signing, wallet fee handling, service delivery, and contest eligibility remain unestablished. No real customers, revenue, or completed bookings are claimed.

This is an unaudited prototype, not service-delivery escrow. No new project-wide license is selected or granted by publication; the archive preserves existing third-party notices and license texts.
