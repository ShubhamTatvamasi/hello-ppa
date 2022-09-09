# hello-ppa

Generate change logs:
```bash
dch -i --create
```

Build deb file:
```bash
sudo debuild -uc -us -S -sa \
  -k"shubhamtatvamasi@gmail.com" \
  -p"gpg --batch --passphrase "" --pinentry-mode loopback"

debsign ../*.changes \
  -k"shubhamtatvamasi@gmail.com" \
  -p"gpg --batch --passphrase "" --pinentry-mode loopback"
```

Upload:
```bash
dput --unchecked ppa:shubhamtatvamasi/helloworld ../*.changes
```

Add PPA repo:
```bash
sudo add-apt-repository --yes ppa:shubhamtatvamasi/helloworld
```

Install helloworld package:
```bash
sudo apt install helloworld
```

https://launchpad.net/~shubhamtatvamasi/+archive/ubuntu/helloworld


Reference:
https://www.debian.org/doc/manuals/maint-guide/dreq.en.html


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
