# Imposter - Social Deduction Word Game

A fun party game where players try to identify imposters among them. Non-imposters receive a secret word from a category, while imposters receive only a one-word hint. Players take turns giving clues about the word without revealing it to imposters, while imposters try to blend in using the clues they hear.

## How to Play

1. **Setup**: Enter the number of players (minimum 3), their names, number of imposters, and select categories
2. **Reveal**: Each player clicks their name to see their role - either the secret word or "IMPOSTER" with a hint
3. **Discuss**: Players take turns giving clues about their word (or pretending to if they're an imposter!)
4. **Vote**: After discussion, players vote on who they think the imposters are
5. **End Game**: See who the imposters were and what the secret word was

## Local Development

### Prerequisites
- Node.js 18.x or higher
- npm (comes with Node.js)

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd Imposter Game
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

4. Open your browser and navigate to:
```
http://localhost:3000
```

For development with auto-reload:
```bash
npm run dev
```

## Deployment

### Deploy to Railway

Railway makes deployment incredibly easy:

1. **Create a Railway account** at [railway.app](https://railway.app)

2. **Install Railway CLI** (optional, for CLI deployment):
```bash
npm install -g @railway/cli
```

3. **Deploy via GitHub (Recommended)**:
   - Push your code to GitHub (see GitHub instructions below)
   - Go to [railway.app](https://railway.app)
   - Click "New Project"
   - Select "Deploy from GitHub repo"
   - Select your repository
   - Railway will automatically detect the Node.js app and deploy it
   - Your app will be live at a Railway-provided URL

4. **Deploy via Railway CLI**:
```bash
railway login
railway init
railway up
```

Your app will be automatically deployed and you'll get a public URL to share!

### Deploy to GitHub

1. **Create a new repository** on [GitHub](https://github.com)

2. **Initialize git** (if not already done):
```bash
git init
```

3. **Add all files**:
```bash
git add .
```

4. **Commit your changes**:
```bash
git commit -m "Initial commit: Imposter game"
```

5. **Add your GitHub repository as remote**:
```bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
```

6. **Push to GitHub**:
```bash
git branch -M main
git push -u origin main
```

### Other Deployment Options

**Render**:
- Connect your GitHub repository
- Select "Web Service"
- Build command: `npm install`
- Start command: `npm start`

**Heroku**:
```bash
heroku create your-app-name
git push heroku main
```

**Vercel**:
```bash
npm install -g vercel
vercel
```

## Features

- Single-page application with no backend database needed
- Responsive design for mobile and desktop
- Dark mode with modern aesthetic
- 55+ animals with themed hints
- Support for multiple categories (expandable)
- Clean, intuitive interface
- No installation required for players - just share the link!

## Tech Stack

- **Frontend**: HTML, CSS, JavaScript (Vanilla)
- **Backend**: Node.js, Express
- **Deployment**: Railway/Heroku/Vercel compatible

## Game Customization

To add more categories or words, edit the `gameData` object in `index.html`:

```javascript
const gameData = {
    animals: [
        { word: "Elephant", hint: "trunk" },
        { word: "Lion", hint: "mane" },
        // Add more animals...
    ],
    // Add new categories here
    foods: [
        { word: "Pizza", hint: "cheese" },
        // Add more foods...
    ]
};
```

Don't forget to add the category checkbox in the HTML:
```html
<label class="checkbox-label">
    <input type="checkbox" name="category" value="foods">
    <span>Foods</span>
</label>
```

## License

MIT

## Contributing

Feel free to submit issues and enhancement requests!

---

Made with ❤️ for party game lovers
