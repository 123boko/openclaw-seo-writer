---
name: seo-writing
description: Write SEO-optimized, human-readable articles that pass AI detection tools. Covers keyword research, content structuring, natural writing techniques, and on-page SEO optimization.
---

# SEO Article Writing Skill

This skill enables the agent to produce high-quality SEO articles that read as if written by an experienced human writer. The content should rank well in search engines while being genuinely useful and engaging to readers.

## Workflow

### Step 1: Keyword Research & Intent Analysis

1. Take the target keyword from the user
2. Use `web_search` to find:
   - Monthly search volume estimates (if available from SERP data)
   - Top 10 ranking URLs
   - "People Also Ask" questions
   - Related searches / LSI keywords
   - Featured snippet opportunities
3. Classify search intent:
   - **Informational**: User wants to learn something → write educational content
   - **Commercial**: User is comparing options → write comparison/review content
   - **Transactional**: User wants to buy/sign up → write conversion-focused content
   - **Navigational**: User looking for specific page → usually not worth targeting

### Step 2: Competitor Content Analysis

1. Use `browser` to visit the top 3-5 ranking pages
2. For each page, note:
   - Total word count
   - Heading structure (H2s, H3s)
   - Content format (listicle, guide, tutorial, etc.)
   - Unique angles or data they include
   - Content gaps — what they missed or covered poorly
3. Identify your content angle:
   - What can you add that competitors don't cover?
   - What format would serve the reader better?
   - Is there a fresher or more opinionated take available?

### Step 3: Create Article Outline

Build a structured outline:

```markdown
# [Title with Primary Keyword]

## Introduction
- Hook: [compelling opening — stat, story, or bold claim]
- Context: [why this matters to the reader]
- Promise: [what they'll learn/gain from reading]

## [H2 Section 1 — address primary intent]
### [H3 Subsection if needed]

## [H2 Section 2 — go deeper]

## [H2 Section 3 — practical application]

## [H2 Section 4 — address "People Also Ask" question]

## [H2 Section 5 — expert tips / advanced insights]

## Conclusion
- Summarize key takeaway (don't repeat everything)
- Clear CTA
```

Present outline to user. Wait for approval before drafting.

### Step 4: Write the Draft

Follow these writing rules strictly:

#### Anti-AI-Detection Writing Techniques

1. **Sentence Length Variation (Burstiness)**
   - Aim for a mix: 5-word sentences, 15-word sentences, 25+ word sentences
   - Never write more than 3 sentences of similar length in a row
   - Use fragments. One-word sentences. They work

2. **Vocabulary Variation (Perplexity)**
   - Don't always use the most common synonym — surprise the reader
   - Use industry jargon sparingly but naturally
   - Include colloquial expressions: "here's the kicker," "long story short," "not gonna lie"

3. **Structural Unpredictability**
   - Don't follow the same paragraph pattern (claim → evidence → conclusion) every time
   - Mix formats within the article: narrative paragraphs, bullet lists, numbered steps, callout boxes, brief Q&A
   - Start some sections with a question, others with a statement, others with a story

4. **Human Imperfections**
   - Use parenthetical asides (like this one — some readers love them)
   - Use em dashes for interruptions — even mid-sentence — to add emphasis
   - Occasionally use informal constructions: "Which, honestly, is kind of the whole point"
   - Use "I think," "in my experience," "from what I've seen" to add personal perspective

5. **Specificity**
   - Replace generic statements with specific ones
   - ❌ "Many businesses have found success with this strategy"
   - ✅ "I worked with a B2B SaaS company that increased organic leads by 47% in 3 months using this exact approach"
   - Include specific numbers, tool names, brand references, and timeframes

6. **Natural Transitions**
   - ❌ "Furthermore," "Additionally," "Moreover," "In conclusion"
   - ✅ "Here's where things get interesting," "But here's the catch," "So what does this actually mean?"
   - Sometimes don't transition at all — just start the next idea

#### SEO Writing Rules

1. **Primary keyword placement**:
   - In the title (H1)
   - Within the first 100 words (naturally)
   - In 2-3 H2 headings where it fits
   - In the meta description
   - In the conclusion
   - In image alt text

2. **Secondary keywords**: Sprinkle naturally throughout — never force them

3. **Content depth**: Cover the topic more thoroughly than any competitor on page 1

4. **Internal links**: Ask user for relevant URLs to link to. Place them contextually, not in a "related articles" dump

5. **External links**: Link to 2-4 authoritative sources (studies, official documentation, reputable publications)

6. **Formatting for readability**:
   - Paragraphs: 1-3 sentences max
   - Use H2 every 200-300 words
   - Use H3 for subsections
   - Include at least one bulleted or numbered list per 500 words
   - Bold key phrases (but don't overdo it)
   - Use tables for comparison data when applicable

### Step 5: On-Page SEO Checklist

After writing, verify and include:

- **Title tag**: 50-60 characters, keyword near the front
- **Meta description**: 150-160 characters, includes keyword, has a CTA or curiosity hook
- **URL slug**: Short, descriptive, includes keyword (e.g., `/best-email-marketing-tools`)
- **Image alt texts**: Descriptive, include keyword variations where natural
- **Schema markup recommendation**: Suggest FAQ, HowTo, or Article schema if applicable
- **Word count**: Meet or exceed the average of top 5 ranking articles

### Step 6: Quality Review

Before delivering, self-check against these criteria:

| Check | Target |
|-------|--------|
| Readability score | Flesch-Kincaid 60-70 |
| Avg sentence length | 15-20 words (with high variance) |
| Passive voice | Under 10% |
| Keyword density | 0.5-1.5% (natural, not forced) |
| Unique sections | Every H2 adds new value |
| AI pattern flags | No repetitive transitions, no hedging, no filler |
| Factual accuracy | All claims verifiable |
| CTA present | At least one, naturally placed |

## Banned Words and Phrases

Never use these in articles — they are strong AI-detection signals:

### Words
delve, utilize, leverage, facilitate, elevate, robust, seamless, cutting-edge, game-changer, revolutionize, empower, holistic, synergy, paradigm, bolster, spearhead, encompass, commencing, pivotal, intricate, multifaceted, embark, foster, realm, tapestry, landscape (when used metaphorically), unleash, harness, navigate (when not literal)

### Phrases
- "In today's [digital/modern/fast-paced] world"
- "It's important to note that"
- "In order to"
- "At the end of the day"
- "It goes without saying"
- "Without further ado"
- "Let's dive in" (as article opener — occasional use mid-article is fine)
- "You're not alone"
- "Whether you're a [beginner/expert]"
- "Look no further"
- "[X] is a powerful tool that"

## Output Format

Save the completed article as a markdown file with frontmatter:

```markdown
---
title: "Your Article Title Here"
meta_description: "Compelling meta description under 160 chars"
target_keyword: "primary keyword"
secondary_keywords: ["keyword2", "keyword3", "keyword4"]
word_count: 1850
slug: "suggested-url-slug"
date: "YYYY-MM-DD"
---

# Article Title

[Article content here]
```
