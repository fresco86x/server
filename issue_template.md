<!--
Thanks for reporting issues back to Nextcloud! This is the issue tracker of Nextcloud, if you have any support question please check out https://nextcloud.com/support

This is the bug tracker for the Server component. Find other components at https://github.com/nextcloud/

For reporting potential security issues please see https://nextcloud.com/security/

To make it possible for us to help you please fill out below information carefully.
--> 
### Steps to reproduce
1.
2.
3.

### Expected behaviour
Update 11.0.1

### Actual behaviour
The update fails with this error:

### Server configuration
**Operating system**:
PRETTY_NAME="Raspbian GNU/Linux 8 (jessie)"
NAME="Raspbian GNU/Linux"
VERSION_ID="8"
VERSION="8 (jessie)"
ID=raspbian
ID_LIKE=debian

**Web server:**
Package: apache2
Version: 2.4.25-3

**Database:**
Package: mysql-server
Source: mysql-5.5
Version: 5.5.54-0+deb8u1

**PHP version:**
Package: php7.0-fpm
Source: php7.0
Version: 7.0.14-2

**Nextcloud version:** (see Nextcloud admin page)
11.0.0

**Updated from an older Nextcloud/ownCloud or fresh install:**
update from 11.0.0

**Where did you install Nextcloud from:**
https://download.nextcloud.com

**Signing status:**
<details>
<summary>Signing status</summary>

```
I can't access the nextcloud
```
</details>

**List of activated apps:**
<details>
<summary>App list</summary>


```
:~# sudo -u www-data php occ app:list
Could not open input file: occ
```
</details>

**The content of config/config.php:**
<details>
<summary>Config report</summary>

```
If you have access to your command line run e.g.:
sudo -u www-data php occ config:list system
from within your Nextcloud installation folder

or 

<?php
$CONFIG = array (
  'instanceid' => 'XXX',
  'passwordsalt' => 'XXX',
  'secret' => 'XXX',
  'trusted_domains' =>
  array (
    0 => 'www.xxx.xxx',
  ),
  'datadirectory' => '/ext/nextcloud',
  'overwrite.cli.url' => 'www.xxx.xxx',
  'dbtype' => 'mysql',
  'version' => '11.0.0.10',
  'dbname' => '<dbname>',
  'dbhost' => 'localhost',
  'dbport' => '',
  'dbtableprefix' => 'oc_',
  'dbuser' => '<dbuser>',
  'dbpassword' => '<dbpw>',
  'logtimezone' => 'UTC',
  'installed' => true,
  'updater.secret' => 'XXX
  'maintenance' => false,
  'theme' => '',
  'loglevel' => 2,
);

</details>

**Are you using external storage, if yes which one:** local/smb/sftp/...
USB-Harddrive - /ext/nextcloud

**Are you using encryption:** yes/no
no

**Are you using an external user-backend, if yes which one:** LDAP/ActiveDirectory/Webdav/...
I don't think so..

#### LDAP configuration (delete this part if not used)
<details>
<summary>LDAP config</summary>

```
With access to your command line run e.g.:
sudo -u www-data php occ ldap:show-config
from within your Nextcloud installation folder

Without access to your command line download the data/owncloud.db to your local
computer or access your SQL server remotely and run the select query:
SELECT * FROM `oc_appconfig` WHERE `appid` = 'user_ldap';


Eventually replace sensitive data as the name/IP-address of your LDAP server or groups.
```
</details>

### Client configuration
**Browser:**
Firefox

**Operating system:**
Windows 10

### Logs
#### Web server error log
<details>
<summary>Web server error log</summary>

```
[Mon Feb 27 06:25:08.006870 2017] [ssl:warn] [pid 967:tid 1995448320] AH01909: 127.0.1.1:443:0 server certificate does NOT include an ID which matches the server name
[Mon Feb 27 06:25:08.008111 2017] [mpm_event:notice] [pid 967:tid 1995448320] AH00489: Apache/2.4.10 (Raspbian) OpenSSL/1.0.1t configured -- resuming normal operations
[Mon Feb 27 06:25:08.008172 2017] [core:notice] [pid 967:tid 1995448320] AH00094: Command line: '/usr/sbin/apache2'

```
</details>

#### Nextcloud log (data/nextcloud.log)
<details>
<summary>Nextcloud log</summary>

```
empty logfile!
```
</details>

#### Browser log
<details>
<summary>Browser log</summary>

```
Insert your browser log here, this could for example include:

a) The javascript console log
b) The network log
c) ...
```
</details>
