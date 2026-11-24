---
name: self-media-content-workflow
description: A general workflow for producing and running a creator's social media content. Use it for content creation, topic planning, trend or competitor research, adapting content for several platforms, short-video scripts, digital-human videos, animated explainer videos, publishing packs, and resuming unfinished tasks. It works out the type of request, calls the content brief, content strategy, trend and competitor research, platform copywriting and short-video modules, and manages the direction, platform, title and final-copy approvals.
---

# Self-media content workflow

## Goal

Connect account positioning, content goals, evidence, platform-native writing and visual assets into a workflow that can be picked up again at any stage. Deliver content that is credible, native to each platform and ready to act on. Do not replace real judgment with bulk generation.

## Core principles

- Confirm the account positioning, target audience, content goal and platforms before writing the body.
- Work on one core topic at a time. Versions for different platforms share facts and evidence, not one body text.
- Separate facts, personal judgments, inferences and advice. Every key number needs a source.
- Ask only questions that change the direction. Do not ask the user for information you can get from existing files or public sources.
- Save important outputs at milestones. Keep small edits in the current version; do not create a new file for every changed sentence.
- With the user, use everyday words such as "save it as a file", "finished piece" or "content library", and avoid internal terms.
- Deliver publishing packs; the user publishes. Never broadcast to several platforms at once. Any external write action needs the user's explicit permission first.
- Do not use the creator's main account login for automated competitor collection, and do not like, comment, follow or send messages automatically.
- Do not claim to detect how likely a text is to be AI-generated. Check only for templated, vague and off-voice writing.
- Follow the current project's `AGENTS.md`, folder rules and user instructions first.

## Resolve the workspace

Find the content root folder in this order:

1. The path the user names.
2. The content folder and naming rules already in the project's instructions.
3. `self-media/` in the current workspace.

Do not assume that a particular vault, account, growth plan or vendor tool exists. Save text outputs as Markdown unless the project rules or the user ask for another format.

## Request routing

Load only the modules needed for the result the user actually wants:

| Request | Modules | Result |
|---|---|---|
| A single piece or multi-platform content | `self-media-content-brief` → `self-media-platform-copywriting` | Content brief and platform-native drafts |
| Account positioning, topic pool, series, content calendar | `self-media-content-strategy` | Strategy, topic pool, series and schedule |
| Trend tracking, keyword research, competitor teardowns | `self-media-trend-radar` | Research report and original topics |
| Spoken script, storyboard, subtitles, shooting plan, digital-human video, animated explainer video | `self-media-short-video` | A short-video package ready to shoot. When the user explicitly chooses a digital human, confirms the likeness and voice rights, and has uploaded and selected the assets on the chosen platform themselves, it can go on to digital-human production and a finished video. When the user wants an animated video with no on-camera presenter and production tools are available, it goes on to animated explainer production and derives landscape and vertical versions for several platforms |

Read a module's whole `SKILL.md` before using it. If a module is not installed, run a minimal version of the stage with the same name in this Skill, and do not invent capabilities that do not exist.

## Start and resume

1. In the content root folder, look for task cards whose status is awaiting the user, writing, or awaiting approval.
2. When the user says "continue", resume the most recent unfinished task.
3. When the user only asks for self-media content creation in general and an unfinished task exists, report its current status first and ask only whether to continue it or start a new one.
4. When the user gives a clear core topic, link or material, go straight to the content brief; do not force a new topic search.
5. When the user asks only for strategy or research, take that branch and do not create unrelated drafts.

## Content creation status flow

`Clarifying needs → Awaiting direction approval → Research and evidence → Awaiting platform approval → Preflight → Awaiting title approval → Awaiting writer choice → Awaiting sample approval → Writing → Making assets → Quality review → Awaiting final-copy approval → Publishing pack delivered`

When the user writes the script themselves, "Awaiting sample approval" and "Writing" become "Awaiting the user's draft" and "Checking the user's draft".

These transitions must be made by the user:

1. Approve the creative direction.
2. Approve the platform mix.
3. Choose or edit the title and, for video, the hook.
4. Say who writes the script: the agent, or the user.
5. When the agent writes: approve the sample of the opening, or say what to change.
6. Approve the final copy.
7. Authorize any external write action.

Approving the final copy does not authorize any external write action.

At each of these points, show the user what they are deciding, stop, and wait for their reply to it. These do not count as the decision: answers to your questions, a request for changes, or a choice of only part of it (for example, the hook without the title). After a change, show the result and ask again. If something the user has already approved changes later, show the change and ask again before going on.

## Main creation flow

### 1. Write the brief and approve the direction

Call `self-media-content-brief`. Put the account positioning, target audience, content goal, core claim, evidence, tone, depth, no-go areas and platform angles on one card for approval. When information is missing, ask at most 3 high-impact questions, and let the user accept reasonable defaults. Then show the card and stop: answers to your questions do not approve it, and research starts only after the user approves or edits the card.

### 2. Add research and evidence

Call `self-media-trend-radar` when needed. Prefer the user's real experience, back-end data, original material, official documents and first-hand releases. Use competitors only to find needs, structures and openings for expression; never rewrite their content as your own.

The evidence pack contains at least:

- A one-sentence claim.
- 3 pieces of verifiable evidence.
- The boundaries between facts, judgments, inferences and advice.
- A concrete result the reader can take away.
- What cannot be said yet or cannot be proven.

The last item is a note for the creator, not text for the audience. In the content, say only what the evidence supports and leave the rest out; do not add lines that tell the audience what you could not prove.

### 3. Choose platforms and check capabilities

Read [platforms.md](references/platforms.md) and recommend one main platform and at most two extra platforms. Explain each platform's role, output and time cost.

Read [preflight-and-registry.md](references/preflight-and-registry.md). Check only the capabilities the chosen platforms need: writing, images, raw footage or screen recordings, digital-human sensitive assets and platform readiness, and video composition and subtitles. Check the animation pipeline and music licensing only when the video production mode is animated explainer production. Check digital-human sensitive assets and platform readiness, and video composition and subtitles, only when the video production mode is digital-human production; for other content types and for on-camera or footage-based tasks, mark these two as not applicable and do not go into `AWAITING_USER` because of them. When a capability is unavailable, offer a fallback such as a manual publishing pack. For the boundaries of digital-human production (rights confirmation, manual upload, third-party data processing, generation, composition and acceptance), see [digital-human-production.md](references/digital-human-production.md).

### 4. Choose the title and hook, then who writes, then the first draft

Call `self-media-platform-copywriting`, and read its `SKILL.md` before writing any title. Design the title, opening, order of evidence, structure and call to action separately for each platform; do not just shorten one text mechanically.

Generate 6 to 8 titles internally, covering entry points such as result, benefit, identity, conflict, contrast, curiosity and numbers. After screening, show the user only the strongest 3 and explain which entry point each one uses. For video, also show 3 hooks, written by the rules in `self-media-short-video`, and say which one you recommend.

Wait for the user to choose or edit the title and, for video, the hook. They are one decision: if the user settles only one, ask for the other. Until both are settled, show only the candidates and the evidence still missing: no outline with spoken lines, no script, no slide text or captions, no covers, and no changes to earlier drafts.

Once the title and hook are settled, ask who writes the script, in a message of its own, and write out both options in full, equally visible: **I write it**, first a sample of the opening and then the full draft; or **you write it**, from a short writer's brief I give you, and I check your draft. Wait for the answer before writing anything.

When you write the script, start with a sample: only the opening of the main piece, in the chosen title and hook (about the first minute of a long video, or the first few lines of a short video or a post), and stop so the user can check that it sounds right. After the user approves the sample, or after the changes they ask for, write the complete first draft around their choice, and save it.

When the user writes, give them a short writer's brief instead, and save it as its own file: the chosen title and hook; the parts in order, one line each on what the part does (with timings for video); the facts they can use, one line each with its source; and what not to say, one line each. Write it for a person, not as working notes: key points first, no research history or process notes, and nothing they do not need in order to write. Keep the full evidence pack as a separate file. When their draft arrives, check it against the evidence pack, the quality gates and each platform's rules; list each problem with a suggested fix, keep their voice and wording except where a fix needs a change, and wait for them to decide. Their checked draft then takes the place of the first draft for the rest of the flow.

### 5. Make visual or video assets

Make assets only after the title is approved. First recommend 2 to 3 styles from the visual style library of `self-media-platform-copywriting` (`references/visual-styles.md`) based on the content type, the platform and the tone in the brief, and say in one sentence how they differ. Read that file again just before you recommend styles, even if you read it earlier. Show a small sample of each, made with the user's own title or text; a description in words alone is not enough, unless nothing can be rendered here. In the same message, ask how the images will be made, and write out both options in full, equally visible: you make them here, or you write a design brief that the user takes to another AI image tool or design app. Ask again each time you show new style candidates. Wait for the user to choose. When the account already has a stable style preference, use it by default and say so. If that module is not installed, confirm the art style, palette and composition with the user directly.

Write the chosen style into the task card's visual anchor, then map the copy to visuals. For software or product content, use real interface material when it exists; otherwise use scenes or metaphors, and never invent a product interface. When the user chooses the design brief, write it instead of making the images (see `references/visual-styles.md` in `self-media-platform-copywriting`), and check the images against it when the user brings them back.

For video, call `self-media-short-video`. By default, without raw footage, deliver the script, storyboard, subtitles, cover and publishing fields. When the user explicitly chooses digital-human production, first confirm the likeness and voice rights; the user then uploads, creates and selects the digital human and voice in Topview or another chosen digital-human platform themselves. This workflow never uploads original portraits or recordings. Only after the user confirms the platform assets are ready, call an available adapter to generate the presenter clips, then compose the explanatory visuals, subtitles and presenter window, and finally check the aspect ratio, length, sound, subtitles and presenter framing for each target platform. For paid generation, follow the runtime tool's rules for confirming costs.

When the user wants a finished animated explainer with no on-camera presenter (science, history, brand stories), follow the animated explainer production guidance in `self-media-short-video`: confirm the script and facts, audition and choose a voice, and confirm the visual anchor before generating assets in bulk and rendering. Use only locally synthesized music, a platform's music library or tracks the user holds a license for, and record the attribution requirements. After the master version is finished, derive the version for each platform (YouTube 16:9 with an SRT subtitle file; Douyin, WeChat Channels and Xiaohongshu 9:16 with burned-in subtitles) and record them in the release matrix.

### 6. Quality review

Run this review after step 5. When the user wants images or video, ask for final-copy approval only after they are made, or after the design brief is written if the user chose it.

Read [quality-gates.md](references/quality-gates.md) in full and check:

1. Facts and evidence.
2. Account voice and templated writing.
3. How native each version is to its platform.
4. Consistency between title, body and visuals.
5. Compliance and commercial disclosure.
6. Completeness of the publishing pack.

For each failed item, write down the fix and the result of the recheck. After the review passes, wait for final-copy approval.

### 7. Save and deliver the publishing pack

Save milestone outputs and read them back to verify them. Report to the user only files confirmed to exist and not to be empty.

Read [publishing-pack.md](references/publishing-pack.md) in full and deliver a manual publishing pack for each chosen platform. The user publishes; never broadcast to several platforms at once.

### 8. Learn the account's style

Read [style-learning.md](references/style-learning.md). Record a single manual edit only as an observation; it becomes a stable preference only when it repeats or the user explicitly confirms it.

## Tool adaptation principles

- First find out which search, browser, image, video and document tools the current environment already provides.
- Digital-human generation, visual composition and subtitle rendering follow the same principle. Topview MCP is an optional generation adapter, used only after the user has uploaded the sensitive assets themselves and confirmed they are ready; it is not a hard dependency of the core Skills.
- Prefer official APIs, authenticated connectors or a browser the user is already signed in to.
- Do not require the user to install a particular vendor's tool for this Skill.
- When charts, tables or reports are needed, reuse the document and data capabilities the environment already has.
- Use the environment's scheduling capabilities only when the user explicitly asks for reminders.
- Never write cookies, tokens, secrets or complete credentials into task cards, logs or the repository.
- Never write original portraits, recordings, their local paths, temporary upload or download links, object storage keys or digital-human platform private IDs into task cards, logs, the content registry or the repository. Index paths of deliverables such as generated clips, final videos and subtitles are recorded as usual; resource IDs needed at run time are used only as temporary references for that operation.
- Collection tools are read-only by default. When a CAPTCHA, rate limit or platform risk control appears, stop at once and hand over to the user.
- Platforms such as Bilibili can be used as public, read-only research sources, but they become creation platforms only when the user chooses them.

## Completion status

Each time you pause or finish, report the current task, completed stages, output paths, known fallbacks and the single next action. Use these statuses:

- `AWAITING_USER`: waiting for the direction, platforms, title and hook, who writes the script, sample of the opening, the user's own draft, final copy or permission for an external write action, or for the user to upload, create and select assets on the digital-human platform themselves.
- `DONE`: every authorized step for this session is complete.
- `DONE_WITH_CONCERNS`: complete, but with clear fallbacks.
- `BLOCKED`: a key dependency failed and the work cannot continue now.
- `NEEDS_CONTEXT`: information that would change the result is missing.

## Resources

- Platform selection: [platforms.md](references/platforms.md)
- Preflight and content registry: [preflight-and-registry.md](references/preflight-and-registry.md)
- Quality review: [quality-gates.md](references/quality-gates.md)
- Publishing pack: [publishing-pack.md](references/publishing-pack.md)
- Style learning: [style-learning.md](references/style-learning.md)
- Digital-human video production: [digital-human-production.md](references/digital-human-production.md)
- Animated explainer production: [animated-explainer-production.md](../self-media-short-video/references/animated-explainer-production.md)
- Multi-platform video versions: [video-platform-versions.md](../self-media-short-video/references/video-platform-versions.md)
- Task card: [content-task-template.md](assets/content-task-template.md)
- Content registry: [content-registry-template.md](assets/content-registry-template.md)
