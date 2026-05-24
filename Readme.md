# Web Search Skill

A custom Google AI Edge Gallery skill that searches the public web using Startpage.

## What it does

- Searches Startpage using a query URL.
- Finds relevant public web pages.
- Summarizes results into concise, usable answers.

## Install

1. Host this folder on GitHub Pages, a public Git repository, or another static file host.
2. Make sure `SKILL.md` is publicly accessible as plain text.
3. In Google AI Edge Gallery on iOS, open **Skills**.
4. Choose **Add Custom Skill** or **Load from URL**.
5. Paste the URL to the raw `SKILL.md` file.
6. Save and test with a search request.

## Example hosted URL

Use the raw URL to `SKILL.md`, not the GitHub folder page.

Example:
`https://raw.githubusercontent.com/yourname/web-search/main/web-search/SKILL.md`

## Notes

- The `name` field in `SKILL.md` must match the folder name.
- If the app shows a front-matter error, check that the file begins with `---` and contains a matching closing `---`.
- Startpage search strings use:
  `https://www.startpage.com/sp/search?query=%s`
