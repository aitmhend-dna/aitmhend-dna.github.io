# Image Implementation Quick Guide

## 📁 Directory Structure

Create an `img/` folder in your project root:

```
aitmhend-dna.github.io/
├── img/
│   ├── hero-dna-morocco.jpg
│   ├── souss-valley-landscape.jpg
│   ├── paternal-heritage.jpg
│   ├── maternal-heritage.jpg
│   ├── dna-analysis-banner.jpg
│   ├── argan-forest.jpg
│   ├── atlas-mountains.jpg
│   └── ... (other images)
├── index.html
├── styles.css
└── ...
```

## 🔄 How to Replace Placeholders

### Step 1: Generate Image in Midjourney
1. Open `MIDJOURNEY-PROMPTS.md`
2. Copy the prompt for the image you want
3. Paste into Midjourney
4. Select and upscale your favorite result
5. Download the image

### Step 2: Optimize the Image
- **Resize** to recommended dimensions
- **Compress** using tools like TinyPNG or ImageOptim
- **Save** with the exact filename from the guide

### Step 3: Replace in HTML

Look for placeholder comments like this:

```html
<!-- 
MIDJOURNEY PROMPT:
"description of image..."

Replace with: <img src="img/filename.jpg" alt="Description">
-->
<div style="...">Placeholder content</div>
```

Replace with:

```html
<img src="img/filename.jpg" alt="Description" style="width: 100%; height: 400px; object-fit: cover; border-radius: 16px;">
```

## 📋 Priority Replacement List

### 🔴 HIGH PRIORITY (Homepage)

1. **Hero Background** - `index.html` line ~167
   - File: `img/hero-dna-morocco.jpg`
   - Dimensions: 1920x1080
   - Impact: First thing visitors see

2. **Souss Valley Landscape** - `index.html` line ~202
   - File: `img/souss-valley-landscape.jpg`
   - Dimensions: 2560x1080 (ultra-wide)
   - Impact: Main geographic context

3. **Heritage Portraits** - `index.html` line ~257
   - Files: `img/paternal-heritage.jpg` + `img/maternal-heritage.jpg`
   - Dimensions: 1080x1440 each
   - Impact: Key identity visuals

### 🟡 MEDIUM PRIORITY

4. **DNA Analysis Banner** - `index.html` line ~327
   - File: `img/dna-analysis-banner.jpg`
   - Dimensions: 2560x1080

5. **Genetics Lab Banner** - `genetics.html` line ~152
   - File: `img/sequencing-lab.jpg`
   - Dimensions: 2560x1080

### 🟢 LOW PRIORITY (Nice to have)

6. Background patterns and decorative images
7. Additional cultural/historical images
8. Supplementary scientific visualizations

## 💡 Tips for Best Results

### Midjourney Settings
```
Standard prompt + --ar [ratio] --v 6 --q 2
```

- `--ar 16:9` = Standard landscape
- `--ar 21:9` = Ultra-wide banner
- `--ar 3:4` = Portrait orientation
- `--v 6` = Latest model
- `--q 2` = Highest quality

### Alternative Styles

If the default prompts don't match your vision:

**More Photorealistic:**
```
Add: --style raw, photorealistic, 8k photography
```

**More Artistic:**
```
Add: artistic interpretation, painted style, impressionist
```

**More Scientific:**
```
Add: scientific journal illustration, technical diagram, medical textbook style
```

## 🎨 Color Matching

Ensure generated images complement the site's color scheme:

- **Primary:** Deep navy blues (#0A2540, #1E3A5F)
- **Accent:** Bright teal/cyan (#0EA5E9, #06B6D4)
- **Secondary:** Emerald green (#10B981)
- **Warm:** Amber/gold (#F59E0B)

You can adjust in Midjourney with:
```
Add to prompt: "color palette: deep blue, teal, emerald, warm earth tones"
```

## 🔍 Quality Checklist

Before uploading an image, verify:

- [ ] Correct dimensions
- [ ] File size < 500KB (compressed)
- [ ] Sharp focus (not blurry)
- [ ] Colors match site theme
- [ ] Appropriate for scientific/academic context
- [ ] No obvious AI artifacts
- [ ] Proper filename (lowercase, hyphenated)

## 🚀 Quick Implementation

For fastest visual impact, implement in this order:

1. Hero background (30 seconds of work, huge impact)
2. Souss valley landscape (main visual anchor)
3. Heritage portraits (emotional connection)
4. Section banners (professional polish)
5. Everything else (incremental improvements)

## 📝 Example Replacement

**Before:**
```html
<div style="width: 100%; height: 400px; background: linear-gradient(...);">
    📷 Souss-Massa Valley Landscape
</div>
```

**After:**
```html
<img src="img/souss-valley-landscape.jpg" 
     alt="Souss-Massa Valley with Atlas Mountains" 
     style="width: 100%; height: 400px; object-fit: cover; border-radius: 16px; box-shadow: 0 10px 30px rgba(0,0,0,0.2);">
```

---

*Remember: Even replacing just the top 3 priority images will transform the site's visual impact by 80%!*
