# github_merge_queue_talk

Notes and demo material for a short talk on the GitHub merge queue.

## Talk overview

The GitHub merge queue lets multiple approved pull requests be merged into a
protected branch safely and quickly, without requiring every author to
rebase on top of each other by hand. Each pull request is tested against the
latest version of the target branch, together with any other pull requests
already ahead of it in the queue, before it is allowed to merge.
