# hello-ppa

Build deb file:
```bash
debuild -k0F195430352D314080C96E67B76BE3858E1FDB4F
```

Upload:
```bash
dput ppa:shubhamtatvamasi/helloworld ../*.changes
```

https://launchpad.net/~shubhamtatvamasi/+archive/ubuntu/helloworld


Reference:
https://www.debian.org/doc/manuals/maint-guide/dreq.en.html

changelog https://packaging.ubuntu.com/html/debian-dir-overview.html


### Multipass Setup

Create VM for development:
```bash
multipass launch focal \
  --name ppa \
  --disk 20G \
  --mem 2G \
  --cpus 2
```

Access VM:
```bash
multipass shell ppa
```

Delete the VM:
```bash
multipass delete ppa
multipass purge
```
