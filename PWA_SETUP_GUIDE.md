# 📱 PWA Setup Guide - Assassin Game

## What is a PWA?

A **Progressive Web App (PWA)** lets users install your game on their phone's home screen like a real app - no App Store needed!

**Benefits:**
- ✅ Install to home screen with an icon
- ✅ Opens full-screen (no browser UI)
- ✅ Works offline (after first load)
- ✅ Fast loading
- ✅ Feels like a native app

---

## 📦 Files Included

Your PWA package includes:

1. **index.html** - Main game file (with PWA features)
2. **manifest.json** - App configuration (name, colors, icons)
3. **service-worker.js** - Enables offline functionality
4. **icon.svg** - App icon (crosshair design)
5. **icon-192.png** - Small icon (for Android)
6. **icon-512.png** - Large icon (for Android)

---

## 🚀 Deployment Steps

### Option 1: GitHub Pages (Recommended)

1. **Create a new GitHub repository**
   - Go to https://github.com
   - Click "New repository"
   - Name it: `assassin-game`
   - Make it **Public**

2. **Upload ALL files**
   - Click "uploading an existing file"
   - Drag ALL 6 files from the `pwa` folder
   - Commit changes

3. **Enable GitHub Pages**
   - Go to Settings → Pages
   - Branch: **main** → **/ (root)**
   - Click Save

4. **Wait 2-3 minutes**
   - Your URL: `https://yourusername.github.io/assassin-game`

5. **Add Firebase Config**
   - Edit `index.html` on GitHub
   - Find line ~670: `apiKey: "YOUR_API_KEY_HERE"`
   - Replace with your actual Firebase config
   - Commit changes

---

### Option 2: Netlify

1. Go to https://app.netlify.com
2. Click "Add new site" → "Deploy manually"
3. **Drag the entire `pwa` folder**
4. Wait 30 seconds
5. Get your URL: `https://random-name.netlify.app`
6. Edit `index.html` to add Firebase config

---

### Option 3: Firebase Hosting

If you already set up Firebase:

```bash
cd pwa
firebase deploy --only hosting
```

Your URL: `https://your-project.web.app`

---

## 📱 How Users Install the PWA

### On iPhone (iOS):

1. **Open Safari** (must use Safari, not Chrome!)
2. Go to your deployed URL
3. Tap the **Share button** (box with arrow)
4. Scroll down and tap **"Add to Home Screen"**
5. Tap **"Add"**
6. App icon appears on home screen! 🎉

### On Android:

1. Open in **Chrome**
2. Go to your deployed URL
3. Chrome will show **"Install App"** banner at bottom
4. Tap **"Install"**
5. Or: Menu (⋮) → **"Install app"** or **"Add to Home Screen"**
6. App icon appears on home screen! 🎉

### On Desktop (Chrome/Edge):

1. Open your deployed URL
2. Look for **install icon** (⊕) in address bar
3. Click it and select **"Install"**
4. App opens in its own window!

---

## 🎨 Customizing Your Icons

The current icons are SVG placeholders. For best results:

### Create Proper PNG Icons:

1. **Design a 512x512 icon** (use Figma, Canva, or Photoshop)
   - Transparent or solid background
   - Simple, recognizable design
   - High contrast

2. **Export two sizes:**
   - `icon-192.png` (192x192 pixels)
   - `icon-512.png` (512x512 pixels)

3. **Replace the placeholder files** with your new icons

4. **Upload to your hosting** (GitHub, Netlify, etc.)

### Icon Design Tips:
- ✅ Use the crosshair design from the game
- ✅ Red (#ff4757) on dark/black background
- ✅ Keep it simple - will be small on phones
- ✅ Square format with rounded corners
- ✅ High resolution (512x512)

---

## 🧪 Testing Your PWA

### PWA Checklist:

1. **HTTPS Required** ✅
   - GitHub Pages, Netlify, Firebase all use HTTPS
   - Won't work on `http://` URLs

2. **Manifest.json** ✅
   - Already included and configured

3. **Service Worker** ✅
   - Enables offline mode and caching

4. **Icons** ✅
   - 192x192 and 512x512 included

### Test It:

1. Deploy your site
2. Open on phone (Safari for iOS, Chrome for Android)
3. Check browser console for:
   - "✅ Service Worker registered"
   - "💾 PWA install prompt available"

4. Try installing!

---

## 🔧 Troubleshooting

### "Add to Home Screen" not showing?

**iOS:**
- Must use Safari (not Chrome)
- Must be HTTPS
- Tap Share → scroll down

**Android:**
- Must use Chrome
- Wait 30 seconds after first visit
- Check Menu (⋮) → "Install app"

### Icons not showing?

- Check icon files uploaded correctly
- Must be named exactly: `icon-192.png` and `icon-512.png`
- Try hard refresh: Ctrl+Shift+R (or Cmd+Shift+R)

### App won't work offline?

- Service Worker needs HTTPS
- Visit site at least once while online
- Check browser console for Service Worker errors

### Firebase not working?

- Make sure you added your Firebase config to `index.html`
- Replace ALL placeholder values
- Check Firebase console for errors

---

## 📊 PWA vs Regular Web App

| Feature | Regular Web App | PWA |
|---------|----------------|-----|
| Install to home screen | ❌ | ✅ |
| Full-screen mode | ❌ | ✅ |
| Works offline | ❌ | ✅ |
| App icon | ❌ | ✅ |
| Push notifications | ❌ | ✅ (optional) |
| Feels like native app | ❌ | ✅ |
| App Store required | N/A | ❌ |

---

## 🎯 Next Steps

1. **Deploy your PWA** using GitHub Pages or Netlify
2. **Add your Firebase config** to index.html
3. **Test on your phone** - try installing it!
4. **Share the URL** with friends
5. **Optional:** Create custom icons for a professional look

---

## 💡 Pro Tips

- **Bookmark the URL** before sharing - easier to find later
- **Test on both iOS and Android** if possible
- **The first load requires internet** - after that works offline
- **Updates automatically** when you change files on GitHub
- **No approval process** - deploy instantly!

---

## 🆘 Need Help?

Common issues:

1. **Can't see install prompt**
   - Wait 30 seconds after first visit
   - Try Menu → Install App (Android)
   - Use Safari Share button (iOS)

2. **Game not loading**
   - Check Firebase config is added
   - Check browser console for errors
   - Make sure all 6 files uploaded

3. **Icons look wrong**
   - Replace SVG files with actual PNG icons
   - Use 512x512 and 192x192 sizes
   - Clear cache and reload

---

## ✅ Success!

Once deployed, users can:
- ✨ Install like a real app
- 🎮 Play from home screen
- 🌐 Works everywhere with internet
- 💾 Loads fast with caching
- 📱 Feels native and professional

Enjoy your PWA! 🎉
