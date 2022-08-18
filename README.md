<!-- DevOps.nvim -->

# Arch Linux Installer

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![Telegram][telegram-shield]][telegram-url]

<!-- GETTING STARTED -->

## Introduction

Install archlinux and config based on a yaml configuration

## Getting Started

### Prerequrments

- Just Learning yaml :)

### Installation

Then we can clone this template or download script directly

```sh
wget archinstaller.ml -O ArchInstaller
# or git clone https://github.com/FakeSudo/ArchInstaller
chmod +x ArchInstaller
./ArchInstaller # or ./ArchInstaller {url}
```

NOTE: before running Installer write config.yaml or pass a pastbin or git gist url to script

## Configuration

Config will separate into user settings that run after Installation and root settings

### Root settings:

- username

- Note : defualt password is 'password' and you can change it after reboot

- hostname

- locale

  common: `en_US.UTF-8 UTF-8`

- timezone

  Find your timezone with `timedatectl list-timezones`

- shell

  Default user shell

  common: `/bin/bash`

- drive

  - blk

    The hard drive you want to install arch on it

    example: `/dev/sda`

  - erase

    Format the hard drive don't enable this field unless you know what are you doing

    example: Boolean value

  - partitions

    List of partition to create
    Contains:

    - size
      in `K/M/G` format
    - filesystem

      type of the partition

      commons: `uefi/linux/swap & all fdisk types`

    - number

      the number of the primary partition

  for more information read `fdisk` manual

- base packages

  Packages needed for booting the system

- base daemons

### User settings contains:

- custom script

- aurhelper

  common: `yay/paru`

- user packages

- user daemon

Note: if you configured user setting you should rerun installer command after reboot

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/FakeSudo/ArchInstaller?style=for-the-badge
[contributors-url]: https://github.com/FakeSudo/ArchInstaller/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/FakeSudo/ArchInstaller?style=for-the-badge
[forks-url]: https://github.com/FakeSudo/ArchInstaller/network/members
[stars-shield]: https://img.shields.io/github/stars/FakeSudo/ArchInstaller?style=for-the-badge
[stars-url]: https://github.com/FakeSudo/ArchInstaller/stargazers
[issues-shield]: https://img.shields.io/github/issues/FakeSudo/ArchInstaller?style=for-the-badge
[issues-url]: https://github.com/FakeSudo/ArchInstaller/issues
[license-shield]: https://img.shields.io/github/license/FakeSudo/ArchInstaller?style=for-the-badge
[license-url]: https://github.com/FakeSudo/ArchInstaller/blob/main/LICENSE.md
[telegram-shield]: https://img.shields.io/badge/Telegram-blue.svg?style=for-the-badge&logo=telegram
[telegram-url]: https://t.me/FakeSudo
