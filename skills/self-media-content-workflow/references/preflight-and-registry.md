# Preflight and content registry

## Preflight

Before writing the full draft and making assets, check only the capabilities the chosen platforms need:

| Capability | What to check | If unavailable |
|---|---|---|
| Writing | Platform module, target language, project format | Deliver a Markdown first draft |
| Images | Generation or editing tools, reference material, output folder | Deliver a visual plan and prompts |
| Raw footage or screen recordings | Footage, screen recordings, subtitles, audio and editing tools | Deliver a script, storyboard and asset list |
| Digital-human sensitive assets and platform readiness | Likeness and voice rights confirmed, third-party data-processing terms, the user's manual upload done, a digital human and voice selected, and a pronunciation list | Stay in `AWAITING_USER`; deliver the digital-human storyboard, lines, portrait requirements and a manual upload checklist |
| Video composition and subtitles | Explanatory visuals, presenter window, subtitle rendering and vertical export | Deliver the visual mapping, subtitle script, composition specs and a publishing pack that can be finished by hand |
| Animation pipeline | Voice, image generation and video composition (for example an installed animation production Skill), whether credentials are configured (check only that they exist), estimated cost | Deliver the section script, storyboard, image prompts, voice-over script and asset list |
| Music licensing | Track source (local synthesis, a platform music library, tracks the user holds a license for), license type and attribution requirements | Use local synthesis or a platform music library, or deliver a version without music |

Check the animation pipeline and music licensing only when the video production mode is animated explainer production. Check digital-human sensitive assets and platform readiness, and video composition and subtitles, only when the task card's video production mode is digital-human production; for other content types and for on-camera or footage-based tasks, mark these two as not applicable and do not stay in `AWAITING_USER` because of them.

Footage that is not in the content folder cannot be checked from here, so do not assume the user has it. For a video made from footage, list the key shots the story needs, one line each, and, unless the user has already said, ask in a message of its own which ones they have, before titles and hooks are shown. Use the answer when writing the hooks and the script. Mark each shot in the asset list as one the user has or one still missing, and deliver the list with the publishing pack.

The preflight reports only whether a capability is available; it never prints credential contents.

## Digital-human sensitive asset safety

- The user uploads, creates and selects the portrait and voice in Topview or the chosen digital-human platform themselves. This workflow never uploads on their behalf through upload credentials, file-upload or voice-cloning interfaces.
- Before uploading, confirm that the user is the person in the portrait and voice or holds explicit permission, and remind them to read the chosen platform's current terms on storage, model improvement, third-party processing, deletion and opting out.
- For sensitive assets, task cards and the content registry record only statuses: rights confirmed, terms read, manual upload done and assets selected. Index paths of deliverables such as generated clips, final videos and subtitles may go into task cards, the content registry and save checks.
- Never record original portraits, recordings, their local paths, temporary upload or download links, object storage keys, file IDs, digital-human IDs, voice IDs or any private ID that could be used to retrieve the sensitive assets again.
- Resource IDs needed at run time are used only as temporary references for the authorized operation and are not written into task cards, logs, the content registry or the repository.
- Generated digital-human clips and final videos go into the user's content folder or a delivery folder the user names, never into the public Skill source repository.

## Account and collection safety

- Publishing and data management on the user's own accounts use different permissions from competitor collection.
- Do not use the main account's login for automated competitor searches, bulk paging or comment collection.
- Competitor research is anonymous or public and read-only by default. If a login is truly needed, use a separate collection account, and get the user's consent first.
- Do not like, comment, follow, send messages or publish automatically.
- Stop at once when a CAPTCHA, rate limit, expired login or platform risk control appears.
- Never write cookies, tokens, secrets or complete credentials into task cards, logs or the repository.

## Content registry

Find the registry location in this order:

1. The location the user names.
2. The project's existing content folder.
3. `content-registry.md` in the content root folder.

Each core topic takes one row, recording the date, core topic, type, goal, platforms, task card, first draft, final copy, assets, status and publish link. The registry keeps only an index; evidence and detailed data stay in the task card.
