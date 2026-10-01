# AGENTS.md

This repository is a Marp slide deck. Treat it as a communication artifact first and a Markdown project second. The goal is not merely to make slides render; the goal is to preserve and improve a talk that has an argument, an audience, a rhythm, and evidence.

These instructions are intentionally reusable across Marp-based slide projects. Do not overfit changes to the current deck unless the user explicitly asks for deck-specific work.

## Working Model

Approach each deck like a concise research presentation:

- Identify the central thesis before editing individual slides.
- Understand the audience, their prior knowledge, and what should change in their mind after the talk.
- Preserve the line of reasoning: motivation, context, evidence, interpretation, implication, and closure.
- Treat each slide as one move in an argument, not as an isolated Markdown fragment.
- Prefer clarity, sequence, and visual economy over decorative complexity.
- Distinguish claims, evidence, examples, and citations.

When the deck is about an organization, community, product, research topic, or historical narrative, avoid flattening it into a timeline. A good deck explains why events matter, what changed, and what the audience should infer.

## Editing Principles

- Keep edits scoped to the user request and the deck's existing style.
- Do not rewrite the author's voice unless the request is explicitly about tone, structure, or narrative.
- Improve slide flow by reducing ambiguity, strengthening transitions, and removing accidental redundancy.
- Prefer one strong idea per slide. If a slide carries multiple claims, split it or make the hierarchy explicit.
- Avoid turning slides into prose documents. Keep slide text sparse and concrete.
- Do not add speaker notes, scripts, rehearsal schedules, or fallback plans to this deck. Keep HTML comments limited to Marp directives.
- Public slides must stand on their own. Source lines should contain citations and attribution, not references to prior discussions, invitation drafts, or editing decisions. Prefer concrete cues, operations, and checkpoints to explanatory reminders; consolidate necessary data assumptions where they affect interpretation instead of repeating caveats across the deck.
- Preserve intentional pacing slides, title-only slides, full-bleed image slides, and pause slides unless they clearly break the requested goal.
- Keep terminology consistent across the deck, especially names, dates, roles, project titles, and recurring concepts.
- When adding factual claims, verify them from reliable sources or mark assumptions clearly for the user.
- When editing dates, statistics, event names, or attributions, prefer exactness over rhetorical convenience.

## Narrative And Argument Quality

Use the same standards expected in strong academic and technical talks:

- Every major claim should have a visible basis: data, example, source, lived evidence, or a clear warrant.
- The deck should make scope conditions clear. Avoid universal claims when the evidence is local, historical, or anecdotal.
- Avoid unexplained jumps between abstraction levels. If moving from a concrete example to a general principle, make the bridge legible.
- Introduce specialized terms before relying on them.
- Keep the audience's cognitive load low: one conceptual shift at a time, clear grouping, and minimal competing visual signals.
- Use contrast deliberately: before/after, problem/response, myth/reality, principle/example, local/global.
- End sections with synthesis, not just the next topic.

If a requested edit weakens the argument, explain the tradeoff briefly and propose a sharper alternative before making broad structural changes.

## Marp Conventions

- Run commands from the repository root. Use repository-relative paths and public references; these instructions must not depend on a contributor's home directory, private configuration, or external agent instruction files.
- The primary source is usually `slide.md`. Edit the source and regenerate `index.html` with the existing build command; do not hand-edit generated HTML.
- Keep YAML front matter valid and minimal. Do not add project-specific metadata unless it serves the deck or publishing workflow.
- Use `---` for slide boundaries. Preserve Marp directives and slide-local classes unless changing them is part of the task.
- Prefer Marp-native image syntax for simple slides and HTML only when Marp syntax cannot express the layout cleanly.
- Keep custom CSS small, purposeful, and close to the deck's established visual system.
- Do not introduce a build system, package manager, theme framework, or asset pipeline unless the repository already uses one or the user asks for it.
- If scripts exist, prefer existing scripts over new commands. If no scripts exist, use the simplest Marp-compatible validation available in the environment.

## Denny's Recurring Slides

Preserve these parts of the deck when editing or restructuring it:

- Opening order: cover, slide-link page, speaker introduction, then the talk.
- Use `Denny Huang` as the public speaker name, including cover text and author metadata.
- The slide-link page must show both a QR Code and a readable, clickable URL. Use `https://denny.one/<project-directory>/` as the publishing path unless the user supplies another URL. Keep the QR payload, visible link target, and front-matter `url` identical; do not invent a short link.
- Store the QR Code locally, with a white quiet zone and high contrast. Check the rendered size and decode it when a scanner is available. Avoid a runtime dependency on a remote QR service.
- Preserve the speaker introduction already in the deck. If the author supplies a replacement introduction or reference deck, keep its original Markdown bullet list, wording, and personal links. Typography and spacing may be adjusted for readability without changing that list. Do not regroup it into categories or cards, translate its wording, or invent credentials unless the user explicitly requests that change.
- Close the main talk with `Thanks for listening`, the usual CC BY-SA 4.0 notice, and the Marp logo and link. Optional reference appendices may follow this closing page without becoming part of the live talk.
- Apply the slide license to original slide content. Keep third-party media under their original rights and attribution; the closing notice must not silently relicense them.
- Carry these pages and their assets into `slide.md`, not only into a README or preview. Use the deck's current visual style rather than importing the previous event's branding.
- Treat visual consistency as a shared visual grammar, not identical coordinates on every slide. Use the approved palette, fonts, recurring cues, and footer as anchors; adapt alignment, columns, type scale, and spacing to the slide's purpose and content density. Make routine layout adjustments within that visual system directly, and verify how the pages read beside their neighbors and in the whole deck.

## Visual And Media Standards

- Visuals should carry meaning, not merely decorate.
- Maintain image aspect ratios unless cropping is intentional.
- For full-bleed images, verify that the important subject is not hidden by slide text, pagination, or viewport cropping.
- Prefer stable local assets in the repository for repeatable builds.
- When adding external media embeds, consider offline behavior, privacy, accessibility, and whether the deck still communicates when the embed fails.
- Keep image filenames descriptive and durable.
- Preserve license and attribution information for reused assets.

## Language And Tone

- Match the deck's language. If the deck is in Traditional Chinese, keep user-facing slide text in Traditional Chinese unless asked otherwise.
- This instruction file is in English because it is primarily for coding agents.
- Keep slide copy concise, concrete, and speakable.
- Avoid generic marketing phrasing, inflated claims, and filler.
- Prefer active, direct phrasing when it improves comprehension.
- Preserve culturally specific terms, community names, and proper nouns carefully.

## Accessibility And Presentation Quality

- Ensure headings are readable from a distance.
- Avoid dense lists unless the slide is meant to be scanned as a reference.
- Watch for long lines, cramped text, low contrast, and overlapping elements.
- Use visual hierarchy consistently: title, subtitle, evidence, source, and aside should not compete equally.
- When possible, make links human-readable and preserve target URLs.
- Do not rely on color alone to communicate meaning.

## Verification

Before finishing a change:

- Review the diff for unintended generated-file churn.
- Check that Markdown, front matter, slide separators, HTML tags, and Marp directives remain well formed.
- If a Marp build or preview command exists, run it.
- If no build command exists, at least inspect the edited source around every changed slide.
- For visual/layout changes, prefer rendering or previewing the deck when the environment supports it.
- Report any validation you could not run and why.

## Collaboration With The User

- For small textual or structural fixes, make the change directly.
- For broad narrative restructuring, first state the proposed structure and the reasoning.
- For factual additions, cite or summarize the evidence path used.
- If the user's request is ambiguous, infer conservatively from the deck and existing style. Ask only when the choice changes the talk's thesis, audience, or publishing workflow.
- Keep final reports short: what changed, where, and how it was checked.

## Denny's slide voice

Write slide bodies as live cues, not documentation.

Each slide should first show the thing the audience needs to locate, type, compare, or check. Denny can explain why live.

Use the style anchors below as the default reference for Denny's slide rhythm. If prior Denny decks are available in the working context and the task is a substantial style rewrite, sample a few before editing. Use them to refine rhythm and density, not to copy old topics.

### Slide Body Grammar

Core transform:

`README prose -> cue / artifact / command / contrast / expected output / 檢核點`

Evidence before explanation:

Start with a concrete artifact: screenshot, URL, demo state, path, command, prompt, case, data point, diagram, expected screen, expected output, or `檢核點`. Use `### 重點` or an equivalent summary cue only after the artifact or demo target is visible.

Sparse does not mean under-specified:

Public talks can use title-only beats. Workshops and courses still need enough state to follow the room: UI path, file path, command, expected result, recovery cue, or `檢核點`.

Every slide should have one visible anchor that tells the audience where they are. One anchor may be a pair: Before / After, Input / Output, You / Agent, Git / GitHub.

### Micro-Style

- Title shapes: `Survey`, `DEMO`, `Practice`, `檢核點`, `需求確認`, `除錯`, a URL, a file path, or a command.
- Question titles: `是否寫過程式？`, `Shell 熟悉程度`, `這個 diff 改了什麼？`
- Contrast titles: `Git / GitHub`, `Public / Private`, `Before / After`, `Input / Output`.
- Chinese / English mixing: Chinese for room cues; English for product names, commands, file paths, repo names, and terms people actually say.
- Body shape: 0-4 bullets, command block, screenshot, URL, repo path, prompt block, expected output, or small checklist.
- Failure cues: `總有意外`, `噢！`, `格式對，內容錯`.

### Rewrite Examples

- `建立可追蹤且具備責任分工的協作流程` -> `誰？改了什麼？`
- `讓學員理解 Markdown 到 JSON 的資料轉換流程` -> `Markdown -> JSON`
- `避免團隊協作時產生檔案衝突` -> `notes/<github>.md` + `不要共用同一個檔案`
- `透過本機預覽確認資料是否正確呈現` -> `pnpm run dev` + `看到自己的卡片`

Avoid:

- Turning each slide into a mini article.
- Marketing tone, motivational filler, or polished documentation voice.
- Over-translating domain-native terms such as `commit`, `diff`, `repo`, `schema`, `prompt`, or `Agent`.
- Explaining away all of the whitespace and timing.
- Replacing a concrete artifact with abstract summary.
- Adding text just because the idea feels important.
- Definition-first slides when a prompt, artifact, demo, or checkpoint would work.
- Objective-summary titles like `建立...`, `說明...`, `提升...`, `確保...`.
- Sentences that start with `透過...來...` but show no artifact, command, or decision.

Revision order:

1. Delete.
2. Shorten.
3. Replace with words Denny would say live.
4. Turn explanation into a cue, command, contrast, expected output, or checkpoint.
5. Add explanation only when the audience would be blocked without it.

Agent check:

- Is this a slide cue, or README prose?
- Does this work as a live cue, not documentation?
- Does the audience need to see this now, or can it be spoken live?
- Can this become one cue, one example, one operation path, or one expected output?
- Is there a visible anchor the audience can use to know where they are?
- For collaboration slides, is the human/tool boundary visible?

## Current Deck: 20261002-gis

- The approved visual system is `theme/civic-atlas.css`: white backgrounds, pastel cards, dark text, CJK typography, recurring pixel cues, and a shared footer. Left alignment is the usual reading anchor; adjust composition and type hierarchy when the page's purpose and content require it. Content layouts with an eyebrow share one h1 top margin; do not introduce separate title offsets per layout. Keep the intentional cover and closing compositions. The slide-link page supports both scanning and typing, the introduction preserves its original bullet list, and the thanks page provides a clear close with readable credits. Reserve dark slides for a small number of key messages. Do not restore the removed `<mark>` highlighting.
- `slide.md` is the complete presentation source, including A01-A07 reference appendices. `index.html` is the generated, publishable deck. `img/` contains the cover crop, local QR Code, historical screenshots, and reused CC BY-SA and Marp graphics.
- `.marprc.yml` enables HTML, loads the theme, and permits local assets; `.vscode/settings.json` uses the same theme. Keep those settings consistent. The deck's public URL is `https://denny.one/20261002-gis/`.
- HTML is the deliverable. Use the existing `build` and `watch` scripts, or the equivalent pnpm commands. Install the dependencies declared in `package.json` when needed; do not add another build workflow. Create PDF output only when the user explicitly asks for it.
- `gh-pages` is both the primary branch and the publishing branch. GitHub Pages publishes from `gh-pages` at `/ (root)`. Track `index.html`, `img/`, source, theme, shared editor settings, and `.nojekyll`; ignore dependencies, generated previews, and local agent state. Rebuild the HTML before a publishing commit. Do not add a separate deployment branch or workflow unless requested.
- This is a 30-minute introduction for university students who may have no computing background. Use Taiwan Traditional Chinese for slide text and retain technical product names. Teach open geodata, disaster-related applications, data interpretation, and the handoff to service design.
- The main exercise uses New Taipei City's important-landmark dataset, with AI assisting preparation and coordinate conversion for uMap and a My Maps format comparison. Do not add MCP, website development, or another complex workflow without a user request.
- Synchronize demo instructions with the companion repository, [ntpc-multiformat-demo-kit](https://github.com/denny0223/ntpc-multiformat-demo-kit). Its `README.md` is the operation entry point; `demo/` has six files, `data/raw/` retains the complete original CSV and source/CRS approvals, and inventory, anomalies, and checks are reported directly. Do not restore separate audit reports or full-data conversion outputs. The current example has 30 Banqiao records, five in each of six original categories. These paths refer to the companion repository, which is not needed to build this slide deck.
- The current demo uses an explicitly approved EPSG:3826 teaching assumption; the source CRS remains unverified. Label the assumption once on the coordinate slide. Use the companion repository's `SOURCE.md` and `data/raw/crs.json` for the detailed status and approval; do not imply program checks prove platform imports, style rendering, or real-site accuracy.
- The landmark dataset includes a shelter category. A recorded location does not establish current opening, availability, or safety. Teach that distinction through concrete questions about location, current conditions, and user needs rather than repeated disclaimers.
- GeoJSON coordinates are longitude first, latitude second. Confirm the source CRS, projection zone, units, and axis order rather than inferring them from field names. Label computed teaching coordinates as examples, not actual dataset records.
- Preserve source attribution and evidence for factual claims. Describe demo verification according to the companion repository's documented results. Reference appendices are for further reading rather than extra lecture time.
- Do not bundle fonts. `img/invitation-crop.jpg` remains the original rights holder's artwork. Do not add official organizer logos or imply endorsement.
- After layout changes, render and inspect every slide, including CJK wrapping, QR readability, card text, source citations, footer, and pagination. Evaluate balance, hierarchy, and continuity with neighboring slides as well as clipping and overlaps. Use temporary screenshots for QA; do not leave unrequested export files in the project. Successful commands and geometry checks alone do not establish visual fit.

From the repository root:

```sh
npm install     # Only when project dependencies are not installed.
npm run build   # Regenerate index.html.
npm run watch   # Rebuild while editing.
```

The publishable deck consists of `index.html` and `img/`; keep `.nojekyll` at the repository root. Open `index.html` in a browser to review the generated deck. Update the source and rebuild whenever image paths or slide content change.
