# Getting Started - Judooo Webapp

## 🎯 For First-Time Developers

Welcome! This guide will help you set up and start developing the Judooo webapp. Start here before diving into the code.

---

## 📋 Prerequisites

Before you start, make sure you have:

- **Node.js** (v16 or higher) - [Download](https://nodejs.org/)
- **npm** or **yarn** - Comes with Node.js
- **Git** - [Download](https://git-scm.com/)
- **A code editor** - Recommended: [VS Code](https://code.visualstudio.com/)
- **Basic Git knowledge** - Or follow our [Git basics guide](#git-basics)

### Check Installations
```bash
node --version    # Should show v16+
npm --version     # Should show 8+
git --version     # Should show 2.30+
```

---

## 🚀 Quick Setup (5 minutes)

### 1. Clone the Repository
```bash
git clone https://github.com/julxng/judooo-webapp.git
cd judooo-webapp
```

### 2. Read the Documentation
**Start with these (in order)**:
1. **README.md** - Project overview
2. **REQUIREMENTS.md** - What you need to build
3. **BRANDING.md** - Design colors and fonts
4. **This file** - Getting started

### 3. Explore the Structure
```bash
# View project folder structure
tree -I 'node_modules'

# Or on Mac:
find . -not -path '*/\.*' -type d | head -20
```

---

## 🛠️ Development Setup

### Backend Setup

```bash
# Navigate to backend folder
cd backend

# Install dependencies
npm install

# Start development server
npm start

# Server runs on: http://localhost:5000
```

### Frontend Setup

```bash
# In a new terminal, navigate to frontend
cd frontend

# Install dependencies
npm install

# Start development server
npm start

# App opens on: http://localhost:3000
```

---

## 📁 Project Structure

```
judooo-webapp/
├── frontend/                 # React app
│   ├── public/
│   ├── src/
│   │   ├── pages/           # Page components
│   │   ├── components/      # Reusable components
│   │   └── styles/          # CSS files
│   └── package.json
│
├── backend/                 # Node.js + Express API
│   ├── routes/              # API routes
│   ├── models/              # Data models
│   ├── controllers/         # Business logic
│   └── package.json
│
├── docs/                    # Documentation
├── README.md                # Project overview
├── REQUIREMENTS.md          # Full specifications
├── BRANDING.md              # Design guidelines
└── GETTING_STARTED.md       # This file
```

---

## 🎨 Design & Branding

**Key Colors**:
- **Primary (Judooo Red)**: `#FF5533`
- **White**: `#FFFFFF`
- **Dark Gray**: `#2C3E50`
- **Light Gray**: `#F5F5F5`

**Font**:
- **Nunito Sans** (all weights)

**Design Reference**:
- Figma: [Design File](https://www.figma.com/design/RINHgEbIgrd9nGiunic6JM/Untitled)
- Brand Assets: [Google Drive](https://drive.google.com/drive/folders/1OY0aoB14R9q8f0m9kvaGWdLE7hACnQAE)

---

## 📖 Key Concepts

### Events
Art events with bilingual names, dates, locations, images, and metadata.

**Key Fields**:
- `name_vie` / `name_en` - Vietnamese & English names
- `start_date` / `end_date` - Event timing
- `city` / `district` - Location
- `is_free` / `price` - Cost info
- `image_url` - Featured image

### Filters
Dynamic, admin-configurable filters for event browsing:
- Name / Search
- Date range
- Location (city/district)
- Event type
- Price range
- And more...

### Admin Dashboard
Manage events, upload images, configure filters, and select featured events.

---

## 🧪 Testing Your Setup

### Test Backend
```bash
cd backend
npm start

# In another terminal, test API:
curl http://localhost:5000/api/events
```

### Test Frontend
```bash
cd frontend
npm start

# Browser opens at http://localhost:3000
```

### Check Branding
Open your browser dev tools and verify:
- Font is "Nunito Sans"
- Red button color is `#FF5533`

---

## 💻 First Task

**Recommended first task for new developers**:

1. Create `frontend/src/styles/variables.css` with CSS variables:
   ```css
   :root {
     --color-primary: #FF5533;
     --color-white: #FFFFFF;
     --color-dark-gray: #2C3E50;
     --color-light-gray: #F5F5F5;
     --font-primary: 'Nunito Sans', sans-serif;
   }
   ```

2. Create a simple `Button` component that uses these variables

3. Test that colors display correctly

4. Commit your changes:
   ```bash
   git add .
   git commit -m "Add CSS variables and Button component"
   git push
   ```

---

## 🔄 Git Basics

### Create a Feature Branch
```bash
git checkout -b feature/your-feature-name
```

### Make Changes & Commit
```bash
git add .
git commit -m "Clear description of what you did"
```

### Push to GitHub
```bash
git push origin feature/your-feature-name
```

### Create Pull Request
- Go to [GitHub repo](https://github.com/julxng/judooo-webapp)
- Click "Compare & pull request"
- Add description
- Submit for review

---

## 🐛 Troubleshooting

### Port Already in Use
```bash
# Kill process on port 5000 (backend)
lsof -i :5000
kill -9 <PID>

# Or for port 3000 (frontend)
lsof -i :3000
kill -9 <PID>
```

### Dependencies Not Installing
```bash
# Delete node_modules and package-lock.json
rm -rf node_modules package-lock.json

# Reinstall
npm install
```

### Git Clone Failed
```bash
# Try with HTTPS
git clone https://github.com/julxng/judooo-webapp.git

# Or with SSH (if configured)
git clone git@github.com:julxng/judooo-webapp.git
```

---

## 📚 Documentation Map

- **README.md** → Project overview & features
- **REQUIREMENTS.md** → Full specifications & API
- **BRANDING.md** → Design colors & fonts
- **GETTING_STARTED.md** → This file (setup & basics)
- **Figma** → Visual design reference
- **Google Docs** → [Original requirements](https://docs.google.com/document/d/170APgACcxFo_mIm0713bOEncKaEkRPHPduXL58iI6L4/edit)

---

## 🤔 Need Help?

1. **Check documentation** - Most answers are in REQUIREMENTS.md
2. **Review Figma design** - For UI/UX questions
3. **Check Git history** - See what other devs did
4. **Read BRANDING.md** - For design/color questions
5. **Ask in comments** - On pull requests or issues

---

## 🎓 Learning Resources

**Frontend (React)**:
- [React Official Docs](https://react.dev)
- [React Router](https://reactrouter.com/)
- [CSS Variables](https://developer.mozilla.org/en-US/docs/Web/CSS/--*)

**Backend (Node.js + Express)**:
- [Express Docs](https://expressjs.com/)
- [Node.js Docs](https://nodejs.org/en/docs/)
- [RESTful API Design](https://restfulapi.net/)

**Git & GitHub**:
- [Git Guide](https://git-scm.com/book/en/v2)
- [GitHub Guides](https://guides.github.com/)

---

## ✅ Done!

You're all set! 🎉

**Next steps**:
1. Set up your local environment
2. Read REQUIREMENTS.md
3. Check out the Figma design
4. Start building!

**Happy coding!** 🚀

---

**Last Updated**: January 2025
**Questions?** See README.md or BRANDING.md
