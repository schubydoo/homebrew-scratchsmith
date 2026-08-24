# homebrew-scratchsmith

Homebrew tap for [**Scratchsmith**](https://github.com/schubydoo/scratchsmith) — the
daemonless supply-chain packager for prebuilt dynamic Linux binaries.

```sh
brew install schubydoo/scratchsmith/scratchsmith
```

> **Linux only.** Scratchsmith packs Linux ELF binaries into `FROM scratch` OCI images,
> so the formula ships the signed Linux (amd64 + arm64) release binaries. Use Homebrew on
> Linux or WSL.

## How this tap stays current

The canonical formula lives in the main repo at
[`Formula/scratchsmith.rb`](https://github.com/schubydoo/scratchsmith/blob/main/Formula/scratchsmith.rb),
where its version/URL/checksums are regenerated on every release. This tap mirrors that
file automatically via `sync-formula.yml` (dispatched right after each release bump, with
a daily cron as a fallback). Don't hand-edit `Formula/scratchsmith.rb` here — changes are
overwritten by the next sync.

## Verifying

Release artifacts are cosign-signed with SLSA provenance — see
[Verifying releases](https://schubydoo.github.io/scratchsmith/latest/#verifying-releases).
