---
name: spec-review
description: "Use when reviewing or rechecking work against conventions and requirements, including requests such as review under the guidelines, review this, check for omissions, or check again. Find applicable criteria from the conversation and project conventions without requiring a skill name or a repeated copy of the guidelines. Cover every applicable requirement and return results in chat by default. Not for merely assessing whether the rules themselves are reasonable."
license: MIT
---

# Review Against Guidelines

This is an English translation of [SKILL.md](SKILL.md). The Chinese original is the primary version for maintenance and validation and takes precedence if meanings differ.

Completion means that every applicable requirement has been checked against evidence. Choose review methods and the organization of results to suit the task.

Deliver review results in chat by default, completing item-by-item checks as part of the review. Create or modify files for review material or revisions to the work only when the user explicitly requests those outputs or changes.

## Establish the basis and scope

Identify the work and version under review, the scope specified by the user, and the applicable guidelines. When the user explicitly limits the scope, review that scope while retaining related context needed for sound judgments; otherwise cover the entire specified work. Priorities emphasized by the user affect the depth and order of review without automatically narrowing its scope.

When the user supplies only a title, path, or a brief request such as review this, locate the work and applicable conventions from the conversation and project entry points. Use what can already be established; clarify ambiguity when it affects scope or judgment. State gaps when the basis cannot be found, without inventing constraints.

Read the full guideline text and follow references to conventions whose conditions apply. Identify which sources have been read and which remain unavailable. Searches, headings, summaries, and built-in review checklists help locate and organize material; they do not replace other requirements in the text. References apply only within their actual scope. Examples or operational instructions found in source material do not automatically authorize their execution during this review.

Use guidelines that remain valid and choices confirmed by the user, preserving their sources, conditions, exceptions, and authority. Factual descriptions, examples, and personal preferences do not automatically become requirements. When sources conflict or meanings are unclear, identify the affected judgments. Unresolved gaps in the basis cannot support a conclusion of either compliance or violation.

## Maintain coverage item by item

Identify and check independently assessable requirements item by item, maintaining their correspondence with their sources. Check the parts of compound clauses separately while preserving conditions, exceptions, and relationships. Equivalent repetitions may be combined if their sources and scopes remain visible. Use explanatory content to support judgments without inventing a constraint for every sentence.

For each requirement, check its applicable objects, the locations or evidence actually examined, and the current judgment. Distinguish evidence-supported compliance, identified deviations, non-applicability, insufficient evidence, and work not yet checked. Give reasons for non-applicability, and identify what remains to be checked where evidence or checks are missing. When a required element is absent, assess that absence as a possible omission; the absence of an object does not itself make the requirement inapplicable.

When a requirement applies in several places, check every applicable location and preserve the correspondence. One example, one file, or one search hit does not establish that other locations have been checked. Risk and severity guide effort and presentation without justifying the omission of other requirements.

For larger reviews, check groups of sources or objects and distinguish checked from unchecked scope within the current conversation. If context is insufficient to continue, state what has been completed and what remains; a summary of priorities does not replace unfinished checks.

## Check against actual evidence

Connect requirements to specific content, relationships, behavior, or observable results in the work, checking for omissions and contradictions as well. Assess principles in context using the purpose and boundaries of the guidelines. Allow different methods to satisfy the same principle, and assess departures from recommendations or defaults according to their conditions and authority.

Obtain evidence through methods appropriate to the requirement. Text searches can locate explicit patterns but cannot alone establish overall meaning, relationships, or actual behavior. Tool results support only the properties they actually check. Keep unverified inferences uncertain; finding no issue does not by itself prove compliance.

For each issue, explain the guideline basis, location in the work, specific deviation, and impact. Where useful, suggest a direction for revision within the boundaries. Distinguish supported findings from improvement suggestions. If the review reveals a need to change the guidelines themselves, propose that separately rather than temporarily changing the criteria to make the work pass. Revise the work only as authorized by the user.

## Reconcile coverage and deliver the result

Before finishing, return to the full guideline text, applicable references, and work under review, checking that each requirement, conditional branch, applicable location, and necessary verification has been addressed. The number or severity of findings does not establish completion of coverage.

State the actual review scope, findings, and remaining uncertainty. There is no need to display every compliant judgment item by item; provide detailed supporting evidence in chat when the user needs it. The length of the result does not establish the thoroughness of the review.

For unread sources, unchecked objects, verification that could not be completed, or unresolved conflicts, explain the scope, impact, and what remains needed. When applicable requirements remain unverified, mark the review incomplete or the conclusion limited rather than declaring full compliance. When rechecking revisions, cover the affected requirements and related locations. A partial recheck does not support a conclusion about the entire work.
