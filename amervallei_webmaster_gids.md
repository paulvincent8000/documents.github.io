## Amervallei Webmaster Guide

![This is from the website.](https://usercontent.one/wp/amervallei.nl/wp-content/themes/genesis-sample/images/header.jpg)

## Backup and Recovery
The website is protected by two backup mechanisms: via the hosting provider and via an internal plug-in.

### Backup and Recovery via Hosting Provider
The hosting provider has a very solid backup and recovery system. Backups are made automatically every day and are retained for 14 days.

Manual backups can be made as desired and kept for unlimited time. To protect the site two items must be backed up at the same time:
- Database
- Files (Webruimte)

_Always make a manual backup before any major work on the site!_

Backup and recovery can be accessed via the [control panel][f9510030].
Instruction for use are available here:
[Backup en Herstel][4855723e].

  [4855723e]: https://help.one.com/hc/nl/articles/115005595365-Aan-de-slag-met-Back-up-herstel "Handleiding van One.com"
  [f9510030]: https://www.one.com/admin/backup.do "One.com Control Panel"

### Backup and Recovery via Wordpress
The Wordpress site is also backed up using a the plug-in [UpdraftPlus][428224c8].

  [428224c8]: https://wordpress.org/plugins/updraftplus/ "Updraft Plus Website"
Backup files are saved once per week to a folder in [Google Drive][46b5005a]. Recovery is done from the control panel in Wordpress. This backup option is simple to use and accessible, but less robust than a backup via the hosting provider as it cannot be easily used if the site becomes inaccessible.

  [46b5005a]: https://drive.google.com/drive/u/1/folders/1Ia0dseuPkpZK-nHOS6T1zBpj2leVo2i3 "Google Drive - Updraft Plus Backup Folder"
