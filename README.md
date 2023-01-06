# ROS Debian package builder action

Convert ROS packages to Debian packages.

## Inputs

## `ROS_DISTRO`

**Required** The ROS distribution codename to compile for.

## `DEB_DISTRO`

**Required** The Debian/Ubuntu distribution codename to compile for.

## `REPOS_FILE`

Repos file with list of repositories to package.
Defaults to sources.repos.

## `GITHUB_TOKEN`

Set to `${{ secrets.GITHUB_TOKEN }}` to deploy to a `DEB_DISTRO-ROS_DISTRO`
branch in the same repo.

## ``SQUASH_HISTORY``

If set to true, all previous commits on the target branch will be discarded.
For example, if you are deploying a static site with lots of binary artifacts, this can help the repository becoming overly bloated.

## `VERBOSE`

Set to true to enable verbose builds.

## Example usage

```
uses: jspricke/ros-deb-builder-action@main
with:
  ROS_DISTRO: rolling
  DEB_DISTRO: jammy
  GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
