<!--
N.B.: This README was automatically generated by https://github.com/YunoHost/apps/tree/master/tools/README-generator
It shall NOT be edited by hand.
-->
⚠️ This is a fork (work in progress) of the official Prosody app to install on Yunohost 12 and aiming at providing the best XMPP support possible!

⚠️⚠️ This branch/repository is not maintained anymore, please use https://github.com/YunoHost-Apps/prosody_ynh/tree/testing and soon https://github.com/YunoHost-Apps/prosody_ynh/ !

🚀 Target is to provide at least:
  * A/V calls (https://github.com/YunoHost/issues/issues/1607) 
  * BOSH (https://forum.yunohost.org/t/unable-to-set-up-bosh-conf-nginx/12995)
  * invite links (if not covered by https://github.com/YunoHost/issues/issues/1677)
  * File sharing for all usual filetypes (https://forum.yunohost.org/t/metronome-mime-types-for-metronome-again/20073)

...and ultimately an Advanced Server compliance level (https://xmpp.org/extensions/xep-0479.html).

✅ What works:
  * install on brand new Yunohost 12
  * LDAP auth
  * A/V calls
  * File upload (broken as of 11/2024)
  * MUC
  * automatically install coturn if not yet present (https://github.com/anubister/coturn_ynh/ , a fork compatible with Yunohost 12)
  * XEP-0163, XEP-0191, XEP-0215, XEP-0237, XEP-0280, XEP-0313, XEP-0363 (see 'xmpp_compliance' file)
    
🐞 What does not work:
  * vjud (Users directory) (help welcomed!)
    
🙋 TODO (help welcomed!):
  * do migration from Metronome datas on Yunohost 11 to Prosody
  * if applicable manage migration from upstream version of coturn app
  * usability by other apps:
    * [PeerTube](https://github.com/YunoHost-Apps/peertube_ynh): to be tested
    * [Movim](https://github.com/YunoHost-Apps/movim_ynh): app broken?
    * [Converse.js](https://github.com/YunoHost-Apps/converse_ynh): seems to work
    * [Jitsi](https://github.com/YunoHost-Apps/jitsi_ynh): to be tested
    * [Nextcloud](https://github.com/YunoHost-Apps/nextcloud_ynh): to be tested
    * [Libervia](https://salut-a-toi.org/): to be tested [non-working app](https://github.com/YunoHost-Apps/sat_ynh)
    * ...?
  * check initial configuration (subdomains available, DNS, ?) : inform or block?
  * update scripts/remove and others...
  * check app score

# READ before install!
Ideally all the README :) but this in particular:
* Ensure you are already running Yunohost 12 (or higher, but not 11), and metronome app is not installed (TBC with data migration logic)
* You must create in Yunohost the subdomains `muc.` and `xmpp-upload.`
* You must apply the workaround for this bug : https://github.com/anubister/prosody_ynh/issues/4#issuecomment-2318658501


💬 Further discussions, support on xmpp:yunohost-xmpp@muc.chapril.org?join
Or in the [forum](https://forum.yunohost.org/c/apps/11).

ℹ️ About this branch 
  * This branch build from source prosody (compilation on server-side) and retrieve 2 modules from prosody servers. It installs on your desired (sub)domain selected during the installation.
  * This branch is **depreciated/not maintained**, use at your own risk or contribute to it!

# Prosody for YunoHost

[![Integration level](https://dash.yunohost.org/integration/prosody.svg)](https://dash.yunohost.org/appci/app/prosody) ![Working status](https://ci-apps.yunohost.org/ci/badges/prosody.status.svg) ![Maintenance status](https://ci-apps.yunohost.org/ci/badges/prosody.maintain.svg)

[![Install Prosody with YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=prosody)

*[Lire ce readme en français.](./README_fr.md)*

> *This package allows you to install Prosody quickly and simply on a YunoHost server.
If you don't have YunoHost, please consult [the guide](https://yunohost.org/#/install) to learn how to install it.*

## Overview

Prosody is a modern XMPP communication server. It aims to be easy to set up and configure, and efficient with system resources. Additionally, for developers it aims to be easy to extend and give a flexible system on which to rapidly develop added functionality, or prototype new protocols.


**Shipped version:** 0.12.4~ynh10
## Documentation and resources

* Official app website: <https://prosody.im/>
* Official admin documentation: <https://prosody.im/doc>
* Upstream app code repository: <https://hg.prosody.im/>
* YunoHost Store: <https://apps.yunohost.org/app/prosody>
* Report a bug: <https://github.com/YunoHost-Apps/prosody_ynh/issues>

## Developer info

Please send your pull request to the [testing branch](https://github.com/YunoHost-Apps/prosody_ynh/tree/testing).

To try the testing branch, please proceed like that.

``` bash
sudo yunohost app install https://github.com/YunoHost-Apps/prosody_ynh/tree/testing --debug
or
sudo yunohost app upgrade prosody -u https://github.com/YunoHost-Apps/prosody_ynh/tree/testing --debug
```

**More info regarding app packaging:** <https://yunohost.org/packaging_apps>
