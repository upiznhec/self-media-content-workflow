# Changelog

All notable changes to this project will be documented in this file.

## English edition update - 2026-11-24

### Changes

- Each time image styles are suggested, write out both ways of making the images in full and equally: the agent makes them, or it writes a design brief that the user takes to another AI image tool or design app. In a test the second option was mentioned only in passing, then left out. Changed in `self-media-content-workflow`, `self-media-platform-copywriting` (`SKILL.md` and `references/visual-styles.md`), the task card template and the README.
- Spell out the approval stops, after a test where the agent went past them: answers to questions, a request for changes or a choice of only part of a decision do not count as approval; the brief is shown and approved before research; title and hook are one decision, and until both are settled only the candidates are shown (no outline with spoken lines, script, slide text or captions); the copywriting module is read before any title is written; final-copy approval comes after the images or video, or after the design brief; and approved text that changes later is shown again for approval. These make the original's approval steps explicit; the steps themselves are unchanged. Changed in `self-media-content-workflow` and `self-media-content-brief`.
- Add one step, at the user's request: after the title and hook are chosen, write only the opening of the main piece as a sample (about the first minute of a long video, or the first few lines of a short video or a post) and wait for the user to approve it, then write the complete first draft. In a test, the user caught a problem with the voice in an outline written before the draft; this workflow has no outline step, so the sample takes that place. Changed in `self-media-content-workflow`, `self-media-platform-copywriting`, `self-media-short-video`, the task card and content registry templates, and the README.
- Tighten the image rules after the same test: style samples are always shown (in words only when nothing can be rendered), and the style file is read again just before styles are suggested; suggested styles must fit the tone in the brief, adapting a preset or proposing a new style when none fits; after every change the images are looked at again, side by side, before they are called fixed, and each revision is saved under a new file name. Changed in `self-media-content-workflow`, `self-media-platform-copywriting` (`SKILL.md` and `references/visual-styles.md`) and the README.
- Add a choice, at the user's request: after the title and hook are chosen, ask in a message of its own who writes the script. If the user writes it, give a short writer's brief (the chosen title and hook, the parts in order, the facts with their sources, and what not to say), written for a person rather than as working notes; then check their draft against the evidence pack, the quality gates and each platform's rules, suggesting fixes without changing their voice. Changed in `self-media-content-workflow`, `self-media-platform-copywriting`, `self-media-short-video`, the task card and content registry templates, and the README.
- Show the content brief in the chat item by item, in the structure set out in `self-media-content-brief` (one line per item, starting with the item's name, with the defaults used filled in), and save it in the same structure. In a test, the agent showed only a short summary of the story and the platforms, so several items, such as the content goal and the core claim, were never shown for approval. The structure itself is the original's. Changed in `self-media-content-workflow` and `self-media-content-brief`.

## English edition update - 2026-11-23

### Changes

- Show 3 title candidates (and, for video, 3 hooks) and wait for the user's choice before writing the first draft. The original writes the complete first draft first and then waits for the title. Changed in `self-media-content-workflow`, `self-media-platform-copywriting`, `self-media-short-video`, the task card and content registry templates, and the README.
- When the agent can render images, show a small sample of each suggested image style, and ask who makes the images: the agent, or the user with their own design tool. If the user makes them, write a design brief for their tool and check the images against it when they come back. The original describes each style in one sentence. Changed in `self-media-content-workflow`, `self-media-platform-copywriting` (`references/visual-styles.md`), the task card template and the README.
- What the evidence pack cannot prove is a note for the creator, not text for the audience: the content says only what the evidence supports. Added to `self-media-content-workflow` and `references/quality-gates.md`, and noted in the README.
- Translation fix: 边界 (the situations a method applies to) had been translated as "limits" in three writing rules, which read as a list of weaknesses. It now reads "when it applies" or "the situations it applies to". Fixed in `self-media-short-video`, `self-media-platform-copywriting` and `references/quality-gates.md`.

## English edition - 2026-11-22

Based on the original repository, [yanhua1010/self-media-content-workflow](https://github.com/yanhua1010/self-media-content-workflow), at commit `1cdc246` (2026-11-09).

### Changes

- Translate all kept Skills, references, templates and repository files into English, keeping the method and the meaning.
- Keep `self-media-content-workflow` (trimmed to the kept modules), `self-media-content-brief`, `self-media-content-strategy`, `self-media-trend-radar` (research process and Reddit discussion discovery), `self-media-platform-copywriting` and `self-media-short-video`.
- Remove `self-media-content-analytics`, `self-media-content-delivery`, `self-media-wechat-publisher`, `self-media-video-publisher`, the workbench app, and the trend radar's overseas comparison mode with its scripts. The workflow now ends with a publishing pack, and the user publishes.
- Rewrite rules that counted Chinese characters by what they are for: on-screen text and subtitle lines are short enough to read as one line on a phone, and narration length is estimated at about 150 words a minute. Remove details that only applied to Chinese text or Chinese-speaking viewers.
- Add a note on platforms that are not covered: Instagram and Facebook (follow the Xiaohongshu method), TikTok (use the short-video Skill) and LinkedIn.

The entries below come from the original repository. Some of them describe parts that this edition removed.

## Unreleased

### Features

- Add Reddit support: `self-media-trend-radar` finds subreddits and threads worth joining, reads comments and subreddit rules (optionally through the AIsa REST API), and returns a list with a rule verdict per thread; `self-media-platform-copywriting` drafts Reddit replies and posts that follow each subreddit's rules on AI content, self-promotion and links, keep personal claims for the user to confirm, and are posted by the user, never automatically.
- Add an optional overseas comparison mode to `self-media-trend-radar`: a dependency-free Python script that searches X, YouTube and Reddit against Xiaohongshu, Douyin and Bilibili through the AIsa REST API, scores each side's recent engagement on a log scale, and writes a Markdown report, with free cost quotes, a per-run budget cap enforced by the gateway, and offline replay of saved responses.
- Add a source-checked social-auto-upload adapter and Node publish script for per-platform video packs, with dry-run planning, confirmation, private/draft defaults, and post-upload records.
- Add explainer narrative and style guidance distilled from high-performing text-led science explainers: second-person or motif hooks, a central question within 15 seconds, an early title card, visible progress devices, an emotional peak with a concrete person, callback endings, one-idea-per-line writing rules, family visual style, visual route choice (procedural motion graphics, illustration, or mixed), slow ambient score selection, and an optional subtitle-only (no voice) format.
- Add an optional, provider-neutral animated-explainer production path for narrated videos without on-camera presenters: story beats, synthetic voice selection, visual anchor, composition, licensed-music mixing with ducking, loudness checks, and fallbacks.
- Add multi-platform video versioning: one master, derived landscape/vertical versions (native re-layout or wrapped vertical with hook title and burned-in captions), SRT captions, per-platform covers, safe areas, music attribution, and AI-labeling fields, plus a release-matrix template.
- Add YouTube platform copywriting guidance (titles, thumbnails, descriptions with chapters, tags, captions, audience and synthetic-content settings) and add YouTube to platform selection and delivery checklists.
- Add `self-media-video-publisher`: per-platform publish packs and tiered publishing (manual pack, form-fill helper, private/draft upload, scheduled) with per-platform authorization, adapter discovery (official YouTube Data API, form-fill extensions, browser-automation uploaders), and credential boundaries.
- Add an optional, provider-neutral digital-human video production path with likeness/voice rights checks, user-managed sensitive-asset uploads, third-party data-processing review, presenter generation, visual composition, captions, 9:16 checks, quality gates, and privacy-safe delivery metadata.

## 0.1.0 - 2026-07-22

### Features

- Add a nine-Skill suite covering briefs, strategy, trend research, platform copywriting, short video, analytics, delivery, and WeChat draft publishing, orchestrated by `self-media-content-workflow`.
- Add reusable templates for account profiles, topic pools, calendars, storyboards, metrics, reviews, registries, and task state.
- Add a visual style library with eight image-style presets and a recommend-and-choose step before asset generation.
- Add tool-agnostic publishing, research, credential, and account-safety boundaries.
- Distribute through the standard `npx skills` CLI, with a repository validator, documentation, and continuous integration.
