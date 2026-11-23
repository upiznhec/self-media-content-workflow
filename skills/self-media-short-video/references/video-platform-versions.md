# Multi-platform video versions

When one video goes to YouTube, Douyin, WeChat Channels and Xiaohongshu, the facts, spoken script and mixed audio are shared, while the aspect ratio, subtitles, cover, title and publishing fields are redone for each platform. This file sets out how to derive each platform's version from one master version.

## Version matrix

Decide the master version first, then list the derived versions. You can record them with [video-release-matrix-template.md](../assets/video-release-matrix-template.md).

| Platform | Usual aspect ratio | Subtitles | Cover | Notes |
|---|---|---|---|---|
| YouTube long video | 16:9 | Upload a subtitle file (SRT); subtitles need not be burned into the picture | Custom 16:9 thumbnail | Both search and recommendation depend on the title, description, chapters and thumbnail |
| YouTube Shorts | 9:16 | Burned-in subtitles | A frame chosen from the video | Use only when posting a short vertical version |
| Douyin | 9:16 preferred | Burned-in subtitles | Vertical cover; the first second should already work as a cover | Landscape can be posted too, but vertical usually fills more of the screen and does better |
| WeChat Channels | 9:16 or 16:9 | Burned-in subtitles | Vertical or landscape cover | Often shared inside WeChat, so a full landscape version also works |
| Xiaohongshu video | 9:16 or 3:4 | Burned-in subtitles | 3:4 cover with a large-type title | The cover decides clicks in the feed; the title leans toward search terms |

Exact resolutions, length limits, file sizes and cover sizes follow the platform's publishing screen and official guidance at the time of publishing.

## Two ways to turn landscape into vertical

### A. Native vertical re-layout (best result)

Create a 9:16 frame in the production project: rearrange the shots, the subject's position and the on-screen text, and render again. This suits accounts whose main audience is on vertical platforms; the cost is a full re-layout and render.

### B. Vertical wrapper around the landscape video (fastest)

Keep the mixed landscape video and place it in the middle of the vertical frame, fill the background with a blurred, enlarged copy of the same picture, and add a hook title above and large subtitles below. This suits cases where landscape is the master version and vertical platforms are extras.

- The hook title states the conflict or contrast in one sentence, in no more than 2 lines, and stays on screen for the whole video.
- The subtitles must be much larger than in the landscape version, placed in the lower part of the frame, above the platform's button area.
- The channel name and attribution at the end are usually unreadable in the shrunken landscape picture; enlarge a separate copy for the vertical version.
- In environments that cannot render text (for example, ffmpeg without its font module), overlay the text with the production pipeline or editing software; never deliver a vertical version without subtitles.

## Safe areas

Vertical platforms lay their interface over the picture: the status bar and search at the top, the title, description and progress bar at the bottom, and the like, comment and share buttons on the right. Put hook titles, subtitles and key numbers in the safe band in the middle, not in the bottom 20% or so or in the button column on the right. Platform interfaces change, so preview on a phone after exporting.

## Subtitles

- Base the subtitles on the final voice-over. Cut them at punctuation into short lines that fit on one line on a phone, timed to the real pauses in the voice-over.
- For subtitle-led videos, burn large subtitles into the master version and share them across all platform versions; for YouTube, also upload an SRT file for search and translation.
- Chinese platforms take burned-in subtitles. YouTube takes an uploaded SRT file, which can be searched and automatically translated, and which deaf and hard-of-hearing viewers can also use.
- Names and numbers are written the same way in the subtitles, the spoken script and the on-screen text.

## Covers

- YouTube: a 16:9 thumbnail with a large subject and little text, short enough to read at a glance on a small thumbnail, or none. It complements the title instead of repeating it.
- Douyin and WeChat Channels: a vertical cover frame with a large-type hook; keep the same layout within a collection.
- Xiaohongshu: a 3:4 cover. The large-type title is key to clicks; it can differ from the publishing title but must not contradict it.

## Music and copyright

- Derived versions reuse the master version's audio track; do not change the music for each platform.
- Chinese platforms detect copyrighted music from outside the platform. When using externally licensed tracks such as CC BY, write the attribution in the description. If the track is detected or muted, re-score the video with the platform's music library, or keep a version without music.
- If YouTube raises a copyright claim (Content ID), dispute it with the license and attribution; do not change the speed or add noise to dodge detection.

## AI labels

- For content with AI-generated visuals or a synthetic voice, declare it truthfully with the "AI-generated" or "synthetic content" option in the platform's publishing screen. China's rules on labeling AI-generated synthetic content (人工智能生成合成内容标识办法) have been in force since September 1, 2025, and require AI-generated synthetic content to be labeled.
- YouTube's "altered or synthetic content" declaration mainly targets content realistic enough to be mistaken for real. An obviously illustrated or animated style usually does not need the box ticked, but saying "visuals drawn with AI" in the description is more transparent to viewers.
- Platform rules change; at publishing time, follow the prompts in the screen, and record the result in the task card.

## Technical checks

After exporting each version, check and record:

- The length matches the master version (or the plan for a short cut).
- Resolution and aspect ratio are correct, and the first and last frames look right.
- There is an audio track, and its average loudness and peak match the master version.
- Subtitles appear throughout, are not covered and have no typos; the end attribution is readable.
- The file plays normally on a phone.
