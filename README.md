# SwiftFormat-nightly

[![GitHub Release](https://img.shields.io/github/v/release/calda/SwiftFormat-nightly?label=current%20build)](https://github.com/calda/SwiftFormat-nightly/releases/latest)
 [![Nightly Release](https://github.com/calda/SwiftFormat-nightly/actions/workflows/nightly.yml/badge.svg?branch=main)](https://github.com/calda/SwiftFormat-nightly/actions/workflows/nightly.yml) [![Build Release Artifacts](https://github.com/calda/SwiftFormat-nightly/actions/workflows/release.yml/badge.svg?event=release)](https://github.com/calda/SwiftFormat-nightly/actions/workflows/release.yml)

Nightly builds of the [SwiftFormat](https://github.com/nicklockwood/SwiftFormat) tool's [`develop`](https://github.com/nicklockwood/SwiftFormat/commits/develop/) branch.

**Nightly builds are subject to breaking changes.**

## Why?

SwiftFormat development happens on the `develop` branch. Commit SHAs on `develop` are unstable since that branch is occasionally rebased.

Nightly release URLs and tags in this repo are stable references and can be used from other repos or tools.

## How?

This repo has a [nightly job](https://github.com/calda/SwiftFormat-nightly/blob/main/.github/workflows/nightly.yml) that:
 - synchronizes this repo's `develop` branch with the [upstream `develop` branch](https://github.com/nicklockwood/SwiftFormat/commits/develop/)
 - publishes a tag and release with the format `YYYY-MM-DD`

Artifacts are built and uploaded to each nightly release using the standard [Build Release Artifacts](https://github.com/nicklockwood/SwiftFormat/blob/develop/.github/workflows/release.yml) job in the SwiftFormat repo. This job is automatically triggered after the nightly job publishes a new release.
