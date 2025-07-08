# Narrative Reflection Co-Pilot

A web-based AI tool that guides users through self-reflection by generating metaphorical stories based on their emotions and experiences.

## Setup

1. **Install Node.js**: Download from [nodejs.org](https://nodejs.org) (free).
   - Verify: `node -v` and `npm -v`.

2. **Create Project**:
   ```bash
   mkdir narrative-reflection-copilot
   cd narrative-reflection-copilot
   mkdir src dist .vscode
   ```

3. **Save Files**:
   - Place `index.html`, `package.json`, `tailwind.config.js`, `README.md`, `.gitignore` in the root.
   - Place `input.css` in `src/`.
   - Place `settings.json` in `.vscode/`.

4. **Install Dependencies**:
   ```bash
   npm install
   ```

5. **Build CSS**:
   ```bash
   npm run build
   ```
   Generates `dist/styles.css`.

6. **Test Locally**:
   - Open `index.html` in a browser or run:
     ```bash
     npx http-server
     ```
   - Visit `http://localhost:8080`, type responses, and click "Send" to test the chatbot.

## Deployment to GitHub Pages

1. **Create GitHub Repository**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo-name>.git
   git push -u origin main
   ```

2. **Deploy**:
   - Run `npm run build` and commit `dist/styles.css`:
     ```bash
     git add dist/styles.css
     git commit -m "Add compiled CSS"
     git push
     ```
   - Enable GitHub Pages in Settings (main branch, `/root`).
   - Visit `https://<username>.github.io/<repo-name>`.

## Troubleshooting

- **Unknown at rule @tailwindcss**: Ensure `.vscode/settings.json` exists to suppress linter warnings. Verify `npm run build` works.
- **Send button not working**: Open DevTools (F12 > Console) and check for errors. Verify `dist/styles.css` exists.
- **Syntax errors**: Run `jshint index.html` to check JavaScript. Ensure no stray `return` statements.

## Next Steps

- Replace mock `generateStory` with xAI Grok API (https://x.ai/api).
- Add Firebase Authentication for user accounts.
- Integrate Stripe for premium features (longer stories, audio).
- Share on X and Reddit (e.g., r/selfimprovement) to attract users.