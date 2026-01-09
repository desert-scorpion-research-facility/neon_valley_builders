# Neon Valley Builders Website

A modern, fast website built with Astro and deployed on GitHub Pages.

## 🚀 Project Structure

```
/
├── public/
│   └── images/          # Your project images go here
├── src/
│   ├── layouts/
│   │   └── BaseLayout.astro   # Main layout template
│   └── pages/
│       ├── index.astro        # Homepage
│       ├── contact.astro      # Contact page
│       └── work/              # Portfolio pages
├── .github/
│   └── workflows/
│       └── deploy.yml         # GitHub Pages deployment
└── package.json
```

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |

## 📦 Deploying to GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to https://github.com/new
2. Name your repository (e.g., `neon_valley_builders`)
3. Make it public
4. Don't initialize with README (we already have one)
5. Click "Create repository"

### Step 2: Update Configuration

Edit `astro.config.mjs` and replace:
- `your-username` with your GitHub username
- `neon_valley_builders` with your repo name (if different)

```js
export default defineConfig({
  site: 'https://YOUR-USERNAME.github.io',
  base: '/YOUR-REPO-NAME',
});
```

### Step 3: Push Your Code

Run these commands in your terminal:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" → "Pages" (in the sidebar)
3. Under "Build and deployment":
   - Source: Select "GitHub Actions"
4. Wait a few minutes for the deployment to complete
5. Your site will be live at: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

## 📸 Adding Your Images

1. Add your project images to the `public/images/` folder
2. Name them according to the projects (e.g., `bbq1.jpg`, `bbq2.jpg`, etc.)
3. The pages will automatically display them

## 🎨 Customizing

- **Colors & Styling**: Edit the `<style>` sections in each `.astro` file
- **Business Info**: Update contact details in `src/pages/contact.astro`
- **Projects**: Add/edit pages in `src/pages/work/`
- **Navigation**: Update links in `src/layouts/BaseLayout.astro`

## 📝 How Astro Works

Astro is a modern web framework that:
- Builds static HTML (super fast!)
- Uses components (reusable pieces)
- Supports multiple file types (.astro, .md, etc.)
- Ships zero JavaScript by default (great for performance)

Each `.astro` file has two parts:
1. **Frontmatter** (between `---`): JavaScript code that runs at build time
2. **Template**: HTML/CSS that becomes your page

## 🆘 Need Help?

- [Astro Documentation](https://docs.astro.build)
- [GitHub Pages Documentation](https://docs.github.com/pages)
- Check the deployment status in the "Actions" tab on GitHub

---

Built with ❤️ using Astro
