# Animated explainer production

This guidance is an optional production branch of `self-media-short-video`, for animated videos with **no on-camera presenter** on science, history, brand stories, knowledge explainers and similar topics. A synthetic voice tells the story, AI-drawn or licensed assets make up the picture, and the production pipeline composes the shots, subtitles, data labels and music. It describes inputs, approvals, production, acceptance and fallbacks, and is not tied to any one image, voice or animation tool.

## Entry conditions

Enter animated explainer production mode only when all of these hold:

- The user explicitly wants a finished video, not just a script or storyboard.
- The core topic, target platforms, aspect ratio of the master version, target length and main call to action are approved.
- Usable voice, image and video composition capabilities have been found at run time: for example an installed animation production Skill (a cinematic explainer pipeline based on Remotion, three.js and the like), an editing software project template, or a video tool the user names.
- When paid generation is involved (image, voice or rendering services), the estimated cost has been explained to the user according to the runtime tool's rules, and the user has agreed.

If any condition is not met, return to plan mode and deliver the script, storyboard, image prompts and asset list.

## Production process

### 1. Narrative skeleton

- First build the structure following [explainer-narrative.md](explainer-narrative.md): a second-person hook or motif line, the central question within 15 seconds, a title card, a progress device, an emotional peak, a callback to the opening and an open ending. Rewrite sections that list years without moving the question forward.
- Split the script into 8 to 12 sections. For each section, write the progress marker (such as a value or a year), the visual job, the spoken facts and the on-screen text.
- Choose one narrative viewpoint for the whole video (a fictional narrator, a voice-over or an object) and one line of progress (time, depth, distance, price and so on).
- Give a conflict or contrast in the first 3 seconds; at the end, arrange a reveal or callback, followed by the title and channel name.
- Mark the source of each key fact and write it into the task card's evidence pack. Animation is visually persuasive, so a factual error costs more than in an image post.

### 2. Voice-over

- When using a synthetic voice, pick 2 to 3 candidates from the voice library available at run time for the user to listen to. Once the user chooses, write the voice into the account's style profile and keep using it.
- Do not clone other people's voices. When cloning the user's own voice, follow the rights and sensitive-asset rules in [digital-human-production.md](digital-human-production.md).
- Estimate the length at about 150 words a minute (2.5 words a second). Write numbers, years and names in the script the way they should be read aloud, and keep a pronunciation list. When the video is made, listen to each name; if one is misread, change the script or the list and regenerate that line.

### 3. Visual assets

- First choose a visual route: procedural motion graphics (particles, line drawings, charts, counters; good for abstract mechanisms and data), illustrated scenes (AI-drawn; good for people, history and physical objects), or a mix of both. Keep one family style within a series: one background color, one warm main color and one cool accent.
- Set the visual anchor first (art style, palette, lighting, composition), write it into the task card, and use the same style suffix for every asset in the video.
- For car models, buildings and people that really exist, describe their appearance from public sources. Do not generate recognizable trademarks, brand logos or text in the picture, to avoid trademark problems and typos in AI-generated text.
- Do not generate realistic portraits of real historical figures that pass as photos. When a narrator is needed, use a fictional character, or give the figure a clearly illustrated style.
- After generating, look at the overview sheet first, and check orientation, empty space, style consistency and factual errors in appearance before moving on to composition.

### 4. Composition and shots

- The main picture carries proof and emotion: camera moves that push forward, settings that change with each section, important objects entering and leaving, and impact or pauses at key moments.
- Subtitles lead: the master version has large burned-in subtitles line by line, with 1 to 2 key words per line in the accent color, so the whole video can be understood with the sound off. Progress markers, section titles and key numbers form a second layer of information beyond the subtitles.
- Put the title card after the hook and the central question (about 15 to 20 seconds in).
- Show key numbers with rolling counters, progress bars or comparison animations, with the source in small text next to them.
- Arrange a clear visual event every 20 to 30 seconds, so the video does not feel like a slideshow.
- Before rendering the whole video, take still frames from each section and check for missing assets or black blocks, overflowing or covered text, labels out of bounds, and the narrator's alignment.

### 5. Music and sound effects

- Direction for choosing music: a slow (about 55 to 70 BPM), minor-key ambient track with a low-frequency bed and steady loudness throughout, so it does not compete with the text or the narration. A series can keep one track or one set of tracks as its sound identity.
- Use only three kinds of source: music synthesized locally by the tool, a platform's music library, and tracks the user holds a license for. Record the track title, artist, license type and attribution requirements.
- For attribution licenses (such as CC BY), write the attribution in the video description; adding a line of attribution at the end of the video is safer.
- Lower the music when narration comes in (sidechain compression or a manual envelope), and lower it further under key lines; try to align the final chord with the fade to black or the title.
- A constant low-frequency bed, engine noise and repeated alert sounds are easily heard as noise. When the user points this out, delete them first instead of continuing to fine-tune.
- Normalize the loudness of the whole video and record the average loudness and peak. Online video commonly targets about −14 to −16 LUFS, with a true peak no higher than −1 dBTP; platforms normalize the volume again, so there is no need to make it louder.

### 6. Master version and versions for each platform

Render one master version first, then derive the version for each platform (landscape, vertical, subtitle files, covers) following [video-platform-versions.md](video-platform-versions.md). Mix the audio in the master version and reuse it in the derived versions, so the sound is the same on every platform.

### 7. Subtitles-only format (optional)

Tell the story with subtitles and music only, without a voice-over; this suits platforms browsed mostly with the sound off. Time the lines by reading speed (1 to 2.5 seconds a line), with a tighter text rhythm than in the voice-over version. It can share visuals with the voice-over version, as an experimental comparison.

## Iteration discipline

- When only the audio changes, export the narration and sound-effect tracks separately, remix them and merge them with the rendered picture; do not re-render the picture.
- When only a few lines change, regenerate only those lines of voice-over, then rebuild the timeline. Once the timeline changes, sound effects and visual events move with it, and the video needs to be re-rendered.
- In each round of changes, keep the previous finished version, increase the version number and record the reason for the change.

## Human approvals

- **Script and facts**: sections, spoken lines, key numbers and sources.
- **Voice**: chosen after listening.
- **Visual anchor**: the asset overview sheet and the narrator's look.
- **Final preview**: the user has watched and listened to the whole finished video. The agent can report only the measured length, loudness and still-frame check results; it cannot replace the user's judgment of how the video sounds.
- **Publishing permission**: approving the final cut is not permission to publish. The user uploads and publishes on each platform; this English edition has no video publishing module.

## Deliverables

- The finished master version and the versions for each platform.
- Subtitle files (such as SRT) and the subtitle text line by line.
- A cover or cover frame for each platform.
- Music license records and attribution text.
- The pronunciation list, the list of fact sources, technical specs (aspect ratio, length, loudness) and the quality review record.
- The production project folder and rebuild command, so lines and music can be changed later.

Save the finished video and the project in the user's content folder or a folder the user names, not in the public Skill source repository.

## Fallbacks

- No animation composition capability: deliver the section script, storyboard, image prompts, voice-over script and asset list.
- Assets but no voice-over: deliver a silent rough cut with subtitles and the voice-over script, marked as waiting for the voice-over.
- Music license unclear: use locally synthesized music or a platform music library, or deliver a version without music and let the user choose music inside the platform.
- Platform rules cannot be confirmed: do not guess AI labels, lengths or sizes; mark them for the user to confirm in the publishing screen.

## Minimum acceptance standard

- The spoken script is complete and matches the subtitles line by line; names and numbers have been checked against the pronunciation list.
- Every key fact has a source, and the numbers on screen match the spoken lines.
- No missing assets, black blocks, overflowing text, trademarks or garbled text.
- The music license is recorded; where attribution is required, it is in both the description and the end of the video.
- Loudness and peak are measured and recorded, and the user has listened to the whole video.
- The aspect ratio, length, subtitles, cover and AI label fields of each platform version are recorded.
