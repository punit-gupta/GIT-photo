# Multi-Gallery Photo & Video Viewer

## Features

The updated `index.html` now provides the following features:

### 1. **Multiple Gallery Support**
   - Browse through multiple galleries from different JSON files
   - Currently configured for:
     - 2012 Convocation (`photos_2012.json`)
     - 2016 Collection (`photos_2016_remote.json`)
   - Easy to add more galleries by editing the `GALLERIES` array in the script

### 2. **Image and Video Support**
   - Automatically detects media type (image or video)
   - Supported video formats: `.mp4`, `.webm`, `.ogv`, `.mov`, `.avi`, `.mkv`
   - Video player with controls (play, pause, volume, fullscreen)
   - Photos with responsive image loading

### 3. **Gallery Tabs**
   - Visual tabs at the top to switch between galleries
   - Active tab is highlighted
   - Clean, intuitive navigation

### 4. **Media Badges**
   - Visual indicators showing "PHOTO" or "VIDEO"
   - Play icon appears on videos on hover

### 5. **Full-Screen Viewer Modal**
   - Click on any media to view in full-screen
   - Supports both images and videos
   - Image counter showing current position (e.g., "1 / 100")

### 6. **Navigation Controls**
   - Previous/Next buttons for browsing media
   - Keyboard shortcuts:
     - Left Arrow: Previous media
     - Right Arrow: Next media
     - Escape: Close modal
   - Circular navigation (goes back to start after reaching end)

### 7. **Hover Effects**
   - Gallery items scale up on hover
   - Overlay with media name appears on hover
   - Play icon visible on video thumbnails

### 8. **Responsive Design**
   - Mobile-friendly layout
   - Adaptive grid for different screen sizes
   - Touch-friendly buttons

### 9. **Security**
   - Password protection with session storage
   - Default password: "punit123"

### 10. **Performance**
   - Lazy loading of images
   - Efficient gallery rendering
   - Smooth animations

## How to Use

### Add More Galleries
Edit the `GALLERIES` array in the JavaScript section:

```javascript
const GALLERIES = [
    { id: 'gallery-2012', name: '2012 Convocation', file: 'photos_2012.json' },
    { id: 'gallery-2016', name: '2016 Collection', file: 'photos_2016_remote.json' },
    { id: 'gallery-2020', name: '2020 Events', file: 'photos_2020.json' }  // Add new gallery
];
```

### JSON Format
Your JSON files should follow this format:

```json
{
    "photos": [
        {
            "src": "path/to/image.jpg",
            "name": "Image Name"
        },
        {
            "src": "path/to/video.mp4",
            "name": "Video Name"
        }
    ]
}
```

### Change Password
Edit the password in the script:
```javascript
const CORRECT_PASSWORD = "your-new-password";
```

## Browser Compatibility
- Modern browsers supporting:
  - ES6 JavaScript
  - CSS Grid
  - HTML5 Video
  - Fetch API
  - CSS Backdrop Filter

## File Structure
```
e:\git\GIT-photo\
├── index.html                  # Main gallery page
├── photos_2012.json           # 2012 photos data
├── photos_2016_remote.json    # 2016 photos data
└── time.html                  # Timeline view (separate file)
```
