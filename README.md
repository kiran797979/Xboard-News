# Xboard News

A modern, responsive news feed web application that aggregates and displays news articles from multiple RSS sources in a clean, carousel-based UI.

## Features
- Fetches and displays news from multiple RSS feeds
- Responsive design using Bootstrap 5
- Accordion and carousel UI for easy navigation
- Clickable articles open in new tabs
- Simple, static site (no backend required)

## Project Structure
```
├── index.html                # Main entry point
├── resources/
│   ├── css/                  # Stylesheets (Tailwind, custom CSS)
│   ├── js/                   # Main JavaScript logic
│   └── data/                 # RSS feed sources
├── assessment/               # Cypress integration tests
│   ├── pages/                # Page objects for tests
│   ├── plugins/              # Cypress plugins
│   ├── specs/                # Test specifications
│   ├── cypress.json          # Cypress config
│   └── package.json          # Test dependencies/scripts
├── runAssessment.sh          # Script to run tests
├── package.json              # Project dependencies (http-server)
└── tailwind.config.js        # Tailwind CSS config
```

## Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (for running a local server or tests)

### Running Locally
1. **Install dependencies:**
   ```sh
   npm install
   ```
2. **Start a local server:**
   ```sh
   npx http-server -p 8081
   ```
3. **Open your browser:**
   Visit [http://localhost:8081](http://localhost:8081)

### Running Tests
1. **Install test dependencies:**
   ```sh
   cd assessment
   npm install
   ```
2. **Run Cypress tests:**
   ```sh
   npm run test
   ```
   Or use the provided script from the project root:
   ```sh
   ./runAssessment.sh
   ```

## Netlify Deployment
- **Branch to deploy:** `main`
- **Base directory:** *(leave blank)*
- **Build command:** *(leave blank)*
- **Publish directory:** `.`

Netlify will serve your site directly from the root directory. No build step is required.

## Data Source
- RSS feeds are defined in `resources/data/magazines.js`.
- The app fetches and displays articles from these sources using the [rss2json API](https://rss2json.com/).

## Testing
- Integration tests are written using [Cypress](https://www.cypress.io/).
- Tests cover UI elements, carousel functionality, and RSS feed rendering.
- See `assessment/specs/homePageSpec.js` for details.

## Author
B Manoj Kiran

## License
MIT 