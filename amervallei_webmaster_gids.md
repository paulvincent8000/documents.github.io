# Amervallei Webmaster Guide

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

## Major Changes and Development Offline
To avoid risk of disruption to the live website all major changes and new developments are carried out and tested in separate places. Work on the live site is limited to managing content and members.
### Staging
Staging is particularly useful for testing updates before they are applied to the live website.

A copy of the entire website is made to a stage. Changes are carried out on the copy and tested. The website is then copied from the stage to replace the live website. The stage is then deleted. If work on the staging site does not function as desired the stage can be replaced or deleted without affecting the live website.


>  _Warning!_
>  - _Always make a manual backup before major work, even when using the staging option_
>  - _Make sure users are not active on the live site as their work may be overwritten_
>  - _Delete the staging site after use to limit security risks_

Staging is set up from the Wordpress dashboard using a plug-in:  [instructions for use][898b4463].

  [898b4463]: https://help.one.com/hc/nl/articles/360000020617-Gebruik-de-One-com-Staging-plugin-voor-WordPress "One.com Staging"
### Development Sites (Speeltuin)
For major development or extensive evaluation of new plug-ins a completely separate site can be preferable to staging. This allows work to be done in a completely separate database and file system, which can simply be shut down when no longer required. A clone of the live website can be made using the plug-in [Duplicator Pro][a28e4407].

[a28e4407]: https://snapcreek.com/duplicator/docs/ "Duplicator Pro Documentation"

## Membership Access
Sensitive personal information and premium content is only available to authorised members after login.

Access restrictions can be applied at different levels:
- Entire Site _(not in use)_
- Entire Pages & Menu Items _(e.g. member pages)_
- Blog Posts & Events
- Selected Content _(e.g. event photos, newsletter content)_

It is possible to assign privileges to different roles. This is not currently used.
> Note: do not grant access to secure content to the *Customer* role.

## Other Security Measures
Further measures taken to protect website security include:
- A [firewall][fd957733] to protect from hackers and spam
- Use of [SSL][2f291dea] to encrypt traffic to and from the website
- Contact form protection agains spam with a [Honeypot][60c79bfc] and challenge question
- Avoid use of Email addresses (and encode them against robots where used)
- Users are prompted to create strong passwords
- Ensure knowledge is spread across multiple webmasters and documented.

  [fd957733]: https://wordpress.org/plugins/wordfence/ "Wordfence"
  [2f291dea]: https://really-simple-ssl.com/knowledge-base-overview/ "Really Simple SSL Plug-in"
  [60c79bfc]: http://www.nocean.ca/plugins/honeypot-module-for-contact-form-7-wordpress-plugin/ "Honeypot Plug-in"

## Register New Members
Members can register via the web shop, where they have the option to enrol for the brewing course or sign up for membership. The web shop handles the full transaction, including payment by Ideal. A notification is sent by e-mail to the treasurer and webmaster. Membership must be confirmed as described in the next section.

### Confirmation of membership
New members create a user account on the website as part of the registration process and are automatically assigned the user role _Customer_. This user account is created before proceeding to checkout and remains in place even if payment is not successfully completed. The user role _Customer_ does not have access to secure content on the website. In order to grant access the new membership must be manually confirmed by changing the user role from _Customer_ to _Subscriber_.

Confirm Membership from the member directory:
```
1. Login to the Website
2. Follow the menu to: Mijn Amervallei > Leden
3. Search for the new member
4. Open user profil (Profiel Bewerken)
5. Change user role to Subscriber (Gebruikersrollen)
6. Click Update Profile button to confirm and close
7. Log off when finished
```
> Administrators: This change can also be made from the user menu in the administration console. Under 'Rol' change user from 'Klant' to 'Abonnee'.

### Brewing Course Information and Pricing
The brewing course and new memberships are sold as products in the web shop. Details of each year's course and any price changes should be made to these products rather than in the site pages directly. Products can be added and modified in the products section of the administrator dashboard.
## Publish Newsletter
Newsletters are published as Posts (Berichten). Assign the category Newsletter to ensure they will appear on the sidebar of the home page.
## Publish Events
Events are posted from the Events section of the administrators dashboard. Current and future events will appear on the front page in chronological order.

## Minor Updates (e.g. plug-ins)
1. Enure backup is available from host
   Backups are automatically made each day. If no activity has taken place on the site then the backup from the previous day will be available.
2. Create staging Site
3. Update one plug-in on the staging Site
4. If the update is successful then update the same plug-in on the live site. The staging site is available to fall back on if needed. Otherwise re-build the staging site again and try updating a different plug-in.
4. Repeat this process one plug-in at a time until all updates have been successfully carried out.
5. If updates on the live site are successful then delete the staging site. Otherwise copy the staging site to live and test. It may be necessary to update the permalinks after a staging site has been copied to live. Then delete the staging site.

##  User Roles
WordPress provides the following roles:
- Administrator (slug: ‘administrator’) – somebody who has access to all the administration features within a single site.
- Editor (slug: ‘editor’) – somebody who can publish and manage posts including the posts of other users.
- Author  (slug: ‘author’)  – somebody who can publish and manage their own posts.
- Contributor (slug: ‘contributor’) – somebody who can write and manage their own posts but cannot publish them.
- Subscriber (slug: ‘subscriber’) – somebody who can only manage their profile.
[WordPress Roles](https://wordpress.org/support/article/roles-and-capabilities/)
