# 🎨 AWS Connect Theme Studio

A Tampermonkey userscript that reskins the **Amazon Connect agent workspace**
with five polished themes — including full recoloring of legacy surfaces AWS
never tokenized (banners, tables, sidebars).

![Version](https://img.shields.io/badge/version-4.2.1-blue) ![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Themes
| Theme | Look |
|---|---|
| 🌑 Black Gold | Obsidian + liquid gold |
| 🌃 Midnight Neon | Cyber navy + electric cyan |
| 🌸 Sakura Blush | Soft pastel rose light |
| 💜 Amethyst Royale | Deep violet + glowing amethyst |
| ☀️ AWS Light | Original workspace (clean restore) |

## 📥 Install
1. Install [Tampermonkey](https://www.tampermonkey.net/)
2. Click this link: **[aws-connect-theme-studio.user.js](https://raw.githubusercontent.com/USERNAME/aws-connect-theme-studio/main/aws-connect-theme-studio.user.js)**
3. Tampermonkey opens → **Install**
4. Reload Amazon Connect → click the 🎨 orb (or `Alt+T`)

## ⚙️ How it works
- Overrides CloudScape CSS custom properties with `!important` at high specificity
- **Dynamic token discovery** maps every `--color-*` var (any build hash) to theme roles
- **CSSOM literal rewriter** recolors hardcoded legacy surfaces (`lily` micro-frontend)
- **Catch-all neutral rewriter** flips remaining gray backgrounds/borders/text on dark themes
- Self-heals via MutationObserver + 3s re-assert

## 🔄 Updates
Pushed automatically — Tampermonkey checks periodically and prompts to update.

## 🐛 Known limitations
- Hidden vendor-specific widgets may use non-neutral brand colors (by design, untouched)
- If a surface stays unthemed, [open an issue](https://github.com/USERNAME/aws-connect-theme-studio/issues) with the CSS class name

## 📄 License
MIT
