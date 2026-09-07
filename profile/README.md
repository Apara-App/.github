<div align="center">
  <img src="https://raw.githubusercontent.com/Apara-App/.github/main/profile/assets/banner.svg" alt="Apara" width="100%">
</div>

<br>

Apara is a macOS application that runs Windows games and other Windows
programs on Apple Silicon. It looks at a Windows binary, works out how to
run it, explains that decision in plain language, and then runs the program
in an isolated, versioned environment — one that can be checkpointed,
rolled back, and reproduced.

In practice that means graphics are chosen per executable — a storefront
can render through DXVK while the game it launches uses Apple's Direct3D —
every environment stays pinned to the exact runtime it was verified with,
so an update cannot break a program that works, and when something cannot
work — kernel-level anti-cheat, a graphics path this Mac does not have —
Apara says why instead of failing quietly.

Measured, not promised: GTA V Enhanced, Counter-Strike 2 at roughly
150 fps, Assassin's Creed Valhalla through Ubisoft Connect, and more —
each recorded as a reproducible, public-domain compatibility profile keyed
to the exact build it was measured on.

Website: **[apara.dev](https://apara.dev)**

The project is in active development.

<br>

<sub>Not affiliated with Apple, CodeWeavers, or the Wine project.</sub>
