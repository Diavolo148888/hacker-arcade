# HACKER ARCADE

```
  four games. one terminal. zero quarters.
  retro CRT hacking mini-games
```

A browser arcade of hacking-themed mini-games wrapped in a full CRT
aesthetic: scanlines, screen flicker, phosphor glow, a BIOS boot
sequence, and glitching title text. Every game teaches a real security
instinct while it kills your time.

Built with vanilla HTML/CSS/JS — no frameworks, no build step, no
dependencies. Drop it on GitHub Pages and it runs.

## The games

| # | Game | The skill it trains |
|---|---|---|
| 01 | **PASSWORD CRACK** | hash cracking with transform rules — leetspeak, appends, capitalization against the clock |
| 02 | **TRACE THE ROUTE** | reading traceroute hops and reasoning about network paths |
| 03 | **PHISH SPOT** | spotting real phishing URLs — actual lookalike-domain tricks (faceb00k, brand-in-path, homoglyphs), the same heuristics as real detectors |
| 04 | **PORT ROULETTE** | service-to-port reflexes (21 FTP, 443 HTTPS, 6379 Redis...) |

Every game has lives/strikes, a countdown timer, level scaling, and a
scoring system that rewards speed.

## Run it

Open `index.html` — that's it. Or serve it:

    python3 -m http.server 8080
    # then: http://localhost:8080

Deploy: GitHub Pages / any static host — it's a folder of files.

## Structure

    index.html      the cabinet: CRT shell, boot sequence, game grid, iframe viewport
    games/
      crack.html    password cracking game
      trace.html    traceroute game
      phish.html    phishing URL game (real lookalike patterns)
      ports.html    port-matching game

## Design notes

- The CRT overlay is pure CSS: repeating-linear-gradient scanlines, a
  radial vignette, and a keyframed flicker
- The boot sequence is a timed text writer before the cabinet reveals
- The toy hash in PASSWORD CRACK is a checksum-style demo, not real
  crypto — the point is the cracking workflow, not the hashing
- All motion respects `prefers-reduced-motion`

## Author

**John Mark "mako" Alojado** — [github.com/Diavolo148888](https://github.com/Diavolo148888)

MIT License — see LICENSE.
