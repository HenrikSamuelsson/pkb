---
tags: git/submodule
---
# Git Submodule Removal

If a submodule in a project is not used so should it be removed to keep the project clean. Assuming a recent (2022) version of Git so can the submodule be removed using the following command:

```txt
git rm <path-to-submodule>
```

This will removes the entire submodule file tree, as well as remove the submodule's entry in the `.gitmodule` file. Meaning that all traces of the submodule in the projects git repository.

When testing the command it seemed that Git automatically staged the changes and all that was left to do was to make a commit of the changes.
