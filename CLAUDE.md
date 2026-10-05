# www.mrlevine.com
## Be ADHD-Friendly
At the start of each session, invoke the `i-have-adhd` skill yourself before doing anything else, then say "ADHD mode is on for the rest of the session", and apply its rules to all lessons and chat messages you generate for the rest of the session. In lessons:
1. Overview answers: key fact first, then a few short bullets.
2. Steps: one action each.
3. Add visible wins so students see their progress as they work.
4. Cut anything students don't need to do the work.
5. Cap lists at 5 items by grouping related items, never by dropping content. Verbatim content, like objectives, is exempt.
6. Put information right next to the step that uses it.
## Infer Which Lesson to Edit
After reading the attached resources from Code.org, infer which lesson to edit in `/content/courses/{course}/{lesson}`.
## Include All Information in Lessons
Students do not see the attached resources from Code.org; they only see the lesson. Do not refer to these resources; copy or adapt the information from them into the lesson.
## Copy Objectives Verbatim
Copy objectives verbatim in the exact order from the attached lesson plan, editing only to ensure every objective ends with a period and is free of typos, briefly summarizing any such edits or lack thereof.
## Address Students Directly
Students read the lessons; use second person to address them, adapting information as needed to conform to this standard.
## State Assignment Todos Clearly
Each `###` under `## Assignment` should open with a key sentence with a verb stating what work to do (in Unit Journal, which is implied), not a scenario.
## Limit Assignment Todos
Assign at most 3 todos of at most 3 steps each. Every `###` and shortcode counts except `instructions-unit-journal-update`. Merge related work rather than drop it; suggest extra todos in the chat, each justified by an objective.
## Favor Hand-drawing
Students use Notability to create their Unit Journals. When applicable, turn assignment todos into something that needs to be hand-drawn.
## Show Time Estimates
Only put time estimates in `###` headings under `## Assignment`, styled as `~10mins`.
## Format Code Examples
Format all code examples like this:
```js {linenos=table}
console.log("Starting my program!");
console.log("Hi!");
```
## Include Vocabulary
If the attached lesson plan defines vocabulary terms, create or update them in `/content/glossary/{term}`, reference them in `## Lesson Overview` with `{{% define "Term" %}}` outside of any `{{< collapse >}}`, and assign them in `## Assignment` with `{{% unit-journal-define-terms "Term1" "Term2" ... %}}`. Write each `summary` as the lesson plan's definition, trimmed to a concise phrase or sentence: capitalize the first letter, no trailing period, and link any other defined glossary term it mentions as `[term](/glossary/slug/)`.
## Compress Videos
For any video that is untracked or has uncommitted changes (check with `git status -uall`), check its size with `ls -lh`. If it exceeds 25 MiB (the Cloudflare Pages limit for a single asset), compress it with `ffmpeg` at CRF 30, increasing the CRF by 1 until the file is under 25 MiB. Do not compress videos that are already committed and unchanged.
## Be Transparent About Information Sources
In the chat, briefly cite where you found any information you added to a lesson, including which attached or online resources you used and whether the information has been modified.
## Suggest Git Commit Messages
Suggest git commit messages based on previous commits. Never add `Co-Authored-By` lines (or any other AI attribution) to the commit messages.
