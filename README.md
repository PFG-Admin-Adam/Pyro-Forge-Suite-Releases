# Pyro Forge Suite Releases

This is the public, installer-only update feed for Pyro Forge Suite.

**[Open the newest beta release and download
`Pyro-Forge-Suite-Complete-Setup.exe`](https://github.com/PFG-Admin-Adam/Pyro-Forge-Suite-Releases/releases).**

That one installer installs the User app, Manager app, and Knowledge Hub
together. The User app also contains the Pyro Forge Unreal source-control
plugin, provisions it during installation, and installs/enables it for the
Unreal project selected in Version Control. No separate plugin download is
required. Standalone EXE and MSI installers remain available in the same
release for individual and managed deployment.

## Source of truth

Application source, Knowledge Hub rules, release automation, and version tags
live exclusively in the private `PFG-Admin-Adam/Pyro-Forge-Suite` repository.
This repository is not a second source repository and must not be maintained by
hand.

An hourly public-repository workflow checks the private SSOT through a
read-only GitHub App. When it finds a new version tag, GitHub's free standard
public runner validates and builds the complete suite, creates the unified
installer from those three app packages, then publishes the verified installers
and `pyroforge-release-manifest.json` here. Installed User, Manager, and
Knowledge Hub apps read this repository without a GitHub credential.

The public workflow receives a read-only private-source token. Publishing uses
the separate, repository-local `GITHUB_TOKEN`, which can write only to this
public release repository. No credential can write to both repositories.

## Integrity

Every app verifies the exact release path, installer file name, byte length,
manifest SHA-256, and GitHub asset digest before offering `Install & Restart`.
The beta installers are not yet code-signed, so Windows SmartScreen may still
show an unknown-publisher warning.
