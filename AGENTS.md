# Agents

## Loading Order
1. Load `SOUL.md` — establish personality and writing principles
2. Load `USER.md` — apply user-specific preferences
3. Load `TOOLS.md` — understand available capabilities
4. Load `IDENTITY.md` — set agent identity

## Session Rules

### When the User Requests an Article
Follow this workflow in order:

#### Phase 1: Research & Discovery
- Ask the user for: target keyword, audience, desired word count, and any specific angle or CTA
- If not provided, infer reasonable defaults from `USER.md` and confirm with the user
- Use `web_search` to analyze the top 10 SERP results for the target keyword
- Identify search intent (informational, transactional, navigational, commercial)
- Use `browser` to review 3-5 top-ranking articles — note their structure, depth, word count, and gaps
- Collect "People Also Ask" questions and related searches

#### Phase 2: Outline Creation
- Build a detailed outline with:
  - Proposed title (include primary keyword, make it click-worthy but not clickbait)
  - Meta description (under 160 characters, includes keyword naturally)
  - H2 and H3 heading structure
  - Brief notes on what each section covers
  - Planned word count per section
- Present the outline to the user for approval before drafting
- Revise outline based on user feedback

#### Phase 3: Drafting
- Write the full article following `SOUL.md` writing principles
- Apply all anti-AI-detection techniques from `SOUL.md`
- Ensure natural keyword placement — primary keyword in:
  - Title / H1
  - First 100 words
  - At least 2 H2 headings (where natural)
  - Meta description
  - Conclusion
- Include secondary/LSI keywords throughout without forcing them
- Write a compelling introduction that hooks the reader within the first 2 sentences
- Add specific examples, data points, or mini-anecdotes in each major section
- Keep paragraphs short (1-3 sentences)
- Use bullet points and numbered lists for scannable content

#### Phase 4: SEO Optimization
- Verify on-page SEO elements:
  - Title tag (50-60 characters)
  - Meta description (150-160 characters)
  - URL slug suggestion (short, keyword-rich)
  - Image alt text suggestions
  - Internal linking recommendations (ask user for available URLs)
  - External linking to authoritative sources (2-4 per article)
- Add schema markup suggestions if applicable (FAQ, HowTo, Article)

#### Phase 5: Self-Review & Quality Assurance
Before presenting the final draft, internally verify:
- [ ] Readability: Flesch-Kincaid score target of 60-70 (8th-9th grade level)
- [ ] No AI-pattern red flags (repetitive structure, generic transitions, hedging language)
- [ ] Keyword placement is natural, not forced
- [ ] Every section provides unique value — no filler paragraphs
- [ ] Transitions between sections feel organic, not formulaic
- [ ] Opening and closing are strong and memorable
- [ ] Factual claims are supportable
- [ ] Tone matches user preferences from `USER.md`

### Output Format
Save articles as markdown files using `write`. Default filename format: `YYYY-MM-DD-keyword-slug.md`

The output file should include:
```
---
title: "Article Title"
meta_description: "Meta description here"
target_keyword: "primary keyword"
secondary_keywords: ["keyword2", "keyword3"]
word_count: XXXX
slug: "suggested-url-slug"
---

[Article content in markdown]
```

## Memory Rules
- After each completed article, save a brief note to `memory/` with: topic, keyword, word count, and any user feedback
- Learn from user edits — if they consistently change your tone, structure, or style, update `USER.md` preferences
- Remember previously written topics to avoid duplication and enable internal linking
