# hello-ppa

Build deb file:
```bash
debuild -k0F195430352D314080C96E67B76BE3858E1FDB4F
```

Upload:
```bash
dput ppa:shubhamtatvamasi/hello ../*.changes
```

Reference:
https://www.debian.org/doc/manuals/maint-guide/dreq.en.html
