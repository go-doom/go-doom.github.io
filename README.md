<p align="center"><img src="https://raw.githubusercontent.com/go-doom/brand/main/social/go-doom.png" alt="go-doom/go-doom.github.io" width="720"></p>

# go-doom.github.io

Sources for **go-doom.github.io** — the go-doom landing page.
Built by [Hugo](https://gohugo.io) — same toolchain and same template
shape as [go-quake1.github.io](https://github.com/go-quake1/go-quake1.github.io)
and [go-tpm2.github.io](https://github.com/go-tpm2/go-tpm2.github.io).
Blood-red palette so it reads as a DOOM-family page.

## Layout

```text
.
├── hugo.toml                       Site config + per-repo card params
├── content/
│   └── _index.md                   Homepage marker (empty)
├── layouts/
│   └── index.html                  Homepage body (inline CSS + theme toggle)
├── static/
│   ├── favicon.svg                 Org logo, used as favicon
│   └── img/logo.svg                Org logo, used as hero (88px)
└── public/                         Hugo build output (gitignored — built by CI)
```

## Build locally

```sh
hugo server -D                            # live reload at http://localhost:1313/
hugo --gc --minify                        # production build → ./public/
```

## Deploy

`.github/workflows/hugo.yml` builds + deploys on every push to `main`.
Configure GitHub Pages on the repo with **Source = "GitHub Actions"**
(not "Deploy from a branch").

## Sibling pages

- [go-quake1](https://go-quake1.github.io) — id Tech 1 (1996), active port.
- [go-quake2](https://go-quake2.github.io) — id Tech 2 (1997), reserved.
- [go-quake3](https://go-quake3.github.io) — id Tech 3 (1999), reserved.
- [cloud-boot](https://cloud-boot.github.io) — the UEFI bootloader that
  hands control to the TamaGo DOOM guest.
