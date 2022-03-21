# arm-dependencies

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/shitwolfymakes/arm-dependencies/publish-image)
![Docker](https://img.shields.io/docker/pulls/shitwolfymakes/arm-dependencies.svg)

[![GitHub license](https://img.shields.io/github/license/shitwolfymakes/arm-dependencies?style=plastic)](https://github.com/shitwolfymakes/arm-dependencies/blob/main/LICENSE)
[![GitHub forks](https://img.shields.io/github/forks/shitwolfymakes/arm-dependencies?style=plastic)](https://github.com/shitwolfymakes/arm-dependencies/network)
[![GitHub stars](https://img.shields.io/github/stars/shitwolfymakes/arm-dependencies?style=plastic)](https://github.com/shitwolfymakes/arm-dependencies/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/shitwolfymakes/arm-dependencies?style=plastic)](https://github.com/shitwolfymakes/arm-dependencies/issues)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/shitwolfymakes/arm-dependencies?style=plastic)](https://github.com/shitwolfymakes/arm-dependencies/pulls)

![PyPI - Python Version](https://img.shields.io/pypi/pyversions/django?style=plastic)


## Overview
This repo codifies the requirements for building and running Automatic Ripping Machine, and provides a docker container that has everything preinstalled. All you need to do is install the ARM source and set up files.

The `arm-dependencies`Docker image is rebuilt every night, so you should always get the most up-to-date versions of MakeMKV and Handbrake when you build ARM from this image.


## Usage
### Git Repo
To add this manually, run the following command:
```shell
git submodule add -b main https://github.com/shitwolfymakes/arm-dependencies arm-dependencies
```

In your fork's `requirements.txt`, replace everything with
```text
-r arm-dependencies/requirements.txt
```

### Docker Container
To base your docker container on `arm-dependencies`, add this to the top of your `Dockerfile`:
```dockerfile
FROM shitwolfymakes/arm-dependencies AS base
```