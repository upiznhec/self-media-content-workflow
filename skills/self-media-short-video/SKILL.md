---
name: self-media-short-video
description: Turns an approved core topic or copy into a video plan that can be shot, screen-recorded or handed to video tools. It also supports making digital-human videos after the user confirms the likeness and voice rights and finishes the manual upload on the platform, and making animated explainer videos with no on-camera presenter (science, history, brand stories) with a synthetic voice and AI-drawn visuals. Use it for spoken scripts, the first 3-second hook, storyboards, subtitles, screen-recording checklists, covers, hashtags, music and licensing, digital-human or animated production packs, landscape and vertical versions for several platforms, and publishing copy for WeChat Channels, Douyin, Xiaohongshu video, YouTube landscape videos and Shorts.
---

# Short video and video production

## Principles

- One video makes only one core claim.
- The first 3 seconds give a conflict, result, benefit or concrete scene. Prefer the second person ("you...") or a motif line that can recur, to draw viewers in.
- Subtitles must work without sound: with the sound off, the subtitles alone are enough to follow the video.
- The spoken script must be easy to say aloud; do not cut a long article into subtitles.
- Visuals prove, demonstrate, compare or carry emotion; they do not repeat the subtitles.
- Prefer a real person's voice, product screen recordings and real evidence; do not default to a digital human or animation.
- The digital human is a production mode used only after the user chooses it, and it requires rights to the portrait and voice. The user personally uploads, creates and selects the sensitive assets on the chosen digital-human platform, and keeps the human preview and publishing confirmation.

## Confirm the inputs

Check the target platform, audience, content goal, length, how the creator appears on camera, available assets, core claim, call to action and what must not be shown. If information that would change the plan is missing, ask at most 3 questions.

## Video production modes

- `Plan mode`: when there is no raw footage, no confirmation that the digital-human platform assets are ready, or no clear permission to make a finished video, deliver a plan that can be shot, and do not make a finished video on your own.
- `Live-action editing mode`: when the user provides raw footage and explicitly asks for editing, use the video, subtitle and audio capabilities available in the current environment.
- `Digital-human production mode`: when the user explicitly chooses a digital human, confirms the likeness and voice rights, and has uploaded, created and selected the digital human and voice on the chosen platform themselves, generate the digital-human presenter clips following [digital-human-production.md](references/digital-human-production.md), then complete the explanatory visuals, subtitles, presenter window and the vertical final video.
- `Animated explainer production mode`: when the user explicitly wants a finished animated video with no on-camera presenter, and voice, image and video composition capabilities are found at run time, follow [animated-explainer-production.md](references/animated-explainer-production.md) and [explainer-narrative.md](references/explainer-narrative.md) to build the narrative skeleton, synthetic voice-over, visual assets, shot composition, music licensing and mixing, and produce the master version first.

In animated explainer mode, tools are also found at run time: an installed animation production Skill, an editing software project template or a video tool the user names. The core process does not hard-code any image or voice service. Before paid generation, tell the user the estimated cost.

In digital-human mode, the generation tool is found at run time. If the current environment provides Topview MCP, it can be used as the adapter for generating digital-human clips after the user confirms that the digital human and voice in Topview are ready. This Skill does not use upload credentials or cloning interfaces in place of the user uploading the original portrait and recording. The core process does not hard-code a vendor API. When generation or composition is unavailable, fall back to a digital-human storyboard, visual mapping, subtitle script, asset list and a publishing pack that can be finished by hand.

## Versions for several platforms

When the finished video goes to several platforms, first decide the master version (YouTube is usually 16:9; vertical platforms are usually 9:16), then derive the other versions following [video-platform-versions.md](references/video-platform-versions.md): landscape to vertical (a native re-layout or a vertical wrapper around the landscape video), burned-in subtitles or SRT, a cover for each platform, AI labels and music attribution. Use [video-release-matrix-template.md](assets/video-release-matrix-template.md) to record each version and its publishing fields.

## Structure

Choose one main structure:

- Problem → method → example.
- Result → process → lesson.
- Conflict → choice → consequence.
- Demonstration → explanation → when it applies.

End with one thing to remember and one main call to action.

## Storyboard

Use [storyboard-template.md](assets/storyboard-template.md). For each shot, write:

- Time and length.
- Shot size, picture, the person's action or the screen-recording operation.
- Spoken lines, subtitles and on-screen text.
- Evidence, B-roll, sound effects, background music and transitions.

The shot lengths must add up to the target length. The facts in the subtitles and the spoken lines must agree.

## Output package

Deliver:

1. 3 hooks and the recommended one. If the user has not chosen a hook yet, show them before writing the script and wait for the choice. Write the script with the chosen hook: first only the opening, as a sample (about the first minute of a long video, or the first few lines of a short one), and wait for the user to approve it before writing the rest.
2. The full spoken script.
3. A storyboard or screen-recording checklist.
4. The subtitle script.
5. The cover title and a description of the cover picture.
6. The publishing title, body, hashtags and background music suggestions.
7. Gaps in shooting or assets.

Digital-human production mode also delivers the likeness and voice rights confirmation, the status of the platform manual upload and asset readiness, generated digital-human clips, specs for the explanatory visuals and presenter window, subtitle files or subtitle text, the pronunciation list, technical specs of the final video, AI or digital-human disclosure requirements and acceptance results. The delivery pack does not include the original portrait, recordings or platform private IDs.

Animated explainer production mode also delivers the master version and the version for each platform, subtitle files, a cover for each platform, music license and attribution text, the pronunciation list, a list of fact sources, technical specs such as loudness and aspect ratio, the production project folder and the rebuild command.

When publishing on several platforms, deliver the release matrix. The user uploads and publishes on each platform; this English edition has no video publishing module.

When the user has provided no raw footage, stop at a plan that can be shot by default. But when the user explicitly chooses digital-human production, completes the rights confirmation, and confirms that the digital human and voice have been uploaded and selected on the chosen platform by hand, you may go on to find and call the digital-human, video, subtitle and audio tools in the current environment.
