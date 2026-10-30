# Agentic Model – Releases

This repository publishes the release feed for Agentic Model installations. It contains no source code.

## What is here

- **Release feed**: a signed `releases.json`, attached to the `feed` release. Installations check this feed regularly
  to find out whether a new version is available.
- **Container images**: published separately in the GitHub Container Registry. The feed refers to them by digest.

## How updates work

1. A new version is built and its images are pushed to the registry.
2. The version is added to the release feed, which is signed with the vendor's key.
3. Installations pick up the feed, verify the signature and offer the update to their administrators.
4. The installation only installs an image that is listed in a correctly signed feed, pinned by its digest.

Feeds or images from anywhere else are ignored, so nobody else can offer an update to an installation.

## For customers

Normally you don't need to do anything here: your installation finds new versions on its own. If your installation
has no internet access, ask your supplier for an update file instead.

## Support

For questions about your installation or license, contact your supplier.
