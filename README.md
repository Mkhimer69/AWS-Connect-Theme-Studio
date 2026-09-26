# 🎨 AWS Connect Theme Studio

<p align="center">
  <img src="https://img.shields.io/badge/version-4.2.4-blue?style=flat">
  <img src="https://img.shields.io/badge/themes-5-blueviolet?style=flat">
  <img src="https://img.shields.io/badge/platform-Amazon%20Connect-232F3E?logo=amazonaws&logoColor=white">
  <img src="https://img.shields.io/badge/engine-Tampermonkey-00485B?style=flat">
  <img src="https://img.shields.io/badge/license-MIT-green?style=flat">
</p>

> A Tampermonkey userscript that reskins the **Amazon Connect agent workspace**
> with five polished themes — including full recoloring of legacy surfaces AWS
> never tokenized (banners, tables, sidebars, flash notifications, threshold cells).

## 🌈 Themes

| Theme | Look |
|---|---|
| 🌑 **Black Gold** | Obsidian + liquid gold |
| 🌃 **Midnight Neon** | Cyber navy + electric cyan |
| 🌸 **Sakura Blush** | Soft pastel rose light |
| 💜 **Amethyst Royale** | Deep violet + glowing amethyst |
| ☀️ **AWS Light** | Original workspace (clean restore) |

<p align="center">
  <img src="assets/black-gold.png" width="49%" alt="Black Gold">
  <img src="assets/midnight-neon.png" width="49%" alt="Midnight Neon">
</p>
<p align="center">
  <img src="assets/sakura-blush.png" width="49%" alt="Sakura Blush">
  <img src="assets/amethyst-royale.png" width="49%" alt="Amethyst Royale">
</p>
<p align="center"><img src="assets/theme-picker.png" width="80%" alt="Theme picker UI"></p>

## 📥 Installation

1. Install [Tampermonkey](https://www.tampermonkey.net/)
2. Click: **[aws-connect-theme-studio.user.js](https://raw.githubusercontent.com/Mkhimer69/AWS-Connect-Theme-Studio/main/aws-connect-theme-studio.user.js)**
3. Tampermonkey opens → **Install**
4. Reload Amazon Connect → click the 🎨 orb (or `Alt+T`) → pick a theme

🔄 **Auto-updates** — Tampermonkey checks periodically and prompts on every new version.

## ⚙️ How It Works

| Layer | What it does |
|---|---|
| 🎛 **Token override** | Overrides CloudScape CSS custom properties with `!important` at high specificity |
| 🔍 **Dynamic token discovery** | Maps every `--color-*` var (any build hash) to theme roles — survives AWS rebuilds |
| 🧱 **CSSOM literal rewriter** | Recolors hardcoded legacy surfaces (`lily` micro-frontend) |
| 🪣 **Catch-all rewriter** | Flips remaining neutral gray backgrounds/borders/text on dark themes |
| 🚨 **Status surfaces** | Flash notifications, alerts & threshold cells repainted via DOM-level styling |
| 🔁 **Self-healing** | MutationObserver + periodic re-assert keeps new UI themed as it renders |

## 🐛 Known Limitations

- Hidden vendor-specific widgets may use non-neutral brand colors (by design, untouched)
- If a surface stays unthemed, [open an issue](https://github.com/Mkhimer69/AWS-Connect-Theme-Studio/issues) with the CSS class name — fixes land fast

## 📄 License

MIT — © 2026 [Fathy Mkhimer](https://github.com/Mkhimer69)

---

<div align="center">
<b>🎨 AWS Connect Theme Studio</b><br><i>Your workspace. Your colors.</i>
</div>
