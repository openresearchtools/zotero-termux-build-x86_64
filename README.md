# Zotero native Termux x86_64 builder

This repository provides an isolated GitHub Actions cache and downloadable build
artifacts for Intel/AMD Android running native Termux. Application source,
Termux recipes, patches and licenses live in
[openresearchtools/zotero-termux](https://github.com/openresearchtools/zotero-termux).

Run **Zotero native Termux x86_64** with an exact source commit and request ID.
The workflow calls the pinned shared build definition, compiles with the official
Termux toolchain, and validates Android/Bionic package metadata and ELF files.
The completed Gecko component is uploaded before application assembly; both
compiler-cache entries and the separately reusable component remain in this
repository. Packages can be downloaded directly from the completed Actions run.

The source workflow dispatches this builder and collects its matching package.
It requires `BUILD_REPOS_TOKEN` with Actions read/write access to this builder.
This repository requires no signing secret and publishes no GitHub releases.
