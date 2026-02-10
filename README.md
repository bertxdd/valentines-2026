# 💖 Romantic Valentine's Day Website

A beautiful, responsive HTML Valentine's Day website to ask someone to be your Valentine. Fully customizable with no backend required.

## 🌹 Features

✨ **Fully Responsive Design** - Works perfectly on mobile, tablet, and desktop
💕 **Romantic Aesthetic** - Soft colors (blush pink, cream, gold accents)
🎵 **Background Music Toggle** - Optional romantic music player
❤️ **Floating Hearts Animation** - Subtle animated hearts in the background
🖼️ **Photo Gallery** - Polaroid-style image gallery with hover effects
💌 **Love Message Section** - Heartfelt message about your feelings
🎉 **Success Animation** - Confetti and celebration effects when she says yes
📱 **Google Fonts** - Beautiful typography with Playfair Display, Dancing Script, and Montserrat
🔧 **Easy to Customize** - Simple configuration at the top of the JavaScript

---

## 📋 How to Use

### 1. **Open the Website**
   - Simply open `index.html` in any web browser
   - No server or backend required

### 2. **Customize Her Name**

#### Option A: Change the default name in the code
1. Open `index.html` in a text editor
2. Find line 325 (in the JavaScript section):
   ```javascript
   const HER_NAME = "[HER NAME HERE]"; // Replace with her actual name
   ```
3. Replace `[HER NAME HERE]` with her actual name:
   ```javascript
   const HER_NAME = "Sarah"; // Example
   ```
4. Save the file

#### Option B: Pass name via URL (no file editing needed)
   - Add `?name=HerName` to the URL when opening
   - Example: `file:///C:/Users/User/Desktop/coding projects/valentines 2026/index.html?name=Sarah`

### 3. **Replace the Photos**

The gallery includes 6 placeholder images. Replace them with your own photos:

1. Open `index.html` in a text editor
2. Find the gallery section (around line 200)
3. For each image, replace the `src` URL:

**Before:**
```html
<img src="https://images.unsplash.com/photo-1522684323590-d24dbb6b0267?w=500&h=400&fit=crop" 
     alt="Our first date" loading="lazy">
```

**After (using local file):**
```html
<img src="path/to/your/photo1.jpg" 
     alt="Our first date" loading="lazy">
```

**Or use a web URL:**
```html
<img src="https://your-image-host.com/photo1.jpg" 
     alt="Our first date" loading="lazy">
```

### 4. **Customize Messages**

#### Hero Section (Welcome message)
Find this section around line 160:
```html
<h1>I've been wanting to ask you something...</h1>
<div class="hero-subtitle">Will you <span class="name">be my Valentine</span>?</div>
<p class="hero-intro">
    There's something special about the way you make me smile...
</p>
```

#### Love Message Section
Find this section around line 210:
```html
<p>
    I want you to know that every moment spent with you is a treasure...
</p>
```

#### Final Message
Find this in the JavaScript (line 326):
```javascript
const CUSTOM_MESSAGE = "No matter what, I'm grateful for you. ✨";
```

---

## 🎨 Customization Guide

### Change Colors

The website uses CSS variables for colors. Edit these in the `<style>` section:

```css
:root {
    --primary-pink: #FFB6D9;    /* Light pink */
    --dark-pink: #E75480;       /* Medium pink */
    --soft-red: #C73E6D;        /* Dark pink/red */
    --cream: #FFF8F5;           /* Cream background */
    --white: #FFFFFF;           /* White */
    --gold: #D4AF81;            /* Gold accents */
}
```

Replace these hex codes with your preferred colors.

### Change Fonts

The website uses Google Fonts. To change them, find this in the `<head>` section:

```html
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700;800&family=Montserrat:wght@300;400;500;600&family=Dancing+Script:wght@400;700&display=swap" rel="stylesheet">
```

Visit [Google Fonts](https://fonts.google.com) to find other fonts you like!

### Add/Remove Gallery Images

To add more images, copy this template in the `.gallery-grid` section:
```html
<div class="gallery-item polaroid-style">
    <img src="your-image-url.jpg" alt="Description" loading="lazy">
</div>
```

To remove images, simply delete the entire `<div class="gallery-item">...</div>` block.

---

## 🎵 Background Music

The website comes with a default background music URL. To use your own:

1. Find this line around line 145:
```html
<audio id="bgMusic" loop volume="0.3">
    <source src="https://assets.codepen.io/assets/songs/harpoon.mp3" type="audio/mpeg">
</audio>
```

2. Replace the `src` URL with your own audio file:
```html
<audio id="bgMusic" loop volume="0.3">
    <source src="path/to/your/music.mp3" type="audio/mpeg">
</audio>
```

You can find royalty-free romantic music at:
- [YouTube Audio Library](https://www.youtube.com/audiolibrary)
- [Free Music Archive](https://freemusicarchive.org/)
- [Pixabay Music](https://pixabay.com/music/)

---

## 📱 Responsive Design

The website automatically adapts to all screen sizes:
- **Desktop** (1200px+) - Full layout with side-by-side gallery items
- **Tablet** (768px-1199px) - Optimized grid layout
- **Mobile** (below 768px) - Single column layout with larger touch targets

No additional configuration needed!

---

## 🚀 Deployment

### Option 1: Share as File
Simply send the `index.html` file to her via email or file sharing.

### Option 2: Host Online (Free Options)

#### GitHub Pages
1. Create a GitHub account
2. Create a new repository named `valentines`
3. Upload `index.html` and any image files
4. Enable GitHub Pages in settings
5. Share the generated URL

#### Netlify
1. Go to [Netlify Drop](https://app.netlify.com/drop)
2. Drag and drop your `index.html` file
3. Get an instant shareable link

#### Vercel
1. Go to [Vercel](https://vercel.com)
2. Click "Import Project"
3. Upload your files
4. Get a live URL

---

## 🎁 Quick Start Checklist

- [ ] Open `index.html` in a text editor
- [ ] Change `[HER NAME HERE]` to her actual name (line 325)
- [ ] Replace placeholder images with your photos
- [ ] Customize the love messages
- [ ] (Optional) Change colors to match your preference
- [ ] Test on mobile by opening in a phone browser
- [ ] Share the link or file with her!

---

## 💡 Tips & Tricks

1. **Take a screenshot** of the success page for a cute keepsake
2. **Add more photos** by copying the gallery item template
3. **Mobile preview** - Open DevTools (F12) and toggle device toolbar
4. **Test everything** before sending - click all buttons, scroll through all sections
5. **Customize the emoji** - Replace any emoji with your favorites!

---

## 🐛 Troubleshooting

**Images not showing?**
- Check that image URLs are correct
- Make sure image files are in the same folder as `index.html` (if using local files)
- Try absolute URLs (full web addresses) instead of relative paths

**Music not playing?**
- Some browsers block autoplay - she'll need to click the 🎵 button first
- Make sure the audio URL is accessible and not blocked

**Name not updating?**
- Make sure you saved the file after editing
- Hard refresh the browser (Ctrl+F5 or Cmd+Shift+R)
- Try using the URL method: `index.html?name=Sarah`

**Colors look different?**
- Clear browser cache
- Try in an incognito/private window
- Check CSS is saved properly

---

## 📝 License

This website template is yours to use and customize freely. Created with love! 💖

---

## 💕 Extra Ideas

- Add a dedicated photo of the two of you as the hero section background
- Include a timeline of your relationship milestones
- Add a "reasons why I love you" list
- Include a playlist of your favorite songs together
- Add a gift idea section with linked Amazon wishlist
- Include a date planning section with activity suggestions

---

**Good luck! She's going to love it! 💖✨**
