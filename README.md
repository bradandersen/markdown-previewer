# Markdown Live Preview

A lightweight, self-contained markdown editor with live preview that runs entirely in your browser. No installation, no dependencies, no server required - just open the HTML file and start writing.

## Features

- **Live Preview** - See your markdown rendered in real-time as you type
- **Native File Browser** - Open and save files using your OS's native file dialogs (Chrome/Edge/Opera)
- **Open Files** - Load existing markdown files from your computer
- **Save Files** - Export your work as `.md` files with custom filenames and locations
- **Copy HTML** - Copy the rendered HTML to your clipboard with one click
- **Sync Scroll** - Synchronized scrolling between editor and preview panes
- **Reset** - Clear the editor to start fresh
- **Auto-save** - Content automatically persists in browser localStorage
- **Help** - Quick access to markdown syntax guide
- **Offline Ready** - Works completely offline (after initial CDN load for marked.js)

## Screenshots

<!-- Add screenshots here when available -->

## Installation

No installation required! Simply download the file and open it in your browser.

### Quick Start

1. Download `markdown-preview.html`
2. Double-click the file to open it in your default browser
3. Start writing markdown!

### Recommended Browsers

For the best experience with native file dialogs:
- Chrome 86+
- Edge 86+
- Opera 72+

Also works in Firefox and Safari with fallback file handling.

## Usage

### Opening Files
Click the **Open File** button to browse and select a markdown file from your computer. The content will load into the editor and render in the preview pane.

### Saving Files
Click the **Save File** button to save your work:
- **Chrome/Edge/Opera**: Opens a native "Save As" dialog where you can navigate your filesystem and choose the save location
- **Firefox/Safari**: Prompts for a filename and saves to your Downloads folder

### Other Features
- **Copy HTML**: Copies the rendered HTML to your clipboard
- **Reset**: Clears the editor (prompts for confirmation)
- **Sync Scroll**: Toggle synchronized scrolling between editor and preview
- **Help (?)**: Opens the markdown syntax guide in a new tab

## Browser Compatibility

| Feature | Chrome 86+ | Edge 86+ | Opera 72+ | Firefox | Safari |
|---------|------------|----------|-----------|---------|--------|
| Live Preview | ✅ | ✅ | ✅ | ✅ | ✅ |
| Open/Save Files | ✅ | ✅ | ✅ | ✅ | ✅ |
| Native File Browser | ✅ | ✅ | ✅ | ⚠️ Fallback | ⚠️ Fallback |
| Sync Scroll | ✅ | ✅ | ✅ | ✅ | ✅ |
| Copy HTML | ✅ | ✅ | ✅ | ✅ | ✅ |
| Auto-save | ✅ | ✅ | ✅ | ✅ | ✅ |

**Note**: Firefox and Safari use fallback methods for file operations (standard file input and download links) as they don't yet support the File System Access API.

## Technical Details

### Technologies Used
- **HTML5** - Structure and semantics
- **CSS3** - Styling with GitHub-flavored markdown preview styles
- **JavaScript (ES6+)** - Application logic and interactivity
- **[Marked.js](https://marked.js.org/)** - Markdown parsing and rendering (loaded from CDN)
- **File System Access API** - Native file browser dialogs (with fallback support)

### File System Access API
This app uses the modern [File System Access API](https://developer.mozilla.org/en-US/docs/Web/API/File_System_Access_API) for native file operations in supported browsers. This provides:
- Native OS file picker dialogs
- Direct filesystem access
- Better user experience when opening/saving files

For browsers without support, the app automatically falls back to traditional file input and download methods.

### Single-File Architecture
The entire application is contained in a single HTML file:
- No build process required
- No external dependencies (except marked.js from CDN)
- Easy to share and distribute
- Works offline after first load

## Supported Markdown

This editor supports GitHub Flavored Markdown (GFM) including:

- Headers (H1-H6)
- Bold, italic, strikethrough
- Lists (ordered and unordered)
- Code blocks with syntax highlighting
- Inline code
- Blockquotes
- Links and images
- Tables
- Task lists
- Horizontal rules

See the [Markdown Guide](https://www.markdownguide.org/basic-syntax/) for syntax reference.

## Privacy & Security

- **100% Client-Side**: All processing happens in your browser
- **No Data Collection**: No analytics, no tracking, no data sent to any server
- **LocalStorage Only**: Auto-save uses browser localStorage - data never leaves your machine
- **No Account Required**: No login, no signup, completely anonymous

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## Acknowledgments

- [Marked.js](https://marked.js.org/) - Fast markdown parser and compiler
- [Markdown Guide](https://www.markdownguide.org/) - Comprehensive markdown syntax reference
- Inspired by [markdownlivepreview.com](https://markdownlivepreview.com/)

## FAQ

**Q: Do I need an internet connection?**
A: After the first load (which fetches marked.js from CDN), the app works completely offline.

**Q: Where is my data stored?**
A: Your content is automatically saved to your browser's localStorage. It never leaves your computer unless you explicitly save a file.

**Q: Can I use this for large documents?**
A: Yes! The editor handles large documents well, though very large files (>1MB) may experience slight lag in live preview.

**Q: Why doesn't the native file picker work in Firefox?**
A: Firefox doesn't yet support the File System Access API. The app uses a fallback method that still works great, just without the native OS dialog.

**Q: Can I customize the styling?**
A: Yes! Since it's a single HTML file, you can easily edit the CSS in the `<style>` section to customize colors, fonts, and layout.

---

**Made with ❤️ for markdown enthusiasts**
