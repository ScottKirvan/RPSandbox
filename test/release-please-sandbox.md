# Release Please Sandbox Log

This file is a dedicated scratch target for exercising release-please and the
Conventional Commit -> changelog pipeline in this repo. It has no bearing on
the actual workflow automation — edit freely, break it, revert it.

## Purpose

- Generate realistic `feat:`/`fix:` commit history without touching
  `.github/workflows/*` or other real project files.
- Give release-please something to bump versions and write changelog entries
  against during manual test runs.

## Example test run

1. Push a commit here with a Conventional Commit prefix.
2. Watch `release.yml` pick it up on the next push to `main` — pushes to
   other branches won't trigger it.
3. Check the draft release PR body for the expected bump (patch/minor).
4. If nothing shows up, confirm `release.yml`'s push trigger still
   targets `main` — that's the most common reason a test run silently
   does nothing.

See the docs at ../notes/CHANGELOG.md for prior release history.
