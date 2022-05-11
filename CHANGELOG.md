# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
[markdownlint](https://dlaa.me/markdownlint/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

-

## [1.2.8] - 2022-05-11

### Changed in 1.2.8

- update images to 3.0.0
- update Senzing version to 3.0.0
- migrated from yum to apt installer
- remove "-withinfo" for loader and redoer
- update dashboards
- update to 3.0.0 paths
- add new truth set
- create new truth set data sources
- update certificate python to 3.8 and add `-1.0.2` to the filename `self-signed-certificate.zip`
- redoer queue parameters: ApplicationAutoScalingScalingPolicyRedoerLoader targetValue = 20
- add private API server URL

## [1.2.6] - 2022-03-10

### Changed in 1.2.6

- removed Jupyter
- removed flowlogs
- updated image versions

## [1.2.5] - 2022-02-01

### Changed in 1.2.5

- updated yum image version

## [1.2.4] - 2021-11-19

### Changed in 1.2.4

- updated senzing version
- updated stream-loader version
- fixed pass role condition

## [1.2.3] - 2021-10-25

### Changed in 1.2.3

- added XTERM env var

## [1.2.2] - 2021-10-20

### Changed in 1.2.2

- updated image versions

## [1.2.1] - 2021-10-05

### Changed in 1.2.1

- updated lambda error messages

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
