---
name: dot-pro
description: Coordinate ChatGPT web Pro direct Git delivery with Dot and local Codex for authorized work. Use for requested Pro or Dot collaboration, compatible Azure Git delivery, ChatGPT Deep Research, or website image workflows. Inspecting this skill does not dispatch a task.
---

# dot-pro

Coordinate ChatGPT web Pro, Dot and local Codex using the runtime's documented native browser or desktop-app APIs. Codex owns the task boundaries, verification and authorized integration. A skill match does not itself authorize sending material, changing settings, writing a repository, merging or deploying.

## Choose and bind the workers

Follow the user's chosen account, browser, conversation, model, execution path, task scope and disclosure limits. For multiple accounts, use the user's assignments or task context; confirm the actual account, selected Pro model, connection and tab before submission. Reuse relevant conversations without duplicating work. Split independent tasks only when useful, give writers distinct branches or non-overlapping ownership, and serialize dependent changes.

Bind each action to its selected tab or desktop session and pair Dot with a Pro conversation only when their account/session matches. Use the runtime's documented browser controls. Do not copy credentials or browser state, bypass login or security prompts, or silently substitute another model. Report unavailable accounts, tools or quota based on the actual visible state.

## Deliver authorized code work

When the user authorizes compatible Azure Git delivery and the selected Pro conversation has the Git MCP connected, prefer Pro's direct path: select the fixed manifest, read relevant source, make the scoped UTF-8 changes, commit on the task fork, and create or update its PR. Pro mode alone does not establish a connection or write access. Read [Git MCP reference](references/git-mcp.md) for its exact tools, manifest handling and recovery. The service and its URL must be supplied and approved by the user; this skill does not provide or deploy a backend.

Use Dot for tasks needing an actual execution environment, business checks, non-text changes, or an existing accepted long-running task. The described MCP has no shell, test/build execution, Issue management, merge or deployment. A PR or tool response is not proof of testing, company receipt or release. Codex verifies the actual branch, PR, changes and reported checks, then performs only the integration authorized by the user and project rules.

If Pro's connection or required tools are unavailable, report the precise limitation. If setup is authorized, connect the approved service; otherwise give Pro the authorized source excerpts, paths and revision for a concrete patch, then have Dot apply, check and deliver it where authorized. If Pro itself is unavailable, say so and continue only through an authorized workable path. Keep consequential blockers and shared-interface questions in the same Pro conversation with the actual error and current diff; do not repeat resolved questions or mandate an extra review.

Keep the owner, account/conversation, fixed baseline, actual branch and PR, dependencies and completion condition in the existing task context. The MCP and direct Git routes may use different branch prefixes for an older manifest; identify the actual branch when handing work between them. An existing Issue may be referenced in the PR body; use an authorized capable tool for any Issue management required by the task.

## Observe, recover and report

Observe the actual target message and status. If a send or write has an uncertain outcome, inspect the original conversation or call `get_delivery` with the same project, fixed manifest, account and task before deciding whether to retry. Do not duplicate assignments, pushes or PRs. Use notifications where available and check at an appropriate interval; report meaningful progress and actual blockers rather than unchanged status.

Follow the task's authorization and current platform confirmation rules. If an automatic review denies an operation, report the operation and reason; do not rephrase or reroute the same denied action. Retry only after the relevant authorization, capability or inputs change. Do not invent checks, hashes, compatibility layers or other work beyond the requested result. Scheduled or recurring tasks require a user request.

## Other website workflows

- **Review and analysis:** provide only authorized context, keep the chosen conversation for follow-up, and compare findings with actual source and behavior. Review alone does not authorize edits.
- **Deep Research:** use the website's actual research mode, wait for its result, and return the available complete report and source links. Report missing access or citations rather than presenting ordinary chat as research.
- **Images:** use the website's image creation or editing flow, upload only authorized references, and retrieve the actual result originals with documented browser capabilities. Continue requested edits in the same conversation.
