# 🌌 Starlight Family Tree

A beautiful, zero-backend family tree application that runs entirely in your browser. Create, visualize, and share your family tree with an intuitive drag-and-drop interface.

![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## ✨ Features

- **🎨 Beautiful UI** - Modern, space-themed design with smooth animations
- **🖱️ Drag & Drop** - Fluid drag-and-drop interface for arranging family members
- **👨‍👩‍👧‍👦 Parent-Child Relationships** - Visual lines connecting family members with multiple parent support
- **📸 Photo Support** - Add photos via URL or upload local images
- **💾 Multiple Save Options**
  - Save as JSON file
  - Export as self-contained HTML (share a single file!)
  - Generate shareable URL links (Base64 encoded in URL fragment)
- **📂 Load from File** - Import previously saved JSON or HTML files
- **🔄 Auto-Save** - Automatic localStorage backup
- **⌨️ Keyboard Shortcuts** - Ctrl/Cmd+S to save, Delete to remove selected person
- **🌐 Zero Backend** - Everything runs locally in your browser
- **🔒 Privacy First** - No servers, no tracking, your data stays with you

## 🚀 Getting Started

### Option 1: Open Directly
Simply open `index.html` in any modern web browser. That's it!

### Option 2: Local Server (Recommended)
For the best experience, serve via HTTP:

```bash
# Python 3
python3 -m http.server 8765

# Python 2
python -m SimpleHTTPServer 8765

# Node.js (with npx)
npx http-server -p 8765
```

Then open `http://localhost:8765/index.html` in your browser.

## 📖 How to Use

### Adding People

1. Fill in the form on the left sidebar:
   - **Full name** (required)
   - **Years** (e.g., "1950–2012")
   - **Notes** (short description)
   - **Photo** (URL or upload file)

2. Click **"Add Person"** button

3. The new card appears on the canvas - drag it to position

### Creating Relationships

1. Select a **parent** from the first dropdown
2. Select a **child** from the second dropdown
3. Click **"Link Parent → Child"**
4. A smooth curved line connects them!

💡 **Tip:** You can link multiple parents to one child for complex family structures.

### Arranging Your Tree

- **Click and drag** any card to move it
- Lines automatically update as you drag
- **Click a card** to select it (shows in the form for editing)
- **Press Delete** while a card is selected to remove it

### Saving & Sharing

#### Save as JSON
- Click **"Save JSON"** button
- Downloads a `.json` file you can load later
- Preserves all data, photos, positions, and relationships

#### Export Self-Contained HTML
- Click **"Download Self-Contained HTML"**
- Creates a single `.html` file with your entire tree embedded
- Share this file with family - they just open it in their browser!
- No need to send multiple files

#### Share by Link
- Click **"Make Share Link"**
- Copies a URL to your clipboard
- Anyone with the link can view your tree
- ⚠️ For large trees with many photos, prefer HTML export

### Loading Saved Trees

1. Click **"Load"** button
2. Select a file:
   - `.json` file (from "Save JSON")
   - `.html` file (from "Download Self-Contained HTML")
   - `.ftree` or `.txt` files with valid JSON
3. Your tree loads with all relationships intact!

## 🎯 Use Cases

- **Family History Projects** - Document your ancestry with photos and notes
- **Genealogy Research** - Organize family connections visually
- **Collaborative Family Trees** - Export and share with relatives for them to add their branch
- **Education** - Teach about family relationships and genealogy
- **Event Planning** - Visualize family connections for reunions or gatherings

## 🛠️ Technical Details

### Built With
- Pure HTML5, CSS3, and vanilla JavaScript
- SVG for relationship lines
- No frameworks or dependencies
- Fully responsive layout

### Browser Compatibility
Works in all modern browsers:
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+

### Data Storage
- **localStorage** - Automatic backup in browser
- **JSON exports** - Portable, human-readable format
- **Embedded HTML** - Self-contained, shareable files
- **URL fragments** - Shareable links (Base64 encoded)

### File Format
JSON structure:
```json
{
  "nodes": [
    {
      "id": "abc123",
      "name": "John Doe",
      "years": "1950–2020",
      "notes": "Grandfather",
      "photo": "https://...",
      "x": 250,
      "y": 150,
      "parents": ["def456", "ghi789"]
    }
  ],
  "selectedId": null
}
```

## 🎨 Customization

The app uses CSS custom properties for easy theming. Edit the `:root` section in the `<style>` tag:

```css
:root{
  --bg1:#0a0b1a;        /* Background gradient start */
  --bg2:#0f1033;        /* Background gradient end */
  --text:#e9ebff;       /* Primary text color */
  --accent:#7c9dff;     /* Accent color (selection outline) */
  /* ... more variables */
}
```

## 🔐 Privacy & Security

- ✅ **No servers** - Everything runs in your browser
- ✅ **No tracking** - No analytics, cookies, or external requests
- ✅ **Your data stays yours** - Only saved where you choose (localStorage, files)
- ✅ **No internet required** - Works completely offline after initial load

## 📋 Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl/Cmd + S` | Save as JSON file |
| `Delete` | Delete selected person |
| `Click` | Select a card |
| `Click + Drag` | Move a card |

## 🤝 Contributing

This is a single-file application designed for simplicity and portability. Feel free to:
- Fork and customize for your needs
- Submit issues for bugs
- Share improvements via pull requests

## 📄 License

MIT License - Feel free to use this for personal or commercial projects!

## 🐛 Troubleshooting

### Cards won't drag
- Make sure you're clicking on the card itself, not a button
- Try refreshing the page
- Check browser console (F12) for errors

### Can't load a file
- Verify the file is valid JSON or a self-contained HTML export
- Check file size (must be under 10MB)
- Open browser console (F12) for detailed error messages

### Lines not showing
- Ensure both parent and child cards exist on the canvas
- Try refreshing the page to redraw connections
- Check that the parent-child link was successfully created

### Photos not loading
- If using URLs, ensure they're publicly accessible
- For uploaded photos, they're embedded as data URLs (may increase file size)
- Check browser console for CORS or loading errors

## 💡 Tips & Best Practices

1. **Start from the top** - Begin with oldest generation and work down
2. **Use consistent naming** - Include maiden names, full names for clarity
3. **Save frequently** - Use Ctrl/Cmd+S or the Save button regularly
4. **Organize spatially** - Arrange generations horizontally at similar Y positions
5. **Backup your work** - Download JSON files and keep copies
6. **Share HTML for viewing** - Family members can open without any setup
7. **Share JSON for collaboration** - Others can load, edit, and send back

## 🎁 Credits

Made with stardust ✨

---

**Questions or feedback?** Open an issue on GitHub or reach out!

**Enjoying Starlight Family Tree?** Give it a ⭐ and share with your family!

