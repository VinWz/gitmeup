
# Configuration

# Staging
## Files permissions

Overall advice: **Use sparingly!** The less specific config items, the better for change and troubleshooting.

To set file permissions bits, in particularly if the file is already staged, do not use the FS permissions but update the Git index instead:

```git update-index --chmod=<perms> <FILE_PATH>```

To check the permissions bits:

``git ls-files -s [file[s]]``

To set permissions automagically on new files, use an attributes dotfile:

.gitattributes
```
*.sh text eol=lf executable
```

* [Mastering Permissions in Git: A Complete Guide to Adding chmod Modes in Your Repository](https://thelinuxcode.com/add-chmod-permissions-to-file-in-git/)
