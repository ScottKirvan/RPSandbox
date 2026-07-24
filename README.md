<div align="center">

  <h1><a href="https://github.com/ScottKirvan/ReleasePleaseTest">ScottKirvan/ReleasePleaseTest</a></h1>
  <h3>Sandbox for testing Release Please and shared GitHub Actions workflow patterns</h3>

<!-- Badges -->
<p>
  <a href="https://github.com/ScottKirvan/ReleasePleaseTest/graphs/contributors">
    <img src="https://img.shields.io/github/contributors/ScottKirvan/ReleasePleaseTest" alt="contributors" />
  </a>
  <a href="">
    <img src="https://img.shields.io/github/last-commit/ScottKirvan/ReleasePleaseTest" alt="last update" />
  </a>
  <a href="https://github.com/ScottKirvan/ReleasePleaseTest/issues/">
    <img src="https://img.shields.io/github/issues/ScottKirvan/ReleasePleaseTest" alt="open issues" />
  </a>
  <a href="https://github.com/ScottKirvan/ReleasePleaseTest/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/ScottKirvan/ReleasePleaseTest.svg" alt="license" />
  </a>
  <a href="https://discord.gg/TN6XJSNK5Y">
    <img src="https://img.shields.io/discord/1052011377415438346?style=flat-square&label=discord&color=00ACD7">
  </a>
</p>

<h4>
    <a href="https://github.com/ScottKirvan/ReleasePleaseTest/issues/">Report Bug</a>
  <span> · </span>
    <a href="https://github.com/ScottKirvan/ReleasePleaseTest/issues/">Request Feature</a>
  </h4>
</div>

**ReleasePleaseTest** is a sandbox repo for iterating on release automation across the BojuStudio project ecosystem. It's used to test and refine Release Please configuration, AI-generated release notes, and Discord notification workflows before rolling changes out to production repos.

Workflows
---------
Local copies of shared workflows live in `.github/workflows/` for in-place experimentation:

- `local-release-notes.yml` — sandbox version of the AI release notes rewriter (narrative prose + What Changed bullets)
- `local-discord-notify.yml` — sandbox version of the Discord release notification (posts only the What Changed bullet list)
- `release.yml` — ties it all together: Release Please → AI notes → Discord notify

Shared production workflows live in [ScottKirvan/.github](https://github.com/ScottKirvan/.github).

Contributions / Contact
-----------------------
- [File an issue](https://github.com/ScottKirvan/ReleasePleaseTest/issues/) or submit a [pull request](https://github.com/ScottKirvan/ReleasePleaseTest/pulls)
- Contact me at [linkedin.com/in/scottkirvan/](https://www.linkedin.com/in/scottkirvan/)
- Find me on [Discord](https://discord.gg/TN6XJSNK5Y) as cptvideo

Credits
-------
**Copyright (c) 2024:** [Scott Kirvan](https://github.com/ScottKirvan) — All rights reserved  
*ReleasePleaseTest is licensed under the [MIT License](LICENSE.md).*

Project Link: [ReleasePleaseTest](https://github.com/ScottKirvan/ReleasePleaseTest)  
[CHANGELOG](notes/CHANGELOG.md)
