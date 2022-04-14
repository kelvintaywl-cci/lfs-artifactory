# lfs-artifactory
Exploring Git LFS with Artifactory on CircleCI

This repo is based on [the official Artifactory Quick-start guide here](https://jfrog.com/knowledge-base/git-lfs-artifactory-quick-start-guide/), but updated to include CircleCI setup.

**NOTE** that the CircleCI setup uses a LFS_CONFIG project env var.

This env var value is the `.lfsconfig` file base64-encoded.

In other words,

```console
# base64 our .lfsconfig and set this to LFS_CONFIG project env var
$ cat .lfsconfig | base64

# to re-install this .lfsconfig
$ printenv LFS_CONFIG | base64 > .lfsconfig
```
