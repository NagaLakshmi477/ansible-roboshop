modules:
============
mongodb:
--------
copy
service
replace
dnf

catalogue:
---------
command
dnf
user
file
unarchieve
npm
systemd_service
service
command

redis:
-----
command
dnf
replace
lineinfile

cart:
------
command
dnf
user
file
unarchieve
npm
copy
systemd_service
service

mysql:
-----
command
dnf
service

frontend:
--------


user:
------
command
dnf
user
file
unarchieve
npm
copy
systemd_service
service
cart:
------
command
dnf
user
file
unarchieve
npm
copy
systemd_service
service




