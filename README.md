logcheck-rules
==============

My personal set of additional logcheck-rules.

This is designed as an overlay to /etc/logcheck/ignore.d.server on Debian.

To add the overlay (might overwrite existing files!):

```
git clone -n https://github.com/fabi125/logcheck-rules.git /tmp/logcheck
mv /tmp/logcheck/.git/ /etc/logcheck/ignore.d.server/
cd /etc/logcheck/ignore.d.server/
git reset HEAD
git checkout-index -af
rmdir /tmp/logcheck
```

To show all lines matching a rule file (those lines will be ignored by logcheck):
```
egrep -f rules /var/log/syslog
```

To show all lines not matching a rule file (those lines will be send via mail):
```
egrep -v -f rules /var/log/syslog
```
