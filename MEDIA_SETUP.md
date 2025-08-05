# 🎵📸🎥 Media Setup Guide

## Quick Setup Instructions

### **Step 1: Add Music Files**
1. Place your MP3 files in `assets/music/` directory
2. Name them exactly as follows:
   - `home_song.mp3`
   - `letter_song.mp3` 
   - `memories_song.mp3`
   - `surprise_song.mp3`
   - `gallery_song.mp3`

### **Step 2: Add Photos**
1. Place your JPG/PNG files in `assets/images/` directory
2. Name them exactly as follows:
   - `gallery1.jpg` to `gallery12.jpg` (for gallery photos)
   - `memory1.jpg` to `memory12.jpg` (for memory timeline)

### **Step 3: Add Videos**
1. Place your MP4 files in `assets/images/` directory
2. Name them exactly as follows:
   - `birthday_video.mp4`
   - `love_video.mp4`
   - `memories_video.mp4`
   - `surprise_video.mp4`

## Detailed File Requirements

### **Music Files:**
- **Format**: MP3 (recommended) or WAV
- **Quality**: 128kbps minimum, 320kbps recommended
- **Duration**: 2-5 minutes per song
- **Size**: Keep under 10MB per file

### **Image Files:**
- **Format**: JPG, PNG, or SVG
- **Size**: 800x600px minimum, 1920x1080px recommended
- **Quality**: High quality, clear images
- **Size**: Keep under 2MB per image

### **Video Files:**
- **Format**: MP4 (recommended) or WebM
- **Resolution**: 720p minimum, 1080p recommended
- **Duration**: 10-60 seconds for short clips
- **Size**: Keep under 50MB per video

## How to Replace Placeholders

### **For Photos:**
Replace the emoji placeholders in the HTML with actual image tags:

```html
<!-- Instead of this: -->
<div style="font-size: 4rem;">💕</div>

<!-- Use this: -->
<img src="assets/images/gallery1.jpg" style="width: 100%; height: 250px; object-fit: cover; border-radius: 10px;">
```

### **For Videos:**
Replace the video placeholders with actual video tags:

```html
<!-- Instead of this: -->
<div style="font-size: 4rem;">🎥</div>

<!-- Use this: -->
<video controls style="width: 100%; border-radius: 10px;">
    <source src="assets/images/birthday_video.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
```

## File Naming Convention

### **Gallery Photos:**
- `gallery1.jpg` - Our First Date
- `gallery2.jpg` - Coffee Together
- `gallery3.jpg` - Sunset Walk
- `gallery4.jpg` - Movie Night
- `gallery5.jpg` - Cooking Together
- `gallery6.jpg` - Dance Night
- `gallery7.jpg` - Beach Day
- `gallery8.jpg` - Stargazing
- `gallery9.jpg` - Birthday Celebration
- `gallery10.jpg` - Holiday Trip
- `gallery11.jpg` - Rainy Day
- `gallery12.jpg` - Anniversary

### **Memory Photos:**
- `memory1.jpg` - First Meeting
- `memory2.jpg` - First Conversation
- `memory3.jpg` - First Date
- `memory4.jpg` - First Kiss
- `memory5.jpg` - First Trip
- `memory6.jpg` - First Celebration
- `memory7.jpg` - First Cook Together
- `memory8.jpg` - First Movie
- `memory9.jpg` - First Dance
- `memory10.jpg` - First Gift
- `memory11.jpg` - First Stargazing
- `memory12.jpg` - First Sunrise

### **Videos:**
- `birthday_video.mp4` - Birthday celebration video
- `love_video.mp4` - Romantic moments video
- `memories_video.mp4` - Memory compilation video
- `surprise_video.mp4` - Surprise reaction video

## Suggested Content Types

### **Music Suggestions:**
- **Home Page**: Upbeat, celebratory music
- **Letter Page**: Soft, romantic instrumental
- **Memories Page**: Nostalgic, emotional music
- **Surprise Page**: Magical, exciting music
- **Gallery Page**: Beautiful, peaceful music

### **Photo Suggestions:**
- Your best couple photos
- Travel and adventure shots
- Celebration moments
- Intimate, romantic photos
- Candid moments together

### **Video Suggestions:**
- Short clips of special moments
- Birthday celebrations
- Travel adventures
- Candid, happy moments
- Personal messages

## Troubleshooting

### **Files Not Loading:**
1. Check file names match exactly (case-sensitive)
2. Ensure files are in the correct directory
3. Verify file formats are supported
4. Check file sizes are reasonable

### **Poor Performance:**
1. Compress images to recommended sizes
2. Optimize video files for web
3. Use appropriate file formats
4. Consider using CDN for large files

### **Scrolling Issues:**
The website includes fixes for smooth scrolling, but if you still experience issues:
1. Ensure all CSS files are loaded properly
2. Check for conflicting browser extensions
3. Try different browsers
4. Clear browser cache

## Tips for Best Results

1. **Choose High-Quality Media**: Use the best quality photos and videos you have
2. **Optimize File Sizes**: Compress files to reasonable sizes for fast loading
3. **Test Everything**: Check that all media loads properly after adding
4. **Backup Your Files**: Keep original files safe before compressing
5. **Be Consistent**: Use similar aspect ratios for photos when possible

## Note
The website will work perfectly with the current emoji placeholders even without adding media files. Adding your own photos, videos, and music will make it much more personal and special! 💖 