---
name: web-search
description: Search the public web using Startpage and return concise, relevant results with titles, URLs, and short summaries.
version: 1.0.0
compatibility: Google AI Edge Gallery on iOS and Android
meta
  search-engine: Startpage
  query-url: https://www.startpage.com/sp/search?query=%s
---

# Web Search

Use this skill whenever the user asks to search the web, find current information, verify facts, compare recent sources, or gather evidence from public websites.

## Goal

Search Startpage for relevant public web pages and return:
- The best matching result or results.
- A short summary of each result.
- The source title and URL.
- A clear answer based on the retrieved pages.

## Search URL

Use Startpage search strings in this format:

`https://www.startpage.com/sp/search?query=%s`

Replace `%s` with the user's query, URL-encoded. Startpage documents this exact format for browser search strings [web:24].

## Search strategy

1. Convert the user request into a short search query.
2. Prefer 2 to 5 keywords for broad searches, or a natural-language question when needed.
3. Search Startpage using the query URL above.
4. Review the top results and identify the most relevant pages.
5. Open the best result pages when details need verification.
6. Prefer primary or authoritative sources when possible.
7. If results are weak, broaden the query and search again.

## Result selection rules

Choose pages that are:
- Directly relevant to the query.
- Recent when the topic is time-sensitive.
- From authoritative or well-known sources when possible.
- Clear enough to summarize accurately.

Avoid:
- Duplicate results.
- Low-quality or spam pages.
- Pages that do not answer the question.

## Output format

Return results in this structure:

- Answer: One or two sentences directly answering the request.
- Results:
  - Title — URL
  - Short summary
  - Why it matters
- Notes: Mention uncertainty or missing context only if necessary.

## When to use this skill

Use this skill for:
- Current events.
- Product research.
- Technical lookups.
- Fact checking.
- Finding sources.
- Comparing public information from the web.

## Limitations

- Do not claim information that was not found in search results or source pages.
- Do not invent citations.
- If Startpage returns weak or no results, say so and suggest a refined query.

## Examples

### Example query
Search for: latest Apple Vision Pro battery life

### Example behavior
1. Search Startpage.
2. Open the most relevant result pages.
3. Summarize the verified findings.
4. Return the source titles and URLs.
