<div align="center">
  <img src="https://raw.githubusercontent.com/Apara-App/.github/main/profile/assets/banner.svg" alt="Apara" width="100%">
</div>

<br>

Apara is a macOS application that runs Windows games and other Windows
programs on Apple Silicon. It looks at a Windows binary, works out how to
run it, explains that decision in plain language, and then runs the program
in an isolated, versioned environment — one that can be checkpointed,
rolled back, and reproduced.

<br>

<p align="center">
  <img src="https://raw.githubusercontent.com/Apara-App/.github/main/profile/assets/library-v2.png" width="49%" alt="The Apara library: Windows games and apps as cards, with tabs for Games, Apps and Stores">
  <img src="https://raw.githubusercontent.com/Apara-App/.github/main/profile/assets/program-detail-v2.png" width="49%" alt="A program page: graphics route, pinned runtime, storage, and why it is set up this way">
</p>

## The premise

A Windows environment should be a **described artifact**, not a directory
that Wine happened to write into. In Apara every environment is a manifest,
a content-addressed runtime, and copy-on-write checkpoints — which is what
makes rollback, reproducibility, and *"what changed?"* answerable
questions rather than folklore.

Six responsibilities carry every program:

| | |
|---|---|
| **Analysis** | the binary is read first — imports, graphics APIs, anti-cheat, instruction set |
| **Plan** | every decision is recorded, with the rationale for each non-default choice |
| **Runtime** | pinned by content hash, so an update cannot break a program that works |
| **Translation** | Direct3D to Metal — and chosen *per executable*, so a storefront can render through DXVK while the game it launches uses Apple's Direct3D |
| **Integration** | a native macOS window, not a remote desktop into somewhere else |
| **Checkpoints** | every risky change gets one first; recovery is ordinary, not an emergency |

And when something cannot work — kernel-level anti-cheat, a graphics path
this Mac does not have — Apara says why, instead of failing quietly.

## Measured, not promised

Compatibility claims here are measurements, each recorded as a
public-domain (CC0) profile keyed to the exact build it was measured on:

- **Grand Theft Auto V Enhanced** — story mode through Apple's Direct3D 12 route
- **Counter-Strike 2** — roughly 150 fps, with graphics selected per executable
- **Assassin's Creed Valhalla** — installed through Ubisoft Connect; a 105-minute session, exited cleanly
- **Dota 2, Warframe, Path of Exile, World War Z, Muck, Brawlhalla** — measured routes, recorded as profiles

Steam, Epic Games Launcher, Battle.net, Ubisoft Connect, and the Rockstar
Games Launcher all run as ordinary programs in the library.

## Where things stand

In active development. The public Mac build is not published yet, and the
repositories open up as the project matures — this page is the public
front door until then.

Website: **[apara.dev](https://apara.dev)**

<br>

<sub>Not affiliated with Apple, CodeWeavers, or the Wine project.</sub>
