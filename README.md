# 🚫 Discord Hide "Active Now" Column

A simple CSS snippet to hide the annoying "Active Now" sidebar on Discord's Friends/Home page for a cleaner interface.

![Discord Version](https://img.shields.io/badge/Discord-Web%20%7C%20Desktop-5865F2)
![CSS](https://img.shields.io/badge/CSS-3-1572B6)
![License](https://img.shields.io/badge/license-Public%20Domain-green)

## ✨ What it does

Completely hides the "Active Now" column that shows:
- Friends currently playing games
- Spotify listening activity  
- Voice channel participants
- Other activity statuses

**Before**: Cluttered sidebar with activity feed  
**After**: Clean, focused friends list

## 🚀 Installation Methods

### Method 1: Browser Extension (Recommended)

**For Stylus** ([Chrome](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne) | [Firefox](https://addons.mozilla.org/en-US/firefox/addon/styl-us/))

1. Install Stylus extension
2. Go to Discord in your browser
3. Click the Stylus icon → "Write style for discord.com"
4. Paste the CSS code and save

**For other extensions** (Tampermonkey, etc.)
- Create a new user style/script targeting `discord.com`
- Add the CSS in a `GM_addStyle()` call

### Method 2: Discord Client Mods

**BetterDiscord**
1. Install [BetterDiscord](https://betterdiscord.app/)
2. Save CSS as `HideActiveNow.theme.css` in themes folder
3. Enable in BetterDiscord settings

**Vencord**
1. Install [Vencord](https://vencord.dev/)
2. Add CSS to Custom CSS section in settings

### Method 3: Browser DevTools (Temporary)

1. Press `F12` on Discord web
2. Go to Console tab
3. Paste and run:
```javascript
const style = document.createElement('style');
style.textContent = 'div[class^="nowPlayingColumn"] { display: none !important; }';
document.head.appendChild(style);
```

## 📝 The CSS Code

```css
/* Hide the "Active Now" column on the Friends/Home page */
div[class^="nowPlayingColumn"] {
  display: none !important;
}
```

## 🔧 How it Works

- **Target**: `div[class^="nowPlayingColumn"]` - Selects divs whose class starts with "nowPlayingColumn"
- **Action**: `display: none !important` - Completely hides the element
- **Scope**: Only affects the "Active Now" sidebar, leaves other Discord features intact

## ⚠️ Important Notes

- **Discord updates** may change class names, requiring CSS updates
- **Web version only** - Desktop app modifications need client mods
- **Reversible** - Simply disable/remove the CSS to restore the column
- **No data loss** - Only hides the UI, doesn't affect Discord functionality

## 🐛 Troubleshooting

**CSS not working after Discord update?**
- Discord may have changed the class name
- Check browser DevTools to find the new selector
- Update CSS accordingly

**Still seeing the column?**
- Ensure CSS is properly applied (check browser/extension)
- Try refreshing Discord (`Ctrl+R`)
- Verify you're on the Friends/Home page, not a server

**Want to show it again?**
- Disable the CSS rule in your extension
- Or temporarily add `/* */` around the CSS to comment it out

## 🤝 Contributing

Found an issue or improvement? 

- **Discord changed class names?** Open an issue with the new selector
- **Better CSS approach?** Submit a pull request
- **Works with other clients?** Share your experience

## 📜 License

Released into the **public domain** - use freely without attribution.

---

**Simple CSS for a cleaner Discord experience** ✨