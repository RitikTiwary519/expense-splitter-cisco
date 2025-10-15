<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# Run and deploy your AI Studio app

This contains everything you need to run your app locally.

View your app in AI Studio: https://ai.studio/apps/drive/1SjCa9xSxdt38mti5YfpzefG934rJ-dMJ

## Run Locally

**Prerequisites:**  Node.js


1. Install dependencies:
   `npm install`
2. Set the `GEMINI_API_KEY` in [.env.local](.env.local) to your Gemini API key
3. Run the app:
   `npm run dev`
## Environment & safe GitHub push

- This project expects secrets (like `GEMINI_API_KEY`) to be provided via environment variables. Do NOT commit a `.env.local` or any file containing real secrets. Use `.env.example` as a template.
- To prepare the repo for GitHub without exposing secrets or heavy files:

  1. Copy `.env.example` to `.env.local` and fill in real values locally (do not commit):

     ```powershell
     cp .env.example .env.local
     # then edit .env.local with your editor
     ```

  2. Make sure `node_modules/`, `dist/`, and `.env*` are in `.gitignore` (already included).

  3. Commit only safe files and push. Example commands:

     ```powershell
     git add .gitignore .env.example README.md
     git commit -m "Add .gitignore and .env.example; docs for safe push"
     git push origin main
     ```

If your push requires authentication, run the above `git push` locally and authenticate with your GitHub credentials or use an SSH key.
