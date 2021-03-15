# opensuse tumbleweed repositories
/etc/zypp/repos.d

# crontab -e
DISPLAY=:0

MAILTO=root

*/30 * * * * /usr/bin/nice -n 19 /usr/bin/zypper --non-interactive-include-reboot-patches --no-gpg-checks dist-upgrade --recommends --replacefiles --force-resolution --auto-agree-with-licenses --allow-downgrade --allow-name-change --allow-vendor-change >> /dev/null
