# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
[markdownlint](https://dlaa.me/markdownlint/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.2.0] - 2021-09-17

### Changed in 1.2.0

- updated to run on self initializing database cluster
- Updated security to match what was done for marketplace
- updated to new POC server
- added WSS support for the web app
- rearranged parameters to match marketplace
- updated images to the latest
- added senzing 2.8.2 as default
- removed EFS mounts for images with built-in data

## [1.0.1] - 2021-05-18

### Changed in 1.0.1

- Improved IamPolicy for SQS

## [1.0.0] - 2021-05-17

### Added to 1.0.0

- Initial functionality to optionally deploy:
  - Senzing: API Server, Web app, Stream loader, Stream producer, Redoer, SSHD, Xterm
  - Swagger UI
