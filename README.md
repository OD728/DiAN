# 🚫 Discord Hide "Active Now" Column


![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Discord Version](https://img.shields.io/badge/Discord-Web%20%7C%20Desktop-5865F2)
![CSS](https://img.shields.io/badge/CSS-1572B6)


A simple CSS snippet to hide the annoying "Active Now" sidebar on Discord's Friends/Home page for a cleaner interface.
Hides the "Active Now" sidebar on Discord's Friends/Home page for a cleaner interface.


## ✨ What it does

Completely hides the "Active Now" column, including:
- Friends playing games
- Spotify activity
- Voice channel participants
- Other activity statuses

## 🚀 Installation Methods

### Method 1: Browser Extension (Recommended)

**For Stylus** ([Chrome](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne) | [Firefox](https://addons.mozilla.org/en-US/firefox/addon/styl-us/))
1. Install Stylus.
2. Go to Discord in your browser.
3. Click Stylus icon → "Write style for discord.com".
4. Paste CSS code and save.

**For other extensions** (Tampermonkey, etc.): Create a new user style/script targeting `discord.com` and add CSS in a `GM_addStyle()` call.

### Method 2: Discord Client Mods

**BetterDiscord**:
1. Install or use a [third party client](https://github.com/Discord-Client-Encyclopedia-Management/Discord3rdparties).
2. Save CSS as `HideActiveNow.theme.css` in themes folder.
3. Enable in third party client css/themes settings.

**Vencord etc.**: Add CSS to Custom CSS section in settings.


## 📝 The CSS Code

```css
/* Hide the "Active Now" column on the Friends/Home page */
div[class^="nowPlayingColumn"] {
  display: none !important;
}
```

## 🤝 Contributing

Found an issue or improvement? 

- **Discord changed class names?** Open an issue with the new selector
- **Better CSS approach?** Submit a pull request
- **Works with other clients?** Share your experience

## 📜 License

Released into the **public domain** - use freely without attribution.

---

**Simple CSS for a cleaner Discord experience** ✨
