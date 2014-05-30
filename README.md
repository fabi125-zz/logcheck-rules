logcheck-rules
==============

My personal set of additional logcheck-rules.

This is designed as an overlay to /etc/logcheck/ignore.d.server on Debian.

To add the overlay (might overwrite existing files!):

```
git clone -n https://github.com/fabi125/logcheck-rules /tmp/logcheck
mv /tmp/logcheck/.git/ /etc/logcheck/ignore.d.server/
cd /etc/logcheck/ignore.d.server/
git reset HEAD
git checkout-index -af
rmdir /tmp/logcheck
```
