# screensaver.greynetic addon for Kodi

This is a [Kodi](http://kodi.tv) screensaver addon.

[![License: GPL-2.0-or-later](https://img.shields.io/badge/License-GPL%20v2+-blue.svg)](LICENSE.md)
[![Build and run tests](https://github.com/xbmc/screensaver.greynetic/actions/workflows/build.yml/badge.svg?branch=Matrix)](https://github.com/xbmc/screensaver.greynetic/actions/workflows/build.yml)
[![Build Status](https://dev.azure.com/teamkodi/binary-addons/_apis/build/status/xbmc.screensaver.greynetic?branchName=Matrix)](https://dev.azure.com/teamkodi/binary-addons/_build/latest?definitionId=44&branchName=Matrix)
[![Build Status](https://jenkins.kodi.tv/view/Addons/job/xbmc/job/screensaver.greynetic/job/Matrix/badge/icon)](https://jenkins.kodi.tv/blue/organizations/jenkins/xbmc%2Fscreensaver.greynetic/branches/)

## Build instructions

When building the addon you have to use the correct branch depending on which version of Kodi you're building against. 
For example, if you're building the `Matrix` branch of Kodi you should checkout the `Matrix` branch of this repository. 
Also make sure you follow this README from the branch in question.

### Linux

The following instructions assume you will have built Kodi already in the `kodi-build` directory 
suggested by the README.

1. `git clone --branch Matrix https://github.com/xbmc/xbmc.git`
2. `git clone --branch Matrix https://github.com/xbmc/screensaver.greynetic.git`
3. `cd screensaver.greynetic && mkdir build && cd build`
4. `cmake -DADDONS_TO_BUILD=screensaver.greynetic -DADDON_SRC_PREFIX=../.. -DCMAKE_BUILD_TYPE=Debug -DCMAKE_INSTALL_PREFIX=../../xbmc/kodi-build/addons -DPACKAGE_ZIP=1 ../../xbmc/cmake/addons`
5. `make`

The addon files will be placed in `../../xbmc/kodi-build/addons` so if you build Kodi from source and run it directly 
the addon will be available as a system addon.
