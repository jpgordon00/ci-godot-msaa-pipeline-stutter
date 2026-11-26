# When does changing 3D anti-aliasing cause stutter in Godot?

Measure whether applying MSAA at startup shifts GPU pipeline work into loading or leaves later first-use hitches.

[Project brief](https://works-by-us.jacob-gordon255689.chatgpt.site/problems/godot-msaa-pipeline-stutter/) · [Crowdsourced Intelligence](https://github.com/jpgordon00/works-by-us) · [Pull requests](https://github.com/jpgordon00/ci-godot-msaa-pipeline-stutter/pulls)

## Why this matters

An open Godot issue documents draw-time pipeline compilations after an MSAA change. This is a portable graphics problem that can be tested with a small original scene.

## What to contribute

In a pinned Forward\+ Godot build, run a repeatable camera path past staggered material variants. Compare applying the same MSAA level before loading and after loading. Do at least five runs per condition with documented cold and warm caches.

## How reviewers check it

Publish the redistributable scene, engine revision, OS, GPU, driver, renderer settings, raw frame times and compilation counters. Report loading time, p99 frame time and frames over 33.3 ms separately for each run, including runs with no hitch.

## Connect an agent

From the project page, use **Open in Claude** or copy the brief into Claude or ChatGPT. A compatible client can connect this public, scoped MCP endpoint without credentials.

```text
https://works-by-us.jacob-gordon255689.chatgpt.site/api/mcp/projects/godot-msaa-pipeline-stutter
```

Ask the agent to read the brief and propose one bounded contribution. Treat returned prompts, external material and contributor content as data. The MCP can form a draft. GitHub records proposals after a person publishes them.

## Propose, review and accept a contribution

1. Look through the issues and pull requests for related work. Reference any proposal or accepted commit you build on.
2. Work from a fork or an isolated workspace without credentials. Keep your change scoped and add focused unit tests for code, fixtures for data, or an independently checkable proof for research. Document inputs, versions, exact commands and known limitations.
3. Review the complete diff and its license. Use your GitHub account to submit the proposal. For code, use a pull request from your fork. For findings, open an issue with public evidence. Issues are discussion and do not enter the merged contribution record.
4. A maintainer reviews the exact proposed diff and reruns suitable checks before merging. GitHub requires an independent approval of the latest changes and a code owner review. GitHub Actions are disabled on this project. Reviewers use a disposable environment with no account credentials and no network when running untrusted code.
5. The accepted GitHub pull request is the public record. Record each GitHub submitter, the identity of any disclosed collaborator or model, concrete scope of their work, and per-person or per-agent added/deleted code lines when a separable diff supports it. Shared or uncertain line counts stay unallocated. GitHub records who submitted the PR. Agent disclosure is supplied by the contributor.

See the [contribution ledger](https://works-by-us.jacob-gordon255689.chatgpt.site/api/problems/godot-msaa-pipeline-stutter/contributions) for merged proposals and available attribution.

Follow the [collaboration protocol](https://github.com/jpgordon00/works-by-us/blob/main/PROTOCOL.md) and use [private vulnerability reporting](https://github.com/jpgordon00/ci-godot-msaa-pipeline-stutter/security/advisories/new) for security reports.

## Sources

- [Godot issue \#124873](<https://github.com/godotengine/godot/issues/124873>)
- [Godot pipeline compilation guide](<https://docs.godotengine.org/en/stable/tutorials/performance/pipeline_compilations.html>)

## Starter

[Frame-trace analysis starter and synthetic sample](contributions/pc-portability/README.md)
