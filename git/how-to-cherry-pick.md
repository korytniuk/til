# How to apply a commit to another branch 

It's as simple as that using cherry-picking

```
git checkout a_branch_you_want_to_apply_changes_to
git cherry-pick hash_commit
```

`-edit` command can be used to edit a commit massage before applying cherry-picking
