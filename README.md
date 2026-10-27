# CodeDoctor AI

A web app for reviewing Python, C++, and Java snippets. It flags likely logic and edge-case bugs, explains worst-case time and auxiliary-space complexity, and suggests a refactored version.

## Run locally in VS Code

1. Install [Node.js](https://nodejs.org/) 20 or newer.
2. Open this folder in VS Code.
3. In the integrated terminal, run `npm start`.
4. Visit http://localhost:3000.

To enable AI reviews, copy `.env.example` to `.env`, add your OpenAI API key, and restart the server. The key stays on the server and is excluded from Git. API usage may incur charges. Without a key, the website loads but analysis is unavailable.

```env
OPENAI_API_KEY=your_api_key_here
OPENAI_MODEL=gpt-4.1-mini
PORT=3000
```

## Publish to GitHub

Create an empty repository on GitHub, then run these commands in the project folder:

```bash
git init
git add .
git commit -m "Build CodeDoctor AI code review website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Never commit `.env` or put an API key in browser code. For a public hosted site, deploy the Node server on a Node.js host and add `OPENAI_API_KEY` in its environment settings. GitHub Pages alone cannot run this server endpoint.
