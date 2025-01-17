# pfSense-pkg-zerotier

pfSense 2.5.0 package to support zerotier.

## Pre-reqs
1. FreeBSD 12.2 Workstation with pkg, git, and gmake

## Build
1. `git clone https://github.com/pfsense/FreeBSD-ports.git`
2. add `ALLOW_UNSUPPORTED_SYSTEM=YES` to /etc/make.conf
3. Copy these files to FreeBSD-ports/net/pfSense-pkg-zerotier
4. Run `make clean ; make package`
5. scp work/pkg/pfSense-pkg-zerotier-0.00.1.txz to pfSense
6. `cd /usr/ports/net/zerotier/ && make package`
7. scp work/pkg/zerotier-1.6.4.txz to pfSense

## Install
1. Run `pkg add http://ftp.smejdil.cz/pfSense/pkg/zerotier-1.6.4.txz`
2. Run `pkg add http://ftp.smejdil.cz/pfSense/pkg/pfSense-pkg-zerotier-0.00.1.txz`

## Images

![pfSense VPN Zerotier Networks](./images/pfSense_VPN_Zerotier_Networks.png)

## ToDo
- [ ] Re-write controller functionality to match API changes
- [ ] Interface creation
