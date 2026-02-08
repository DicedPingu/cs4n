# Control Profiles
Pick one profile and include it in your prompt.

## Profile A - Fast Patch
Use when: small bug/docs fix needed quickly.
- Keep edits minimal and localized.
- Prefer smallest safe change over refactor.
- Run focused validation only.

## Profile B - Production Safe
Use when: reliability and regressions matter.
- Read all related files before editing.
- Add or update tests for behavior changes.
- Explain tradeoffs and failure modes.
- Avoid risky commands and broad rewrites.

## Profile C - Deep Refactor
Use when: structure and maintainability are the priority.
- Reorganize modules for coherence.
- Preserve behavior unless explicitly approved to change.
- Leave migration notes in changed docs.
- Validate full affected workflow, not only unit tests.

## Profile D - Reviewer Mode
Use when: you want a strict code review first.
- Prioritize findings by severity.
- Include file references for each finding.
- Suggest concrete patches, not just comments.
- State residual risk and missing tests.

