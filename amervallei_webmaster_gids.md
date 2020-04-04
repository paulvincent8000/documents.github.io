## Amervallei Webmaster Guide

![This is from the website.](https://usercontent.one/wp/amervallei.nl/wp-content/themes/genesis-sample/images/header.jpg)

## Backup and Recovery
Reliable backups ensure the website can be recovered in the event of disaster. The website is protected by two backup mechanisms: via the hosting provider and via an internal plug-in.

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

### Staging
Staging avoids the risk of downtime by allowing major changes to be tested before they are applied to the live website.

A copy of the entire website is made to a stage. Changes are carried out on the copy and tested. The website is then copied from the stage to replace the live website. The stage is then deleted. If work on the staging site does not function as desired the stage can be replaced or deleted without affecting the live website.


>  _Warning!_
>  - _Always make a manual backup before major work, even when using the staging option_
>  - _Make sure users are not active on the live site as their work may be overwritten_
>  - _Delete the staging site after use to limit security risks_

Staging is set up from the Wordpress dashboard using a plug-in:  [instructions for use][898b4463].

  [898b4463]: https://help.one.com/hc/nl/articles/360000020617-Gebruik-de-One-com-Staging-plugin-voor-WordPress "One.com Staging"
