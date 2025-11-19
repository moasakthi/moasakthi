# Personal Website - Siva Sakthi Velan R

A modern, responsive personal website showcasing my portfolio as a Data & AI/ML Architect, Principal Data Engineer, and Cloud Modernization Expert.

## 🌐 Live Demo

Once deployed to GitHub Pages, your website will be available at:
`https://[your-username].github.io/[repository-name]/`

## 📋 Features

- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Modern UI/UX**: Clean, professional design with smooth animations
- **Sections**:
  - Hero section with introduction
  - About section with professional summary
  - Experience timeline
  - Featured projects showcase
  - Skills & technologies
  - Contact information

## 🚀 Getting Started

### Prerequisites

- A GitHub account
- Git installed on your local machine

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

2. Open `index.html` in your web browser, or use a local server:
```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

3. Navigate to `http://localhost:8000` in your browser

## 📦 Deployment to GitHub Pages

### Method 1: Using GitHub Web Interface

1. **Create a new repository** on GitHub (or use existing one)
   - Repository name: `your-username.github.io` (for user site) or any name (for project site)
   - Make it public (required for free GitHub Pages)

2. **Upload files** to the repository:
   - Click "uploading an existing file"
   - Drag and drop all files: `index.html`, `styles.css`, `script.js`
   - Commit the changes

3. **Enable GitHub Pages**:
   - Go to repository **Settings**
   - Scroll to **Pages** section
   - Under **Source**, select `main` branch (or `master`)
   - Click **Save**

4. **Access your site**:
   - User site: `https://your-username.github.io`
   - Project site: `https://your-username.github.io/repository-name`

### Method 2: Using Git Command Line

1. **Initialize git repository** (if not already):
```bash
git init
```

2. **Add files and commit**:
```bash
git add .
git commit -m "Initial commit: Personal website"
```

3. **Add remote and push**:
```bash
git remote add origin https://github.com/your-username/your-repo-name.git
git branch -M main
git push -u origin main
```

4. **Enable GitHub Pages** (follow steps 3-4 from Method 1)

## 🎨 Customization

### Update Personal Information

1. **Edit `index.html`**:
   - Update name, title, and description in the hero section
   - Modify experience, projects, and skills sections
   - Update contact information (email, LinkedIn, etc.)

2. **Update `styles.css`**:
   - Change color scheme by modifying CSS variables in `:root`
   - Adjust fonts, spacing, and layout as needed

### Color Scheme

Edit the CSS variables in `styles.css`:
```css
:root {
    --primary-color: #6366f1;    /* Main brand color */
    --secondary-color: #8b5cf6;  /* Secondary color */
    --text-primary: #1f2937;     /* Main text color */
    /* ... more variables */
}
```

## 📁 Project Structure

```
.
├── index.html          # Main HTML file
├── styles.css          # All styling
├── script.js           # JavaScript functionality
├── README.md           # This file
└── .gitignore          # Git ignore file
```

## 🛠️ Technologies Used

- **HTML5**: Semantic markup
- **CSS3**: Modern styling with CSS Grid, Flexbox, and animations
- **JavaScript**: Interactive features and smooth scrolling
- **Google Fonts**: Inter font family

## 📝 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Feel free to fork this project and customize it for your own use!

## 📧 Contact

**Siva Sakthi Velan R**
- Email: moa_sakthi@live.in
- LinkedIn: [sivasakthivelan](https://www.linkedin.com/in/sivasakthivelan/)
- Location: Chennai, India

---

Built with ❤️ using HTML, CSS, and JavaScript

