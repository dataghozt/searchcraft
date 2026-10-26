# SearchCraft

**SearchCraft is a Claude Skill for research-first SEO, GEO, AEO, semantic SEO, and Google AI Overviews content workflows.**

It helps Claude plan, research, write, audit, and improve content using available search and research tools. Its workflow focuses on search intent, related queries and user questions, SERP review, evidence verification, natural writing, and useful content—not keyword stuffing or fabricated metrics.

## What it does

- Researches a topic using web/search tools available in the current Claude environment
- Maps search intent and related subtopics
- Identifies related queries and user questions when those sources are accessible
- Reviews competing search results and content gaps
- Plans keyword clusters and content briefs
- Produces natural, evidence-based articles and landing-page copy
- Improves content for SEO, GEO, AEO, semantic search, and AI-assisted search experiences
- Suggests metadata, internal links, FAQs, and structured data when relevant
- Audits existing content for intent gaps, clarity, duplication, unsupported claims, and readability
- Avoids invented search volumes, ranking data, citations, and product claims

## Important limitation

SearchCraft is an **instructional skill**, not a standalone crawler, keyword database, Google API, or browser. It does not automatically grant Claude access to Google Search, Google Autocomplete, People Also Ask, Google Search Console, paid SEO platforms, or any other external service.

Research depth depends on the tools, integrations, permissions, and source material available in your Claude setup. If live research or a metric is unavailable, the skill instructs Claude to say so rather than fabricate it.

## Repository structure

```text
searchcraft/
├── SKILL.md
├── README.md
├── LICENSE
├── .gitignore
└── examples/
    └── EXAMPLE_PROMPTS.md
```

## Install in Claude

Claude's interface can change over time, so labels may vary.

1. Download the `searchcraft-claude-skill.zip` package.
2. Open Claude and navigate to **Customize → Skills** (or the current Skills management area).
3. Choose the option to upload or add a skill.
4. Upload the ZIP file and follow Claude's prompts.
5. Enable the SearchCraft skill if Claude asks you to enable it.

If your Claude plan or workspace does not expose Skills, check the current Anthropic documentation and account availability.

## Install in Claude Code

For a personal skill, place the skill directory in your Claude Code skills folder:

```text
~/.claude/skills/searchcraft/SKILL.md
```

For a project-specific skill, place it in:

```text
.claude/skills/searchcraft/SKILL.md
```

The directory must contain `SKILL.md`. You can also keep the README, examples, and license alongside it for project maintenance.

## Example prompts

- “Research this topic using the available live search tools, map the search intent, identify unanswered questions, and create an evidence-based article brief.”
- “Cluster these keywords by search intent and recommend which page should target each cluster. Do not invent search-volume data.”
- “Audit this article for SEO, GEO, AEO, and Google AI Overviews readiness. Preserve the existing facts and flag anything that needs verification.”
- “Create a natural, publish-ready article for this audience. Research claims first, answer the main question near the beginning, and avoid filler.”
- “Review the competing results available to you and identify reader-focused content gaps without copying competitors.”

More prompts are available in [`examples/EXAMPLE_PROMPTS.md`](examples/EXAMPLE_PROMPTS.md).

## Design principles

1. Research before drafting when research is required.
2. Match content to search intent.
3. Verify important claims.
4. Write for people first.
5. Make content clear to both readers and search systems.
6. Be transparent about tool and data limitations.
7. Never promise rankings or AI citations.

## Contributing

Issues and pull requests are welcome. Keep improvements practical, evidence-aware, and compatible with Claude Skills. Do not add instructions that encourage fabricated metrics, citations, or search findings.

## License

MIT. See [`LICENSE`](LICENSE).
