# Icon Configuration Manager

🎨 A beautiful and intuitive web application for managing icon configurations with automated GitHub deployment.

## ✨ Features

- **Modern UI Design**: Gradient backgrounds, smooth animations, and responsive layout
- **Icon Preview**: Real-time icon preview in the table with support for emojis and image files
- **Preset Icons**: Quick selection from a collection of preset emoji icons
- **File Upload**: Support for uploading custom icon files (images, .icns, .ico)
- **Clipboard Integration**: Paste icon markers directly from clipboard
- **Import/Export**: Save and load configurations as JSON files
- **Auto Deploy**: One-click deployment to GitHub with automated commit and push
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Interactive Notifications**: Real-time feedback for all operations

## 🚀 Quick Start

### Local Development

```bash
# Install dependencies
npm install

# Start local server
npm start
```

Then open http://localhost:8080 in your browser.

### Deployment

```bash
# Auto deploy to GitHub
npm run deploy
```

Or manually:

```bash
# Add changes
git add .

# Commit
git commit -m "chore: update configuration"

# Push to GitHub
git push origin main
```

## 📖 Usage Guide

1. **Add Configuration**
   - Enter a title for your icon configuration
   - Specify the command or script path
   - Set the working directory (optional)
   - Choose an icon (preset, file upload, or paste marker)
   - Click "➕ Add Entry"

2. **Edit Configuration**
   - Click "✏️ Edit" on any row
   - Modify the values in the form
   - Click "➕ Add Entry" to save changes

3. **Delete Configuration**
   - Click "🗑️ Delete" on any row
   - Confirm the deletion

4. **Import/Export**
   - Click "💾 Export JSON" to download current configuration
   - Click "📥 Import JSON" to load a previously saved configuration

5. **Deploy to GitHub**
   - Click "🚀 Auto Deploy to GitHub" button
   - The application will export the configuration and simulate the deployment process

## 🛠️ Technologies

- HTML5
- CSS3 (Flexbox, Grid, Animations)
- Vanilla JavaScript
- Git/GitHub for version control

## 📁 Project Structure

```
icon-config-manager/
├── index.html          # Main application file
├── package.json        # NPM configuration and scripts
├── README.md          # This file
└── icon-config.json   # Exported configuration (generated)
```

## 🎨 Customization

You can easily customize the application by modifying:

- **Colors**: Update the gradient colors in the CSS
- **Preset Icons**: Modify the `presetIcons` array in the JavaScript
- **Layout**: Adjust the grid and flexbox settings
- **Notifications**: Customize notification messages and timing

## 📝 License

MIT License - feel free to use this project for your needs!

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

Made with ❤️ using modern web technologies
