# How to develop and deploy the project?

1. Create a new GitHub repository using the [HTML and Vanilla JS template](https://github.com/new?template_name=mits-html-and-vanila-js-v1&template_owner=marketable-it-skills).
2. Place your solution code inside the `/src` folder.
3. Pushing to GitHub triggers GitHub Actions (see `.github/`) to:
   - Build a Docker image
   - Push it to GitHub Container Registry
4. In `docker-compose.yml`, update:
   `image: ghcr.io/<your-github-account>/<your-repo-name>:latest`
5. Run locally:
   ```bash
   docker compose up -d
   ```
6. Visit: [http://localhost](http://localhost)

## Development Setup

### Prerequisites
- Node.js 18+ and npm (for testing framework in Task 1)
- Modern web browser (Chrome recommended for PWA testing)
- Basic HTTP server for PWA development
- Text editor or IDE

### Task 1: Automated Testing Setup
1. Navigate to the provided starter kit for Task 1
2. Install testing dependencies:
   ```bash
   npm install
   ```
3. Run existing tests to understand the structure:
   ```bash
   npm test
   ```
4. Write comprehensive unit tests for the provided JavaScript code
5. Ensure 100% code coverage and mutation testing compliance

### Task 2: Progressive Web App Development
1. Navigate to the provided starter kit for Task 2
2. Start the provided HTTP server:
   ```bash
   npm start
   ```
3. The PWA development server will be available at `http://localhost:3000`
4. The AI news API will be available at `http://localhost:3000/api`
5. Use browser dev tools to test PWA features:
   - Application tab for service worker and manifest
   - Network tab for offline functionality
   - Lighthouse audit for PWA compliance

### Task 3: Web Components Development
1. Navigate to the provided starter kit for Task 3
2. Start the development server:
   ```bash
   npm start
   ```
3. The test website will be available at `http://localhost:8080`
4. Develop the three required web components:
   - `<limited-textarea>`
   - `<confirmation-modal>`
   - `<count-down>`
5. Test components integration in the provided example website

### Testing and Validation
- Use Chrome DevTools for debugging and testing
- Test PWA installation and offline functionality
- Verify web components work across different browsers
- Ensure all automated tests pass with 100% coverage