## Patching
1. Convert stash to patch file using the command `git stash show "stash@{0}" -p > patch`
2. Apply the patch file using the command `git apply /path/to/patch/file`

### Errors:
*1. No valid patches in input (allow with "--allow-empty")*
The encoding of the patch file might be different (eg: `UTF-16 LE`), save the patch file in `utf-8` encoding

*2. patch does not apply*
In this case, try to add `--ignore-whitespace` option
```
git apply --ignore-whitespace /path/to/patch/file
```
