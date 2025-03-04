# Release notes

**Release date: 2025-03-XX**  
**Release no.: 2024/Q4**  
**Release tag: 4.0.0**

OS2forms has been cleaned up, as agreed with the OS2forms coordination group in the fall of 2024\.

This release primarily consists of a number of modules that have been removed from OS2forms, as they have either never been used or are no longer in use. In addition, a few new modules have been added, as requested by the OS2forms coordination group.

There are also some modules that Bellcom and the OS2forms coordination group had agreed should be removed, but which have not been removed. In the list below you can see which ones \- and why they have not been removed. Some of them we had overlooked were core modules (they were not placed in the core group), while others have some dependencies that we need to investigate further. Based on a precautionary principle, they have therefore not been removed in this release.

In addition, a single module from ITK has been added, which is not on the list of modules in the central maintenance agreement. It is the module OS2web Audit (os2web\_audit) \- link to readme: [https://github.com/OS2web/os2web\_audit/blob/develop/README.md](https://github.com/OS2web/os2web_audit/blob/develop/README.md).

**Modules that have been added:**

* OS2Forms Fasit (os2forms\_fasit) \- link to documentation: [https://github.com/OS2Forms/os2forms/blob/8a4d1ec8d4efaa2783accac51bf60be54f182f97/modules/os2forms\_fasit/docs/BENYTTELSE.md](https://github.com/OS2Forms/os2forms/blob/8a4d1ec8d4efaa2783accac51bf60be54f182f97/modules/os2forms_fasit/docs/BENYTTELSE.md)  
* FBS Handler (os2forms\_fbs\_handler) \- we can't find any link to documentation or readme on this module.

**Modules that have been removed:**

* Active Directory Integration / LDAP Integration \- NTLM & Kerberos Login (ldap\_auth)  
* Advanced Link (editor\_advanced\_link)  
* Checklist API Example (checklistapiexample)  
* Chosen (chosen)  
* Chosen Field (chosen\_field)  
* Chosen Library (chosen\_lib)  
* CKEditor Accessibility Checker (ckeditor\_a11ychecker)  
* CKEditor Balloon Panel (ckeditor\_balloonpanel)  
* CKEditor Entity Link (ckeditor\_entity\_link)  
* Configuration Filter (config\_filter)  
* Crop API (crop)  
* Date Popup (date\_popup)  
* Drupal Upgrade (migrate\_upgrade)  
* Easy Breadcrumb (easy\_breadcrumb)  
* Email Logging and Alerts (emaillog)  
* Entity (entity)  
* Entity Browser (entity\_browser)  
* Entity Browser example (entity\_browser\_example)  
* Entity Browser IEF (entity\_browser\_entity\_form)  
* Entity Embed (entity\_embed)  
* Environment indicator (environment\_indicator)  
* Environment indicator UI (environment\_indicator\_ui)  
* Field Color (field\_color)  
* Field Group (field\_group)  
* Field Group Migrate (field\_group\_migrate)  
* Header and Footer Scripts (header\_and\_footer\_scripts)  
* ImageWidgetCrop (image\_widget\_crop)  
* ImageWidgetCrop examples (image\_widget\_crop\_examples)  
* Inline Entity Form (inline\_entity\_form)  
* Linkit (linkit)  
* Maillog / Mail Developer (maillog)  
* Media entity crop (crop\_media\_entity)  
* Metatag (metatag)  
* Metatag Custom Routes (Paths) (metatag\_routes)  
* Metatag Extended Permissions (metatag\_extended\_perms)  
* Metatag: App Links (metatag\_app\_links)  
* Metatag: Dublin Core (metatag\_dc)  
* Metatag: Dublin Core Advanced (metatag\_dc\_advanced)  
* Metatag: Facebook (metatag\_facebook)  
* Metatag: Favicons (metatag\_favicons)  
* Metatag: Google Custom Search Engine (CSE) (metatag\_google\_cse)  
* Metatag: Google Plus (metatag\_google\_plus)  
* Metatag: Hreflang (metatag\_hreflang)  
* Metatag: Mobile & UI Adjustments (metatag\_mobile)  
* Metatag: Open Graph (metatag\_open\_graph)  
* Metatag: Open Graph Products (metatag\_open\_graph\_products)  
* Metatag: Page Manager (metatag\_page\_manager)  
* Metatag: Pinterest (metatag\_pinterest)  
* Metatag: Twitter Cards (metatag\_twitter\_cards)  
* Metatag: Verification (metatag\_verification)  
* Metatag: Views (metatag\_views)  
* Migrate Advanced Example Setup (migrate\_example\_advanced\_setup)  
* Migrate Example (Advanced) (migrate\_example\_advanced)  
* Migrate Example (migrate\_example)  
* Migrate Example Setup (migrate\_example\_setup)  
* Migrate JSON Example (migrate\_json\_example)  
* Migrate Plus (migrate\_plus)  
* Migrate Tools (migrate\_tools)  
* OS2forms Declaration of Consent (os2forms\_consent)  
* OS2Forms SimpleSAML Checklist (os2web\_simplesaml\_checklist)  
* Paragraphs (paragraphs)  
* Paragraphs Demo (paragraphs\_demo)  
* Paragraphs Library (paragraphs\_library)  
* Paragraphs Type Permissions (paragraphs\_type\_permissions)  
* Scheduler (scheduler)  
* Scheduler Rules Integration (scheduler\_rules\_integration)  
* Simple LDAP (simple\_ldap)  
* Simple LDAP SSO (simple\_ldap\_sso)  
* Simple LDAP User (simple\_ldap\_user)  
* starterkit\_theme (starterkit\_theme)  
* Web Server Logging and Alerts (errorlog)  
* White darkblue theme (white\_darkblue)

**Modules that were agreed to be removed but have not been removed:**

* Clientside Validation (clientside\_validation) – required by “Webforms” and “OS2forms”  
* Clientside Validation Demo (clientside\_validation\_demo) – required by “Webforms” and “OS2forms”  
* Clientside Validation jQuery (clientside\_validation\_jquery) – required by “Webforms” and “OS2forms”  
* Drupal Roles Authorization consumer (authorization\_drupal\_roles) – required by “LDAP”  
* Embed (embed) – required by ”OS2forms”  
* Entity Mask (ctools\_entity\_mask) – required by ”ImageWidgetCrop”  
* Migrate (migrate) – is part of Drupal core, so it cannot be removed  
* Migrate Drupal (migrate\_drupal) – is part of Drupal core, so it cannot be removed  
* Migrate Drupal UI (migrate\_drupal\_ui) – is part of Drupal core, so it cannot be removed  
* Redirect 404 (redirect\_404) – required by ”OS2forms”  
* Redirect Domain (redirect\_domain) – required by ”OS2forms”  
* Views Revisions (views\_revisions) – required by ”OS2forms”  
* Webform iCheck (webform\_icheck) – is part of Webforms, so it cannot be removed  
* Webform jQueryUI Buttons (webform\_jqueryui\_buttons) – is part of Webforms, so it cannot be removed  
* Webform Location Geocomplete (webform\_location\_geocomplete) – is part of Webforms, so it cannot be removed  
* Webform Toggles (webform\_toggles) – is part of Webforms, so it cannot be removed