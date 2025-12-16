# Fake-Candidates-Checker

A starter Apify Actor scaffold for checking candidate authenticity. The initial version uses the Apify SDK with a CheerioCrawler and is ready to run locally or deploy on the Apify platform.

## Project structure

- `.actor/actor.json` — Actor configuration (name, version, runtime, metadata)
- `.actor/input_schema.json` — Defines Actor input fields and console form
- `.actor/output_schema.json` — Defines Actor output links
- `.actor/dataset_schema.json` — Output view definition for stored dataset items
- `src/main.js` — Actor entry point (Cheerio-based crawler)
- `Dockerfile` — Container definition for deployment

## Development workflow

1. Install dependencies (skip if already installed in your environment):
   ```bash
   npm install
   ```
2. Run the Actor locally:
   ```bash
   apify run
   ```
3. Authenticate with Apify (once per environment):
   ```bash
   apify login
   ```
4. Deploy to the Apify platform:
   ```bash
   apify push
   ```

## Notes
- The Actor uses the default Cheerio-based scaffold and does not include Playwright. Add PlaywrightCrawler only if you need JavaScript rendering.
- Update the Actor name and description in `.actor/actor.json` and `package.json` if you rebrand the project.
- The `storage/` directory is ignored locally to keep the repository clean and should be created automatically by Apify when runs are executed.
