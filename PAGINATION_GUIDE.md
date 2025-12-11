# Updated Gallery Features

## New Changes - Home Page Icons with Pagination

### Home Page (Gallery Selection)
- Landing page shows gallery icons instead of tabs
- Each gallery displays:
  - Large emoji icon (📷 for photos, 🎥 for videos)
  - Gallery name
  - Total number of items
- Click on any gallery to view its photos/videos

### Gallery View with Pagination
- Shows **20 photos/videos per page**
- Clean pagination controls below the gallery
- Shows current position (e.g., "Showing 1 - 20 of 1097 items")
- Pagination features:
  - **Previous/Next buttons** to navigate between pages
  - **Page number buttons** for direct access
  - **Disabled state** for Previous/Next when at boundaries

### Navigation
- **Back to Galleries** button at the top to return to home page
- Click any photo/video to open full-screen modal viewer
- Arrow keys, keyboard shortcuts still work in modal

### How It Works

#### Starting Page Flow:
1. User logs in → Password verified
2. Home page shows gallery icons (2012 Convocation, 2016 Collection)
3. Click icon → Opens gallery with first 20 items
4. Use pagination to browse pages
5. Click Back to return to home page

#### Features Maintained:
✅ Full-screen modal for images and videos
✅ Keyboard navigation (Arrow keys, Escape)
✅ Previous/Next buttons in modal
✅ Media badges (PHOTO/VIDEO)
✅ Play icons on videos
✅ Responsive design
✅ Password protection

### Customization

To change items per page, edit this line in the JavaScript:
```javascript
const ITEMS_PER_PAGE = 20;
```

To add gallery emoji icons, modify the GALLERIES array:
```javascript
const GALLERIES = [
    { id: 'gallery-2012', name: '2012 Convocation', file: 'photos_2012.json', icon: '📷' },
    { id: 'gallery-2016', name: '2016 Collection', file: 'photos_2016_remote.json', icon: '🎥' }
];
```

Change the `icon` property to any emoji you like! Examples:
- 📷 Camera
- 🎥 Video
- 🎬 Movie clapper
- 🖼️ Picture frame
- 🏖️ Beach scene
- 🏔️ Mountain
- 🎉 Party
