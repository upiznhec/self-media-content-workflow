# Digital-human video production

This guidance is an optional production branch of `self-media-short-video`. It describes inputs, human approvals, generation, composition, acceptance and fallbacks, and is not tied to any one digital-human or video tool.

## Entry conditions

Enter digital-human production mode only when all of these hold:

- The user explicitly chooses a digital-human video, not just a script or storyboard.
- The core topic, spoken script, target platforms, target length and main call to action are approved.
- The user is the person whose portrait and voice are used, or holds explicit permission that can be verified.
- The user knows the chosen platform's current terms on storage, model improvement, third-party processing, deletion and opting out.
- The user has uploaded, created and selected the digital human and voice in Topview or the chosen digital-human platform themselves, and has explicitly confirmed that they are ready.
- The aspect ratio, visual style, presenter window position and subtitle form are decided, as is whether AI or digital-human disclosure is needed.

If any of these is missing, return to plan mode and list the gaps; do not guess the user's permission or the platform rules.

## Production process

1. **Rights and data-processing check**: confirm that the user is the person or holds explicit permission, and knows the chosen platform's current terms on storage, model improvement, third-party processing, deletion and opting out. Record only the confirmation status, never the original sensitive assets or platform private IDs.
2. **The user's manual upload**: the user logs in to Topview or the chosen platform and uploads, creates and selects the digital human and voice by hand. This Skill does not use upload credentials, file-upload or voice-cloning interfaces in place of this step. When it is done, the user confirms that "the digital human and voice are ready".
3. **Spoken script preparation**: use the final spoken script as the only source of lines. Keep a pronunciation list for this task's names and numbers. Any change in how something is said goes back into the script or the list; it is not fixed by ear after the video is made.
4. **Generate digital-human clips**: with the digital-human generation capability found at run time and the platform assets the user has already selected, generate presenter clips in sync with the lines. Before paid generation, follow the tool's rules for confirming costs. Prefer natural blinking, slight nodding, and gestures and expressions that fit the meaning; avoid looping, stiff movements.
5. **Compose the explanatory visuals**: the main picture carries the evidence, process, comparison or interface demonstration; the presenter window only keeps the viewer company and adds emphasis, and does not cover key information. In vertical frames, keep the whole face, the head and enough of the shoulders or upper body, so the result is not just a floating head. By default, prefer a rounded rectangle for the window; use a circle or oval only when the whole upper body is still clearly visible.
6. **Add subtitles**: put the subtitles on the main visual layer, with natural line breaks and a line width suited to phone reading; add no extra badges, section labels or explanatory tags. Subtitles must match the final audio line by line, with names and numbers written as in the list.
7. **Export and review**: export the vertical final video for the target platforms. Douyin and Xiaohongshu usually prefer 9:16; exact resolution, length limits, AI labels and commercial disclosure follow the platform's screen or official rules at the time of publishing. After exporting, check the picture, audio, subtitles, presenter framing and readability on phones.

## Human approvals

- **Rights and data processing**: the portrait, likeness, voice and third-party material may be used for this generation and for publishing, and the user knows the chosen platform's current data-processing terms.
- **Platform assets ready**: the user has finished uploading, creating and selecting on the platform themselves; this Skill does not upload original sensitive assets on their behalf.
- **Style and layout**: the visual style, the shape and position of the presenter window, the subtitle style, and whether to keep background music.
- **Final preview**: the spoken script is complete, the presenter looks natural, the subtitles have no errors, the explanatory visuals match the copy, and the presenter window covers nothing and is not reduced to a floating head.
- **Publishing permission**: approving the final cut is not permission to publish; creating drafts or any other external write on a platform still needs separate permission.

## Deliverables

- Generated digital-human clips.
- A visual mapping of the main picture and presenter window, or notes on the composition project.
- The final vertical video, plus an optional subtitle file or subtitle text.
- Cover title, cover picture, publishing title, body, hashtags, background music, and commercial and AI disclosure fields.
- The likeness and voice rights confirmation, platform asset readiness status, pronunciation list, technical specs and quality review record.

The delivery pack must not contain original portraits, recordings, their local paths, temporary upload or download links, object storage keys, file IDs, digital-human IDs, voice IDs or any private ID that could be used to retrieve the sensitive assets again.
Generated digital-human clips and final videos are saved in the user's content folder or a delivery folder the user names, not in the public Skill source repository.

## Fallbacks

- The user has not finished the manual upload and selection on the platform: stay in `AWAITING_USER`, and never try to upload on their behalf.
- No digital-human generation capability: deliver lines that can be used by hand, portrait requirements, a storyboard of the explanatory visuals, the subtitle script and a publishing pack.
- Digital-human clips can be generated but the visuals cannot be composed: deliver the clips, the visual mapping and the subtitle files, and say clearly that the final composition is not done.
- Platform rules cannot be confirmed: do not guess labels or lengths; mark them for the user to confirm in the publishing screen.
- The spoken script is incomplete, or sound and picture are out of sync: keep the status at quality review and do not move on to final-copy approval.

## Minimum acceptance standard

- The spoken script is complete, and the length matches the script and storyboard.
- The presenter's face, head and the planned upper body inside the window are not cropped; expressions and gestures show no obvious loops or stiffness.
- Subtitles match the audio, with no extra badges, section labels, typos, garbled text or covered areas.
- The main picture does the information job, and the presenter window does not cover evidence or key text.
- Original portraits, recordings, their local paths, temporary links and platform private IDs are not in the task card, the content registry, the delivery pack or the repository; index paths of deliverables are not covered by this rule.
- The mobile preview on the target platforms is readable, and the aspect ratio, volume, cover and disclosure fields are recorded.
