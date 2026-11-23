# Digital-human production in the workflow

This reference sets only the safety boundaries and stage transitions for the main workflow. The script, storyboard, visual composition and acceptance are handled by `self-media-short-video`. The digital human is an optional branch, not the default way to appear on camera.

## Entry conditions

- The user explicitly chooses a digital-human video and approves the final spoken script, target platforms, length and visual direction.
- The user is the person whose portrait and voice are used, or holds explicit permission that can be verified.
- The user knows the chosen digital-human platform's current terms on storage, model improvement, third-party processing, deletion and opting out.
- The user has uploaded, created and selected the digital human and voice in Topview or the chosen platform themselves.

This workflow never uploads original portraits or recordings. Until the manual upload is done, stay in `AWAITING_USER`. The only next step is to ask the user to finish uploading and selecting on the platform, then confirm that "the digital human and voice are ready".

## Stage transitions

```text
Spoken script and platforms approved
→ Likeness and voice rights and third-party data processing confirmed
→ AWAITING_USER: the user uploads, creates and selects the assets on the digital-human platform
→ The user confirms the platform assets are ready
→ Cost and generation settings confirmed (if applicable)
→ Digital-human presenter clips
→ Explanatory visuals, subtitles and presenter window composed
→ Quality review
→ Awaiting final-copy approval
```

The confirmation that the manual upload is ready is the sensitive-asset gate of the digital-human branch. It does not replace the five existing approvals: direction, platforms, title, final copy and permission for an external write action. Approving the final copy still does not authorize any external write action.

## Data minimization

- For sensitive assets, the task card records only yes/no statuses: rights confirmed, third-party terms read, platform upload done and assets selected. Index paths of deliverables such as generated clips, final videos and subtitles may go into the task card, the content registry and save checks.
- Never record original portraits, recordings, their local paths, temporary upload or download links, object storage keys, file IDs, digital-human IDs, voice IDs or any private ID that could be used to retrieve the sensitive assets again.
- When a resource ID is truly needed at run time, use it only temporarily in the authorized operation; do not write it into logs, task cards, the content registry or the repository.
- The publishing pack contains only generated clips, the final video, subtitles and public publishing fields, never original sensitive assets.
- Generated digital-human clips and final videos are saved in the user's content folder or a delivery folder the user names, not in the public Skill source repository.

## Risks and fallbacks

- The user has not finished the manual upload: stay in `AWAITING_USER`, and never try to upload on their behalf.
- The rights or third-party data-processing boundaries are unclear: the status is `NEEDS_CONTEXT`; do not start generation.
- Generation or composition is unavailable: deliver the lines, storyboard, visual mapping, subtitle script and a checklist for making it by hand.
- The presenter looks unnatural, lines are incomplete, sound and picture are out of sync, or the disclosure requirements are unconfirmed: stop at quality review and do not move on to final-copy approval.
