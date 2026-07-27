# github_merge_queue_talk

Notes and demo material for a short talk on the GitHub merge queue.

## Talk overview

The GitHub merge queue lets multiple approved pull requests be merged into a
protected branch safely and quickly, without requiring every author to
rebase on top of each other by hand. Each pull request is tested against the
latest version of the target branch, together with any other pull requests
already ahead of it in the queue, before it is allowed to merge.

## Agenda

The problem with direct merges and stacked pull requests
How the merge queue works under the hood
Real world examples from busy shared repositories
A short live demo of two competing pull requests
Questions and discussion

## Why a merge queue

Without a merge queue, a pull request is usually only tested against the
target branch as it looked when the check last ran. If several pull
requests merge in quick succession, later ones may never be retested
against everything that landed just before them. A merge queue closes
that gap by always testing against the true, up to date state of the
target branch plus any queued changes ahead of it.

## Real world examples

Large shared repositories with many active contributors see dozens of
pull requests approved per day. Without a merge queue, teams often fall
back to a single release manager manually rebasing and merging one
change at a time, which quickly becomes a bottleneck as the team grows.
