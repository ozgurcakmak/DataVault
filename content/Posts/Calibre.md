#software #linux #troubleshooting 

## `ebook-convert` tool
When we install this tool with [[Aurora Linux]] , it installs the flatpak version. This version does not let us easily access to this utility. To run it successfully:

```bash
flatpak run --command=ebook-convert com.calibre_ebook.calibre input.mobi output.epub
```

However this is a handful. To do it better we can assign an alias:

```bash
alias ebook-convert='flatpak run --command=ebook-convert com.calibre_ebook.calibre'
```

Now we can run it as usual:
```bash
ebook-convert test.mobi test.epub
```

### Batch conversion
```bash
for f in *.mobi; do ebook-convert "$f" "${f%.mobi}.epub"; done
```

