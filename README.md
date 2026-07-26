<div align="center">

  <h1><a href="https://github.com/ScottKirvan/RPSandbox">ScottKirvan/RPSandbox</a></h1>
  <h3>Sandbox for testing Release Please and shared GitHub Actions workflow patterns</h3>

<!-- Badges -->
<p>
  <a href="https://github.com/ScottKirvan/RPSandbox/graphs/contributors">
    <img src="https://img.shields.io/github/contributors/ScottKirvan/RPSandbox" alt="contributors" />
  </a>
  <a href="">
    <img src="https://img.shields.io/github/last-commit/ScottKirvan/RPSandbox" alt="last update" />
  </a>
  <a href="https://github.com/ScottKirvan/RPSandbox/issues/">
    <img src="https://img.shields.io/github/issues/ScottKirvan/RPSandbox" alt="open issues" />
  </a>
  <a href="https://github.com/ScottKirvan/RPSandbox/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/ScottKirvan/RPSandbox.svg" alt="license" />
  </a>
  <a href="https://discord.gg/TN6XJSNK5Y">
    <img src="https://img.shields.io/discord/1052011377415438346?style=flat-square&label=discord&color=00ACD7">
  </a>
</p>

<h4>
    <a href="https://github.com/ScottKirvan/RPSandbox/issues/">Report Bug</a>
  <span> · </span>
    <a href="https://github.com/ScottKirvan/RPSandbox/issues/">Request Feature</a>
  </h4>
</div>

**RPSandbox** is a sandbox repo for iterating on release automation across the BojuStudio project ecosystem. It's used to test and refine Release Please configuration, AI-generated release notes, and Discord notification workflows before rolling changes out to production repos.

Workflows
---------
Local copies of shared workflows live in `.github/workflows/` for in-place experimentation:

- `local-release-notes.yml` — sandbox version of the AI release notes rewriter (narrative prose + What Changed bullets)
- `local-discord-notify.yml` — sandbox version of the Discord release notification (posts only the What Changed bullet list)
- `release.yml` — ties it all together: Release Please → AI notes → Discord notify

Shared production workflows live in [ScottKirvan/.github](https://github.com/ScottKirvan/.github).

Contributions / Contact
-----------------------
- [File an issue](https://github.com/ScottKirvan/RPSandbox/issues/) or submit a [pull request](https://github.com/ScottKirvan/RPSandbox/pulls)
- Contact me at [linkedin.com/in/scottkirvan/](https://www.linkedin.com/in/scottkirvan/)
- Find me on [Discord](https://discord.gg/TN6XJSNK5Y) as cptvideo

Credits
-------
**Copyright (c) 2024:** [Scott Kirvan](https://github.com/ScottKirvan) — All rights reserved  
*RPSandbox is licensed under the [MIT License](LICENSE.md).*

Project Link: [RPSandbox](https://github.com/ScottKirvan/RPSandbox)  
[CHANGELOG](notes/CHANGELOG.md)
