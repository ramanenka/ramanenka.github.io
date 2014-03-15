---
layout: post
title:  "Create a zip with files that were changed in a specific commit."
date:   2013-10-01 19:35:40
---
To create an archive that contains files changed in a specific commit you may use the following command:

```bash
export COMMIT_HASH=1ae404a0cbe5
git archive -o ../$COMMIT_HASH.zip $COMMIT_HASH `git diff-tree --no-commit-id --name-only -r $COMMIT_HASH`
```
