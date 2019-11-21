# Upgrade Guide

This document describes breaking changes and how to upgrade. ~~For a complete list of changes including minor and patch releases, please refer to the [changelog](CHANGELOG.md)~~.

## v3

Removed use of `level-spaces` internally and dropped support for `options.sublevel`. You can still use `level-spaces` by setting `options.sub`, which should work fine as long as you don't use `options.defaultTTL`.

## v2

Switched to `level-spaces`.

## v1

Version 1.0.0 stores are not backwards compatible with previous versions. If you have unexpired entries in a store managed by < 1.0.0, don't expect them to expire if you upgrade to 1.0.0. This is due to a `level-sublevel` change. It is also recommended that you only use `level-sublevel` >= 6.0.0 with `level-ttl`.
