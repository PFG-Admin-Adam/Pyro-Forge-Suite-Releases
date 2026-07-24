# Pyro Forge Suite Releases

This is the public, installer-only update feed for Pyro Forge Suite.

Download beta installers from
[Releases](https://github.com/PFG-Admin-Adam/Pyro-Forge-Suite-Releases/releases).

## Source of truth

Application source, Knowledge Hub rules, release automation, and version tags
live exclusively in the private `PFG-Admin-Adam/Pyro-Forge-Suite` repository.
This repository is not a second source repository and must not be maintained by
hand.

Each private SSOT version tag builds the complete suite once and automatically
publishes the verified installers and `pyroforge-release-manifest.json` here.
Installed User, Manager, and Knowledge Hub apps read this repository without a
GitHub credential.

## Integrity

Every app verifies the exact release path, installer file name, byte length,
manifest SHA-256, and GitHub asset digest before offering `Install & Restart`.
The beta installers are not yet code-signed, so Windows SmartScreen may still
show an unknown-publisher warning.
