# Homebrew tap for Radarr and Sonarr

This personal tap packages the official macOS app archives published by the
[Radarr](https://radarr.video/) and [Sonarr](https://sonarr.tv/) projects.

The update workflow checks the upstream GitHub releases every day, downloads the
ARM64 and Intel app archives, recalculates SHA-256 checksums, and commits cask
updates only when a new stable release is available.

## Install

```sh
brew tap Super-Zane/arr
brew trust --cask Super-Zane/arr/radarr
brew trust --cask Super-Zane/arr/sonarr
brew install --cask Super-Zane/arr/radarr
brew install --cask Super-Zane/arr/sonarr
```

## Update

```sh
brew update
brew upgrade --cask Super-Zane/arr/radarr Super-Zane/arr/sonarr
```

The binaries come from the upstream GitHub releases. This tap removes the
disabled Homebrew cask definitions, but it does not make the upstream apps
Apple-notarized; macOS Gatekeeper behavior may still require the official
self-signing step after an update.
