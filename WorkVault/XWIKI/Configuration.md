---
title: "Configuration (XWiki.org)"
source: "https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HEnablesuperadminaccount"
author:
published:
created: 2025-11-13
description: "Configuration"
tags:
---
## Configuration


**Contents**

- [Enable superadmin account](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HEnablesuperadminaccount)
- [Language settings](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HLanguagesettings)
	- [Algorithm](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HAlgorithm)
- [Date format](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDateformat)
- [Enabling/Disabling Statistics](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HEnabling2FDisablingStatistics)
- [Optional Store Features](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HOptionalStoreFeatures)
	- [Document versioning](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDocumentversioning)
	- [Document recycle bin](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDocumentrecyclebin)
	- [Attachment recycle bin](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HAttachmentrecyclebin)
- [Customizing error pages](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HCustomizingerrorpages)
- [Customizing the Skin](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HCustomizingtheSkin)
- [Security configuration](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSecurityconfiguration)
- [HTTPS/SSL](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HHTTPS2FSSL)
- [Customizing Menus](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HCustomizingMenus)
- [Encoding](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HEncoding)
- [User Authentication](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HUserAuthentication)
	- [Customizing the Verified Registration Page](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HCustomizingtheVerifiedRegistrationPage)
- [Default User Preferences](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDefaultUserPreferences)
- [Initial Groups](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HInitialGroups)
- [Logging](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HLogging)
- [Configuring Interwiki links](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HConfiguringInterwikilinks)
	- [Interwiki links (XWiki Syntax 1.0)](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HInterwikilinks28XWikiSyntax1.029)
	- [Interwiki links (XWiki Syntax 2.x)](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HInterwikilinks28XWikiSyntax2.x29)
- [Link URLs](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HLinkURLs)
	- [Reverse proxy setup](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HReverseproxysetup)
	- [Short URLs](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HShortURLs)
- [Configure the names of database schemas](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HConfigurethenamesofdatabaseschemas)
- [Controlling Page Tabs](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HControllingPageTabs)
- [Configure "Version Summary" behavior](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HConfigure22VersionSummary22behavior)
- [Configuring Directories](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HConfiguringDirectories)
	- [Permanent Directory](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HPermanentDirectory)
	- [Temporary Directory](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HTemporaryDirectory)
- [Configuring WebDAV (since 1.7)](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HConfiguringWebDAV28since1.729)
	- [Securing WebDAV Server](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSecuringWebDAVServer)
	- [Disabling WebDAV](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDisablingWebDAV)
- [Redirections](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HRedirections)
	- [Trusted domains](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HTrusteddomains)
- [Customizing the PDF export Look & Feel](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HCustomizingthePDFexportLook26Feel)
	- [General Architecture](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HGeneralArchitecture)
	- [Override the PDF Templates](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HOverridethePDFTemplates)
		- [Customize the PDF Footer](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HCustomizethePDFFooter)
		- [Customize the PDF Cover](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HCustomizethePDFCover)
		- [Override the CSS rules](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HOverridetheCSSrules)
		- [Override the xhtml2fo.xsl rules](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HOverridethexhtml2fo.xslrules)
		- [Debugging PDF export](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDebuggingPDFexport)
- [Configuring Wiki Syntaxes and default Syntax](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HConfiguringWikiSyntaxesanddefaultSyntax)
- [Title behavior](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HTitlebehavior)
- [Link Label Generation](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HLinkLabelGeneration)
- [Rendering Cache](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HRenderingCache)
- [Allowed Pages for Inactive Users](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HAllowedPagesforInactiveUsers)
- [Rendering Transformations](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HRenderingTransformations)
- [Macros categories and visibility](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HMacroscategoriesandvisibility)
- [Securing Groovy Scripts](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSecuringGroovyScripts)
- [Lock Duration](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HLockDuration)
- [Editing](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HEditing)
	- [Default editor](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDefaulteditor)
	- [Default WYSIWYG editor](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDefaultWYSIWYGeditor)
	- [Section Editing](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSectionEditing)
	- [Editing Conflicts](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HEditingConflicts)
	- [In-place Editing](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HIn-placeEditing-3)
- [Delete Pages](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDeletePages-3)
	- [Enabling Advanced users to skip the recycle bin](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HEnablingAdvanceduserstoskiptherecyclebin-3)
- [Readonly](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HReadonly-3)
- [Sample xwiki.cfg](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSamplexwiki.cfg-3)
- [Sample xwiki.properties](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSamplexwiki.properties-3)
	- [In-place Editing](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HIn-placeEditing)
- [Delete Pages](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDeletePages)
	- [Enabling Advanced users to skip the recycle bin](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HEnablingAdvanceduserstoskiptherecyclebin)
- [Readonly](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HReadonly)
- [Sample xwiki.cfg](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSamplexwiki.cfg)
- [Sample xwiki.properties](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSamplexwiki.properties)
	- [In-place Editing](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HIn-placeEditing-1)
- [Delete Pages](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDeletePages-1)
	- [Enabling Advanced users to skip the recycle bin](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HEnablingAdvanceduserstoskiptherecyclebin-1)
- [Readonly](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HReadonly-1)
- [Sample xwiki.cfg](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSamplexwiki.cfg-1)
- [Sample xwiki.properties](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSamplexwiki.properties-1)
	- [In-place Editing](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HIn-placeEditing-2)
- [Delete Pages](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDeletePages-2)
	- [Enabling Advanced users to skip the recycle bin](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HEnablingAdvanceduserstoskiptherecyclebin-2)
- [Readonly](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HReadonly-2)
- [Sample xwiki.cfg](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSamplexwiki.cfg-2)
- [Sample xwiki.properties](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSamplexwiki.properties-2)

Once you have XWiki [installed](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Installation/) you'll want to configure it. Configuration can be done in 2 ways:

- by stopping the XWiki instance and editing either the xwiki/WEB-INF/xwiki.cfg file or the xwiki/WEB-INF/xwiki.properties one, and then restarting XWiki. Note that xwiki.cfg was the historical file containing the configuration option, but we're moving away from it, and in due time, all the XWiki configuration options will be found in xwiki.properties
- by logging in as a user with admin rights and going to the administration page using the top level menu. You can also go directly to *http://localhost:8080/xwiki/bin/admin/XWiki/XWikiPreferences*. This allows the server to keep running while making the changes.
	- Some configurations are only accessible from the xwiki.cfg and xwiki.properties files and have no equivalent on the administration page.
	- If you're a developer and need to understand how Configuration works in XWiki, check the [Configuration Module Documentation](https://extensions.xwiki.org/xwiki/bin/view/Extension/Configuration%20Module).
	You can verify some basic settings of your XWiki installation (on Tomcat, MySQL) using the [Check Config and Indexes application](https://extensions.xwiki.org/xwiki/bin/view/Extension/Check%20Config%20And%20Indexes%20Application).

There are various things you can configure:

## Enable superadmin account

Edit the xwiki.cfg file and enable the xwiki.superadminpassword property. For example:

```
# Enable to allow superadmin. It is disabled by default as this could be a security breach if
# it were set and you forgot about it.
xwiki.superadminpassword=system
```

When logging in, the username will be "superadmin" and the password will be the one you set in the xwiki.superadminpassword property.

## Language settings

To define the default language for your wiki, go to the administration page, click on "Localization", locate the "Default Language" field and select the language you wish to use.

In addition, you can configure your wiki to be multilingual. See the [I18 user page](https://www.xwiki.org/xwiki/bin/view/Documentation/UserGuide/Features/I18N) for more information.

Last, you can force your wiki to display only in one of the languages specified in the settings by editing your WEB-INF/xwiki.cfg file. Search for the "Internationalization" section, and you should see two commented settings that you can uncomment to fix their value (1 means true, 0 - false).

```
#-# By default, XWiki chooses the language specified by the client (browser) in the Accept-Language HTTP header. This
#-# allows to use the default language of the wiki when the user didn't manually choose a language.
# xwiki.language.preferDefault=0

#-# Force only one of the supported languages to be accepted. Default is true.
# xwiki.language.forceSupported=1
```

Since XWiki 11.2+ the option xwiki.language.forceSupported is by default set to true. The option was by default set to false on prior versions.

## Algorithm

The algorithm to find the locale to use is the following, in this order:

- If the wiki is not multilingual use the wiki default locale (default\_language xproperty in XWikiPreferences xobject or English if not found).
- If the wiki is multilingual
	- Try to get the locale passed in the request (looking for a language query string parameter).
	- If the language value is default use the wiki default locale. If a parameter is found, it sets a language cookie to remember the language in use.
	- Try to get the locale from the language cookie
	- If the default language is preferred (xwiki.language.preferDefault from xwiki.cfg or preferDefaultLanguage property from the space preferences (WebPreferences xobject) or wiki preferences (XWikiPreferences xobject})), and since the user didn't explicitly ask for a language already, then use the wiki default locale.
	- Try to use the browser's Accept-Language header sent in HTTP request.
	- Fallback to the wiki default locale

In addition, the xwiki.language.forceSupported configuration property (editable in xwiki.cfg) is enabled by default. It means that if at any step above the locale found is not in the list of supported locales, then the locale is not set and the algorithm moves to the next step.

## Date format

To define the date format used in the interfaces, go to *Wiki -> Administer Wiki -> Localization*, locate the "Date format" field and enter the date format you wish to use. Examples:

| Format | Result |
| --- | --- |
| MMMM dd, HH:mm | January 27, 12:27 |
| yyyy/MM/dd, HH:mm | 2009/01/27, 12:27 |
| dd/MM/yyyy, HH:mm | 27/01/2009, 12:27 |

[More information about date formatting](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/text/SimpleDateFormat.html).

## Enabling/Disabling Statistics

To disable [the Statistics feature](https://extensions.xwiki.org/xwiki/bin/view/Extension/Statistics%20Application), edit your xwiki.cfg file and replace the following properties as shown here (to enable statistics, change 0 to 1):

```
xwiki.stats=0
xwiki.stats.default=0
```

where:

- xwiki.stats controls whether statistics are on or off
- xwiki.stats.default controls whether statistics are on or off by default for the current Wiki. This is useful in [multi wiki mode](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Virtualization/). A wiki can decide whether statistics are on or off by setting the "statistics" field in XWiki.XWikiPreferences. If no such field is defined, then the default value xwiki.stats.default is used.
	There's no UI to set the statistics on or off for a given subwiki. Thus at the moment you'll need to do 2 things:
	- Edit XWiki.XWikiPreferences to add a new boolean property to the class, by going to *http://localhost:8080/xwiki/bin/edit/XWiki/XWikiPreferences?editor=class*
	- Set the statistics property to true by going to *http://localhost:8080/xwiki/bin/edit/XWiki/XWikiPreferences?editor=object* and setting the statistics property to true

## Optional Store Features

## Document versioning

One of the key features of a wiki engine is the ability to keep all the history of a document, allowing users to see the evolution of a document and revert changes. However, the history of an active wiki continuously grows and is usually much larger than the data version. It is possible to disable the versioning feature in XWiki, meaning less storage space will be used, although it will not be possible to revert the document in case of vandalism.

To disable versioning, edit xwiki.cfg and add `xwiki.store.versioning=0`.

[Attachment versioning](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Attachments#HVersions) is also available and turned on by default.

## Document recycle bin

By default, deleted documents are not permanently removed, but are placed in a recycle bin, from which they can later be removed or restored. To disable it, edit xwiki.cfg and add `xwiki.recyclebin=0`.

Disabling the recycle bin will make it impossible to restore a deleted document, unless a database backup is available.

## Attachment recycle bin

See the [Attachment recycle bin](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Attachments#HDeletion).

## Customizing error pages

When an error occurs, the screen displayed to the user can be easily customized without modifying the skin in the following cases: when the wiki, document or attachment that is currently looked for does not exist, or when a denied access occurs. You need to create the following respective pages in your wiki:

- XWiki.WikiDoesNotExist,
- XWiki.DocumentDoesNotExist,
- XWiki.AttachmentDoesNotExist,
- XWiki.AccessDenied

Creating these pages rather than editing the skin's velocity files will save you time during upgrades since you won't need to merge the possibly updated skin files with yours.

## Customizing the Skin

See the [Skin Guide](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Skins).

## Security configuration

See the [Security Guide](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Security).

## HTTPS/SSL

By default, the protocol to use to generate external URLs (HTTPS, HTTP) is extracted from requests to XWiki, so most of the time you don't have anything to do if you properly configure your proxy, but it's possible to force a specific protocol using xwiki.url.protocol property in xwiki.cfg.

To set up HTTPS/SSL, you may need to configure your Servlet Container and any front-end web server or proxy in front of XWiki. For example:

- [Tomcat](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Installation/InstallationWAR/InstallationTomcat/)
- [Jetty](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Installation/InstallationWAR/InstallationJetty/)

## Customizing Menus

The first thing to understand is that menus depend on the skin you're using. If you're using the 1.0 skin you're likely using the [Panels Application](https://extensions.xwiki.org/xwiki/bin/view/Extension/Panels%20Application) to provide the different menu panels you see on the left or right of your wikis. Check the [Panels Application](https://extensions.xwiki.org/xwiki/bin/view/Extension/Panels%20Application) to know more on how to configure/modify them.

## Encoding

See the [Encoding Guide](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/Encoding/).

## User Authentication

See the [Authentication Guide](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Authentication/).

## Customizing the Verified Registration Page

The Verified Registration Page is part of the [Administration Application](https://extensions.xwiki.org/xwiki/bin/view/Extension/Administration%20Application). It allows you to require users to fill in a captcha and validates user input on both the server side and the client side using Javascript. The configuration allows you to add fields and validation constraints to the fields.

To enable captcha, see the [Captcha configuration](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Access%20Rights/Captcha%20configuration/).

For more information about configuring the registration page, you can visit the page on the [Administration Application](https://extensions.xwiki.org/xwiki/bin/view/Extension/Administration%20Application).

## Default User Preferences

See the [User Module documentation](https://extensions.xwiki.org/xwiki/bin/view/Extension/User%20Module/API/#HConfiguration).

## Initial Groups

You can set the default groups to which new users will automatically be added by changing the xwiki.users.initialGroups parameter in your [xwiki.cfg](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HSamplexwiki.cfg) file. To make sure all new users be added to the groups **XWiki.CoolPeople** and **XWiki.CommunityMembers** you will have to set the initialGroups parameter like this:

```
xwiki.users.initialGroups=XWiki.CoolPeople, XWiki.CommunityMembers
```

- Current members will not be automatically be added to these groups, only new members.
- The groups have to be created before being specified as initial groups.

## Logging

See the [Logging page](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Logging).

## Configuring Interwiki links

[Interwiki linking](http://en.wikipedia.org/wiki/InterWiki) is a short hand syntax for linking to pages on other websites. For example, you could link to [http://en.wikipedia.org/wiki/InterWiki](http://en.wikipedia.org/wiki/InterWiki) just by typing \[\[InterWiki@WikiPedia\]\].

Note that different lists have to be maintained to support this function in XWiki Syntax 1.0 and 2.x.

The link notation for Interwiki links has changed in XWiki Syntax 2.1. Links should look like this in XWiki Syntax 2.1: \[\[interwiki:WikiPedia:InterWiki\]\].

## Interwiki links (XWiki Syntax 1.0)

Since XWiki renders wiki syntax using the [Radeox](http://codemonkeyism.com/forking-radeox-a-new-wiki-render-engine/) engine, it supports Interwiki links in [much the same way as SnipSnap](http://snipsnap.org/space/InterWiki+HowTo).

To configure Interwiki links on your wiki:

- Create a file named \[location from where you start your container\]/conf/ **intermap.txt**
- Fill intermap.txt with content like:
	```
	IMDB http://us.imdb.com/Title?
	OpenWiki http://openwiki.com/?
	SourceForge http://sourceforge.net/
	TWiki http://twiki.org/cgi-bin/view/
	Why http://clublet.com/c/c/why?
	Wiki http://c2.com/cgi/wiki?
	WikiPedia http://www.wikipedia.com/wiki/
	```
	You can of course add your own entries.

Radeox's parser for intermap.txt is very fragile. A blank line at the bottom of the file is enough to make it fall over.

Restart XWiki (you'll need to restart XWiki every time you change intermap.txt) and try out an Interwiki link. If it does not work, check your xwiki.log file. You'll see if conf/intermap.txt could not be found, or if there was an error parsing it.

## Interwiki links (XWiki Syntax 2.x)

In order to use Interwiki links in the XWiki Syntax 2.x it is necessary to configure the appropriate list in your xwiki.properties file. Look for the following section:

```
#-# InterWiki definitions in the format alias=URL
#-# See http://en.wikipedia.org/wiki/Interwiki_links for a definition of an InterWiki link
# Some examples:
# rendering.interWikiDefinitions = wikipedia = http://en.wikipedia.org/wiki/
# rendering.interWikiDefinitions = definition = http://www.yourdictionary.com/
```

## Link URLs

With parameters, you can specify what type of links XWiki will make.

## Reverse proxy setup

XWiki can and does run behind reverse proxies such as Apache mod\_proxy. Usually, the only thing needed is to have the X-Forwarded-Host HTTP header set to the external URL, and XWiki will write links correctly.

Some reverse proxy software does not set this header, and with XWiki 3.0M3 or newer, you can use the xwiki.home parameter in single wiki instances (non farm) to achieve the same result.

- **xwiki.home** - parameter in xwiki.cfg will be used to make all links pointing to the main wiki on the server. If your main wiki is called "xwiki" but you want your users to access it by going to *www.yoursite.tld* instead of *xwiki.yoursite.tld*, you may set the xwiki.home parameter to *http://www.yoursite.tld/*  
	This parameter will also work for single wiki instances and will be the final authority if the X-Forwarded-Host parameter is not set.
- **xwiki.url.protocol** - with the xwiki.url.protocol parameter in xwiki.cfg you can explicitly specify the protocol as HTTPS. This is useful if you are running XWiki behind a reverse proxy which converts HTTPS into plain HTTP so XWiki only sees HTTP.

## Short URLs

It's possible to [configure XWiki to use shorter URLs](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/ShortURLs/).

## Configure the names of database schemas

Sometimes, especially in a complex environment, we need to control the names of database schemas other than the default.

- **xwiki.db**: name of database schema for the main wiki (including the name of the wiki in a single-wiki environment, otherwise the database name comes from the Hibernate configuration file).
- **xwiki.db.prefix**: useful mainly for [sub wikis](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Virtualization/), where we have a separate database schema for each sub wiki. This prefix is added to the database schema name after usual mapping between wiki names and schemas. Note that this is also applied to the main wiki database name.

## Controlling Page Tabs

You can do this from the [Administration](https://extensions.xwiki.org/xwiki/bin/view/Extension/Administration%20Application#HPresentation).

If you wish to turn on/off comments/annotations/attachments/history/information tabs only for a single page you just need to [define some properties in a script in the page](https://www.xwiki.org/xwiki/bin/view/Documentation/DevGuide/Scripting#HControllingPageTabs).

Last, suppose you wish to turn them off based on some programmatic rule (such as display them only for Administrators). In that case, you should define the properties in the layoutExtraVars.vm template file from your XWiki installation. For example:

```
#if (!$hasAdmin)
  ## Hide tabs
  #set($displayDocExtra = false)
  ## Hide viewer shortcuts in the menu
  #set ($displayShortcuts = false)
#end
```

## Configure "Version Summary" behavior

When editing a page, you can add a brief description of your changes in the "Version Summary" field by default (look at [Common edit actions](https://www.xwiki.org/xwiki/bin/view/Doc/xs/user/base/page/edit-page/common-edit-actions/)). You can disable this feature by setting xwiki.editcomment=0 in xwiki.cfg.

When the "Version Summary" feature is enabled, you can also make "Version Summary" mandatory by setting xwiki.editcomment.mandatory=1 in xwiki.cfg. This will show a pop-up window with the request to write a short comment if no comment is entered. It doesn't allow you to enter an empty comment. If you want a popup, but you also want to be able to enter an empty comment, set xwiki.editcomment.suggested=1 in xwiki.cfg.

If you set "Version Summary" as mandatory or suggested, you can remove the "Version Summary" field and use only a pop-up window to write a comment. Set xwiki.editcomment.hidden=0 in xwiki.cfg to do this.

You can use the special fields in the XWikiPreferences object instead of editing xwiki.cfg. These fields are: editcomment, editcomment\_mandatory.

## Configuring Directories

XWiki uses the following directories:

- A Temporary directory. It's used, for example, to cache images after re-sizing them or store attachments after loading them out of the database.
- A Permanent directory. It's used to store data such as extensions and [filesystem attachments](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Attachments#HFilesystemAttachmentStore) that must not be deleted and search indexes that are replaceable but laborious to create.

## Permanent Directory

To set the permanent directory, you have 2 options:

- Set the xwiki.data.dir system property when starting the JVM (ie. the Servlet Container's JVM, specifically: \-Dxwiki.data.dir=...)
- Set the environment.permanentDirectory property in your xwiki.properties file

Make sure to choose a folder different from the XWiki home on which XWiki (which usually means whatever user is running the application server in which XWiki is installed) has write access. For example, the standard Debian package uses /var/lib/xwiki/data, which is usually a good fit for many Linux distributions.

If the location points to a file or a directory to which XWiki does not have write access, a warning will be printed in the log, and the temporary directory will be used as a default. The temporary directory can be periodically cleaned and all its content deleted, so it mustn't be used for anything else. Thus, setting the Permanent directory is critical to avoid pointing to the temporary directory.

There are 2 ways to find out what your current permanent directory:

- Check the XWiki logs and look for the "Using permanent directory" string.
- Put the following in a wiki page (using the wiki editor). Beware that you'll need to have programming rights for this to work:
	```
	{{velocity}}
	$services.component.getInstance('org.xwiki.environment.Environment').getPermanentDirectory().getCanonicalPath()
	{{/velocity}}
	```

List of sub-directories in the permanent directory:

- store: Data stores
	- store/file: Attachments ([when they're saved on the filesystem](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Attachments#HAttachmentStorage), which is the default, otherwise they're saved in the database), and deleted documents. Note that even when attachments are saved on the filesystem the attachment metadata is saved in the database (e.g. creator, date, etc).
	- store/solr: Solr configurations and data that cannot reindex from a different data source (cache data is located in cache, see below).
- extension: Installed extensions and metadata about where they are installed.
- cache: Cache files. These files and subdirectories can be removed, XWiki will regenerate them (e.g. the Solr search indexes). However that can take a lot of time. Examples of what's contained in the cache:
	- Solr search indexes
	- Descriptors of core extensions. If you delete them, XWiki will try to resolve those extensions again at startup, but it won't need to resolve much since the WAR embeds complete descriptors for all the JARs. Removing this directory allows cleaning descriptors that were downloaded in previous versions of XWiki.
	- FOP Font cache
- mails: The [Mail Sender API](https://extensions.xwiki.org/xwiki/bin/view/Extension/Mail%20Sender%20API) (used by several features of XWiki that require sending mails) will serialize email messages in this directory before they are sent, so that if XWiki crashes or is stopped, those mails are not lost and can be resent. Once a mail is successfully sent, its associated file is removed from this directory. Thus this directory will contain mails that failed to be sent.
- logs: Contains the XWiki logs but this is only true for the [XWiki Standalone packaging](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Installation/#HInstallationMethods) which has Jetty configured to generate its logs in this directory.
- jobs/status: Logs and statuses of the various background jobs executed inside XWiki (e.g. when deleting a page or set of pages, a job is used). The path follows the job ID. XWiki 17.2.0+, 16.10.6+ The path has store version as prefix as different versions can have differences in how job IDs are mapped to file names. The current version is 3. Note that most of them are used only to remember what happened during the job execution and are generally safe to remove, but some might use the job status for other purposes. Here are a few examples of standard jobs (but there can be more coming from extensions):
	- jobs/status/3/distribution: Remember the decisions taken in each wiki's Distribution Wizard (DW) (usually during install/upgrade). It's recommended to keep them, but the worst that can happen when deleting them is getting the DW again during next restart (if one of the steps is triggered, for example, when you have an orphaned or invalid extension installed) and having to cancel some steps again until the next upgrade
	- jobs/status/3/extension: Removing them is safe and won't have any impact other than losing the log of latest install/uninstall of each extension
	- jobs/status/3/refactoring: Removing them is safe and won't have any impact other than losing the log of latest refactoring operations
	- jobs/status/3/solr/indexer: Removing it is safe and won't have any impact other than losing the log of latest Solr indexing operation
	- jobs/status/3/wikicreation: Removing it is safe and won't have any impact other than losing the log of latest wiki creation operations
- database: This is only true for the [XWiki Standalone packaging](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Installation/#HInstallationMethods) and contains the HSQLDB database data (i.e. the wiki pages and more).
- mentions: The [Mentions Application](https://extensions.xwiki.org/xwiki/bin/view/Extension/Mentions%20Application/) uses this directory to store the queue of documents waiting to be analysed for new mentions.
- observation: The [Observation Module Remote](https://extensions.xwiki.org/xwiki/bin/view/Extension/Observation%20Module%20Remote) uses this directory to store the unique identifier of the instance in a cluster.
- XWiki 15.9+ configuration.properties: Contains configuration generated by XWiki itself (for example, the validation and encryption keys used for cookies when not provided in xwiki.cfg)

## Temporary Directory

The temporary directory is taken from the Servlet Container's javax.servlet.context.tempdir Servlet Context property and thus must be configured at that level. If it is pointed to a file or directory where XWiki cannot write, it will print a warning in the log and attempt to use the [java.io.tmpdir](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/System.html#getProperties\(\)) System property. If this is not a writable directory, an exception will be thrown.

Also note that 3rd party libraries used by XWiki could be using another temporary directory. Usually that would the tmp dir provided by the JVM, i.e. the location pointed to by the [java.io.tmpdir](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/System.html#getProperties\(\)) System property.

To know the location, put the following in a wiki page (using the wiki editor). Beware that you'll need to have programming rights for this to work:

```
{{velocity}}
$services.component.getInstance('org.xwiki.environment.Environment').getTemporaryDirectory().getCanonicalPath()
{{/velocity}}
```

## Configuring WebDAV (since 1.7)

WebDAV support has been added to XWiki since XWiki 1.7. It is very important to note that WebDAV is enabled by default.

## Securing WebDAV Server

XWiki's WebDAV implementation only supports the [Basic Access Authentication](http://en.wikipedia.org/wiki/Basic_access_authentication) scheme for authenticating WebDAV clients. For this reason, it is highly recommended that you employ a transport-level security mechanism like SSL to protect your clients. You may consult your web application container's documentation to see how this can be achieved.

## Disabling WebDAV

To disable WebDAV support in your XWiki server, edit your web.xml file and remove the URL-mapping element for mapping WebDAV requests. The URL-mapping element for WebDAV looks like this:

```xml
<servlet-mapping>
 <servlet-name>webdav</servlet-name>
 <url-pattern>/webdav/*</url-pattern>
</servlet-mapping>
```

## Redirections

XWiki supports defining redirections for incoming requests. To activate this feature, modify your xwiki.cfg file and set the following property: `xwiki.preferences.redirect=1`.  
Then, for each redirection you want to add, add a XWiki.GlobalRedirect object to your main wiki's XWiki.XWikiPreferences document. The XWiki.GlobalRedirect object has 2 fields: pattern and destination. The URL received is matched on pattern, and if there's a match, it's replaced with the value from the destination. XWiki then redirects to the new URL.

## Trusted domains

By default, redirections are only allowed to the trusted domains of the wiki. Those trusted domains are coming from two sources:  
\- all domains used to access the wiki are trusted by definition, as well as the aliases used for subwikis,  
\- in xwiki.properties, it's possible to specify the property url.trustedDomains to specify other domains that should be trusted.

In case a redirection is attempted on a domain not trusted, a warning is displayed in logs, and the redirection is prevented.  
Note that this whole mechanism can be switched off by setting url.trustedDomainsEnabled to false in xwiki.properties.

XWiki 17.9.0+, 16.10.13+, 17.4.6+

A new mechanisms ensure that users get asked before being driven to an untrusted domain when clicking on a link in the wiki. That mechanism reuses the configured list of trusted domain, but also a new configuration to allow specific URLs without allowing an entire domain: url.allowedFrontendUrls.

It's possible to also disable this mechanism by using url.frontendUrlCheckEnabled=false in xwiki.properties.

## Customizing the PDF export Look & Feel

The default PDF export now uses the [client-side PDF Export Application](https://extensions.xwiki.org/xwiki/bin/view/Extension/PDF%20Export%20Application/). The documentation below is for the older server-side PDF export (implemented with Apache FOP)

## General Architecture

Here's how the PDF and RTF exports currently work:  
![XWikiExport201010290119.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/XWikiExport201010290119.png?rev=1.1)

As shown in the diagram, you can customize 4 parts:

- The templates, pdf.vm and the referenced subparts, pdfhtmlheader.vm, pdfheader.vm, pdffooter.vm, pdftoc.vm, pdfcover.vm, which can be overridden by a copy located in a custom skin
- The CSS is used to render the content as PDF/RTF. There is no pdf.css by default. It could be created in /templates or a skin; a copy in a skin, and override the one located in /templates
- The XHTML2FO XSL transformation. The default one, [xhtml2fo.xsl](http://www.github.com/xwiki/xwiki-platform/tree/master/xwiki-platform-core/xwiki-platform-oldcore/src/main/resources/xhtml2fo.xsl), is packed in a core jar, but could be overridden by a new one in a template or an xhtml2fo.xsl file in WEB-INF/classes directory, if customization needed.
- The FOP XSL transformation. The default fop.xsl is also packed in a core jar.

After the export request triggers XWiki ExportAction, the content of your document is parsed by Velocity to get the initial XHTML content. **[JTidy](http://jtidy.sourceforge.net/)**, a HTML/XHTML syntax checker and pretty printer, will clean the initial XHTML to make it XHTML compliant. No customization is possible in this step.

In order to provide your customization you need to start by tweaking the default templates (they can also be copied to a new skin) and/or by creating a new [XWiki Class](https://www.xwiki.org/xwiki/bin/view/Doc/xs/user/base/page/edit-page/edit-class-editor/). To do that, simply create a new page called *XWiki.PDFClass* and edit it in class mode (for ex. *http://yourserver.com/xwiki/bin/edit/XWiki/PDFClass?editor=class*). Add the following "Text Area" properties as needed (they are all optional, so you only need to define the ones you need to use):

- style: contains the CSS information that will overwrite or complement the default pdf.css values if they exist. **[css4j](https://css4j.github.io/)**, a CSS API implementation for the Java™ platform, will handle this.
- xhtmlxsl: contains the XHTML to FO XSL overriding the default one. It is processed by **[Apache Xalan](http://xml.apache.org/xalan-j/)**, a XSLT processor for transforming XML documents into HTML, text, or other XML document types. This field needs to be the actual content of the customized xhtml2fo.xsl. Note that you can also use velocity in this field (useful to get the content of an attached.xsl file, which comes in very handy when you need to fill in a big file, since the limit of textarea properties is 60 000 characters)
- fopxsl: contains the FOP to PDF/RTF XSL overriding the default one. It is processed by **[Apache FOP](http://xmlgraphics.apache.org/fop/)**.

The name of the class must be XWiki.PDFClass.

The good thing about fop/xsl-fo is that the xsl-fo document is independent of the final result. So we can export the wiki documents into many formats.

Then create a new page (say XWiki.PDFTemplate) and add the XWiki.PDFClass object to it.

Last use that page when calling the PDF/RTF export using the pdftemplate parameter as in *http://yourserver/xwiki/bin/export/Space/Page?format=pdf&language=en&pdftemplate=XWiki.PDFTemplate*.

No template is used by default.

As mentioned, the style property stores CSS code. The field is parsed by the Velocity engine, so you can use the [current color theme](https://extensions.xwiki.org/xwiki/bin/view/Extension/Color%20Theme%20Application#HUsingColorThemesvariables) to style your PDF. Also, you can insert a page break in a PDF file with the page-break-before CSS instruction. For example:

```
#template('colorThemeInit.vm')
h2 {
   color: $theme.titleColor;
}

td {
   border-color: $theme.borderColor;
}

h1, .my_Page_break {
  page-break-before:always;
}
```

## Override the PDF Templates

By default, the PDF footer will display the page number, the last author and the date the last modification was performed. In order to also display a customized message, the template pdffooter.vm must be overridden. To do that, edit the skin class (e.g. *http://yourserver/xwiki/bin/edit/XWiki/XWikiSkins?editor=class*) and add a "TextArea" object named pdffooter.vm:

After adding the pdffooter.vm, you might want to edit it (clicking on it opens a detailed editor) and e.g. give it a "Pretty name". In this editor, also set the "Editor" property to "pure text" as otherwise the WYSIWYG-Editor will be used:

Next, edit the skin page (e.g. *http://yourserver/xwiki/bin/edit/XWiki/DefaultSkin?editor=object*) and add the following code to the pdffooter.vm property:

```
$msg.Page <span class="page-number"></span> - $msg.get('lastmodifiedby')
$xwiki.getUserName($tdoc.author, false)
$msg.get('lastmodifiedon')
$!xwiki.formatDate($tdoc.date)
<div>
<p>CustomName SAS. All rights reserved. Confidential and proprietary document. Printed Copies are not controlled.</p>
</div>
```

To see the changes, just export any wiki page:

### Customize the PDF Cover

For instance, this could be useful when you want to add the company's logo to the PDF cover. In order to do this, the template pdfcover.vm must be overridden. Just like for the PDF header, a "TextArea" property named pdfcover.vm must be added to the XWiki.XWikiSkins class (e.g. *http://yourserver/xwiki/bin/view/XWiki/XWikiSkins?editor=class*).

![OverridePDFCover.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/OverridePDFCover.png?rev=1.2)

Next, edit the skin page (e.g. *http://yourserver/xwiki/bin/edit/XWiki/DefaultSkin?editor=object*) and add the following code to the pdfcover.vm property:

```
<img src="$xwiki.getSkinFile("logo.png")"/>

<div style="text-align: center; width: 100%;">
<h1>
#set($title = "$!pdfdoc.display('title', 'rendered')")
#if($title == '')
  $escapetool.xml($!doc.displayTitle)
#else
  $escapetool.xml($title)
#end
</h1>
<br />
<br />
$!xwiki.getUserName($tdoc.author, false)
<br />
$!xwiki.formatDate($tdoc.date)
</div>
```

The last step consists of attaching the image "logo.png" to the skin:

![OverridePDFCoverFinal.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/OverridePDFCoverFinal.png?rev=1.2)

### Override the CSS rules

In order to use your template when exporting a page as PDF, you need to create a class in the XWiki space and name it PDFClass. Next, edit the page in "Class" mode (e.g. *http://yourserver/xwiki/bin/edit/XWiki/PDFClass?editor=class*) and add the following TextArea properties:

- style: contains the CSS rules that will override the default pdf.css values; by default, there won't be a pdf.css file on your filesystem, but you can create it in the folder \\webapps\\xwiki\\templates\\ or specify it in your skin page
- xhtmlxsl: contains the XHTML2FO XSL transformation that will override the default one
- fopxsl: contains the FOP XSL transformation that will override the default one

For each property added, make sure to set the Content property metadata to PureText in order not to get the WYSIWYG editor, which would make it complex to enter XML/XSL.

![CreatePDFClass.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/CreatePDFClass.png?rev=1.2)

Then, create the wiki page for which you want to customize the PDF export (e.g. XWiki.PDFTemplate) and add a XWiki.PDFClass object.

Supposing your wiki page Sandbox.TestPage1 contains a table, you have to edit it in "Wiki" mode and add a style parameter as shown below:

```
(% class="mytable" %)
|=Column 1|=Column 2
| data|data
```

Next, edit the template page (e.g. XWiki.PDFTemplate) in "Objects" mode and write your own CSS rules in the style property:

![CreatePDFTemplate.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/CreatePDFTemplate.png?rev=1.2)

Because no template is used by default, you need to specify the pdftemplate parameter in the URL to use your template: *http://yourserver/xwiki/bin/export/Sandbox/TestPage1/?format=pdf&pdftemplate=XWiki.PDFTemplate*.

![SandboxTestPage1PDF.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/SandboxTestPage1PDF.png?width=700&rev=1.2)

**Tip**: download the [PDF class](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/XWiki.PDFClass.xar?rev=1.1) and [PDF template](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/XWiki.PDFTemplate.xar?rev=1.1) for this example and test them on your wiki.

Even though RTF export is expected to work the same way, there are still some issues to be solved affecting how CSS properties control the final layout.

If some CSS styling doesn't work on PDF export, you could check if CSS instruction is supported by XSL-FO on [Apache™ FOP Compliance Page](https://xmlgraphics.apache.org/fop/compliance.html).  
Furthermore, you can not use multiple attributes to select a CSS element (see issue: [XWIKI-14653](https://jira.xwiki.org/browse/XWIKI-14653)).

### Override the xhtml2fo.xsl rules

As explained above, the entire code of [xhtml2fo.xsl](http://www.github.com/xwiki/xwiki-platform/tree/master/xwiki-platform-core/xwiki-platform-oldcore/src/main/resources/xhtml2fo.xsl) needs to be copied into the xhtmlxsl textarea and then customized.

For example, to disable the generation of clickable URLs in the PDF, modify the following section:

```
<xsl:template match="html:a[@href]" mode="transform">
    <fo:basic-link xsl:use-attribute-sets="a-link">
      <xsl:call-template name="process-a-link"></xsl:call-template>
    </fo:basic-link>
  </xsl:template>
```

as

```
<xsl:template match="html:a[@href]" mode="transform">
    <fo:inline>
      <xsl:call-template name="process-a-link"></xsl:call-template>
    </fo:inline>
  </xsl:template>
```

or disable the generation of clickable URLs for some specific href links in the PDF

```
<xsl:template match="html:a[@href]" mode="transform">
    <xsl:choose>
      <!-- disable these internal links ("data-parent" attribute start with "#accordion" or href is "#my_anchor") -->
      <xsl:when test="starts-with(@data-parent,'#accordion') or @href = '#my_anchor'">
        <fo:inline>
          <xsl:call-template name="process-a-link"></xsl:call-template>
        </fo:inline>
      </xsl:when>
      <xsl:otherwise>
        <fo:basic-link xsl:use-attribute-sets="a-link">
          <xsl:call-template name="process-a-link"></xsl:call-template>
        </fo:basic-link>
      </xsl:otherwise>
    </xsl:choose>
  </xsl:template>
```

### Debugging PDF export

To inspect the contents of the created XHTML file (and be able to style it) - turn on logging *http://yourserver/xwiki/bin/view/AdminGuide/Logging* and set com.xpn.xwiki level to DEBUG. After PDF export action, xwiki log file contains intermediates states XHTML code after these lines:

```
DEBUG c.x.x.p.i.PdfExportImpl        - Cleaning HTML: //(show XHTML code without style)//
DEBUG c.x.x.p.i.PdfExportImpl        - Cleaned XHTML:
DEBUG c.x.x.p.i.PdfExportImpl        - Applying the following CSS: //(show CSS properties)//
DEBUG c.x.x.p.i.PdfExportImpl        - HTML with CSS applied: //(show HTML code with CSS properties merged in tag with "style=" )//
DEBUG c.x.x.p.i.PdfExportImpl        - Final XHTML for export:
DEBUG c.x.x.p.i.PdfExportImpl        - Intermediary XSL-FO: //(show document with eXtensible Stylesheet Language - Formatting Objects used to generate PDF files)//
DEBUG c.x.x.p.i.PdfExportImpl        - Final XSL-FO source:
and finally DEBUG c.x.x.p.i.PdfExportImpl        - PageSequence x-page-sequence generated 3 pages.
```

## Configuring Wiki Syntaxes and default Syntax

To configure the [Wiki syntaxes](https://www.xwiki.org/xwiki/bin/view/Documentation/UserGuide/Features/XWikiSyntax/) available to the user when writing wiki pages, check the [Rendering Administration Application](https://extensions.xwiki.org/xwiki/bin/view/Extension/Rendering%20Administration%20Application/).

## Title behavior

The following configuration parameters (found in xwiki.cfg) can be used to control title behavior:

```
#-# Defines whether title handling should be using the compatibility mode or not. When the compatibility
#-# mode is active, XWiki will try to extract a title from the document content.
#-# If the document's content first header (level 1 or level 2) matches the document's title
#-# the first header is stripped.
#-# The default value is 0.
# xwiki.title.compatibility=1

#-# Defines the maximum header depth to look for when computing a document's title from its content. If no header
#-# equal or lower to the specified depth is found then the computed title falls back to the document name.
#-# The default value is 2.
# xwiki.title.headerdepth=2

#-# Defines if setting the title field must be mandatory in the WYSIWYG and Wiki editors. It is mandatory when this
#-# property is set to 1. The default value is 0 (not mandatory).
# xwiki.title.mandatory=0
```

## Link Label Generation

Starting with XWiki Syntax 2.0 it's possible to configure how labels are generated by the system when the user doesn't provide one (e.g. \[\[mywiki:Main.WebHome\]\]).

Here's an extract from the xwiki.properties file, which is where this feature is configurable:

```
#-# Specifies how links labels are displayed when the user doesn't specify the label explicitly.
#-# Valid values:
#-#   %w: wiki name
#-#   %s: full space name (e.g. space1.space2)
#-#       Note: Prior to 7.4.2/8.0M2 this was only displaying the last space name
#-#   %ls: last space name. New in 7.4.2/8.0M2
#-#   %p: page name
#-#   %np: nested page name (i.e. will display the space name for Nested Pages). New in 7.4.2/8.0M2
#-#   %P: page name with spaces between camel case words, i.e. "My Page" if the page name is "MyPage"
#-#   %NP: nested page name with spaces between camel case words, i.e. "My Page" if the page name is "MyPage".
#-#        New in 7.4.2/8.0M2
#-#   %t: page title
#-#
#-# Note that if the page title is empty or not defined then it defaults to %np. This is also the case
#-# if the title cannot be retrieved for the document.
#-#
#-# The default is "%np". Some examples: "%s.%p", "%w:%s.%p".
# rendering.linkLabelFormat = %np
```

## Rendering Cache

See the [Performance page](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Performances/#HRenderingcache).

## Allowed Pages for Inactive Users

The xwiki.cfg configuration file includes xwiki.inactiveuser.allowedpages. This property can be used to build a whitelist of pages that can be read by inactive users. The format that should be used is a comma-separated list of pages that users marked as inactive can see.

This property is needed because in XWiki, some users can be marked inactive, for example, when enabling user email verification in the administration. An inactive user has an account, but the account needs to be validated for the user to be able to access the wiki. Access rights do not apply to inactive users (they are recognized neither as XWikiGuest nor as members of XWikiAllGroup).

Inactive users are always allowed to see the XWiki.AccountValidation page is used to validate their account.

## Rendering Transformations

You can control which [Transformations](https://rendering.xwiki.org/xwiki/bin/view/Main/Architecture) are active (by default, the [Macro](https://rendering.xwiki.org/xwiki/bin/view/Main/Architecture) and [Icon](https://rendering.xwiki.org/xwiki/bin/view/Main/Transformations#HIconTransformation) ones are active) by editing xwiki.properties:

```
#-# Controls what transformations will be executed when rendering content.
#-# A transformation modifies the parsed content. For example the Icon transformation replaces some characters with
#-# icons, a WikiWord transformation will automatically create links when it finds wiki words, etc.
#-# Note that the Macro transformation is a special transformation that replaces macro markers by the result of the
#-# macro execution. If you don't list it, macros won't get executed.
#-# The default value is: rendering.transformations = macro, icon
```

For example, if you wish to turn off the Icon Transformation in order not to render emoticons, you'd have to define the following property: `rendering.transformations = macro`.

## Macros categories and visibility

You can override the default categories of a macro by editing xwiki.properties.

```
#-# Overrides default macro categories (Each macro has default categories already defined, for example
#-# "Navigation" for the Table of Contents Macro).
#-# Note: the categories are case sensitive.
#-#
#-# Ex: To redefine the macro categories for the TOC macro so that it'd be in the "My Category" and "Deprecated" 
#-# categories + redefine the category for the Script Macro to be "My Other Category", you'd use:
# rendering.transformation.macro.categories = toc = My Category\,Deprecated
# rendering.transformation.macro.categories = script = My Other Category
```

You can also configure the macro categories for which macros should be hidden by default, by editing xwiki.properties:

```
#-# Override the default hidden macro categories.
#-# Note: the categories are case sensitive.
#-#
#-# The default value is:
# rendering.transformation.macro.hiddenCategories = Internal,Deprecated
#-#
#-# For instance, to make the "Development" category hidden by default, in addition to the "Internal" and
#-# "Deprecated" categories, you'd use:
# rendering.transformation.macro.hiddenCategories = Development,Internal,Deprecated
```

Note that these macros are still visible if your users have configured to show [hidden pages](https://www.xwiki.org/xwiki/bin/view/Doc/xs/user/base/page/view-page/hide-page/hidden-pages/) by [editing the profile preferences](https://www.xwiki.org/xwiki/bin/view/Doc/xs/user/user/profile/edit-profile/edit-profile-preferences/).

## Securing Groovy Scripts

See:

- The [Commons Groovy Module](https://extensions.xwiki.org/xwiki/bin/view/Extension/GroovyModuleCommons)
- The [Platform Groovy Module](https://extensions.xwiki.org/xwiki/bin/view/Extension/GroovyModulePlatform)

## Lock Duration

By default, when a user starts editing a page, a lock will be set on that page, see [Page Editing](https://www.xwiki.org/xwiki/bin/view/Documentation/UserGuide/Features/PageEditing/#HLocking). The lock is valid by default for 30 minutes, after which it gets invalidated.

In order to increase this duration, you have 2 options:

- Add a property named lock\_Timeout to your xwiki.cfg configuration file, set the value in seconds (and restart XWiki). For example, for 15 minutes: lock\_Timeout = 900.
- Or add the configuration in the wiki itself:
	- Edit the XWiki.XWikiPreferences document using the class editor
	- Add a Number property named lock\_Timeout (case sensitive)
	- Edit the XWiki.XWikiPreferences document using the object editor
	- Find the lock\_Timeout property and put the desired number of \*seconds\* a lock should be valid for
	- Don't forget to save the document

## Editing

## Default editor

You can choose which default editor to use when editing wiki content (wiki or WYSIWYG editor). XWiki uses the following strategy when deciding which editor to use:

1. If editing a [TextArea object property](https://www.xwiki.org/xwiki/bin/view/Doc/xs/dev/model/data-model/x-properties/) and that property has explicitly specified a specific editor to be used to edit it, then that editor will be used. This is set when [using the Class editor](https://www.xwiki.org/xwiki/bin/view/Doc/xs/user/base/page/edit-page/edit-class-editor/). For example:
	![editor-class-property.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/editor-class-property.png?rev=1.1)
2. Then, if no property editor is defined, or if editing standard wiki content (like page content), XWiki will check if the [current user has configured an editor for a given content type](https://extensions.xwiki.org/xwiki/bin/view/Extension/Edit%20Module#HConfiguretheDefaultEditor). If the current edited content is of that type, then that editor will be used. For example:
	![editor-content-user.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/editor-content-user.png?rev=1.1)
3. Then, if no property editor is defined, XWiki will check if the [current (nested) page has configured an editor for a given content type](https://extensions.xwiki.org/xwiki/bin/view/Extension/Edit%20Module#HConfiguretheDefaultEditor). If the current edited content is of that type, then that editor will be used. For example:
	![editor-content-page.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/editor-content-page.png?rev=1.1)
4. Then, if no property editor is defined, XWiki will check if the [current wiki has configured an editor for a given content type](https://extensions.xwiki.org/xwiki/bin/view/Extension/Edit%20Module#HConfiguretheDefaultEditor). If the current edited content is of that type, then that editor will be used. For example:
	![editor-content-wiki.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/editor-content-wiki.png?rev=1.1)
5. Then, if no property editor is defined, XWiki will check if there's a [configuration in xwiki.properties for a given content type](https://extensions.xwiki.org/xwiki/bin/view/Extension/Edit%20Module#HConfiguretheDefaultEditor) and if the current edited content is of that type, then that editor will be used. For example:
	```
	edit.defaultEditor.org.xwiki.rendering.syntax.SyntaxContent=text
	```
6. Then, if no editor has been defined, XWiki will check if the current [user has defined a preferred editor to use](https://extensions.xwiki.org/xwiki/bin/view/Extension/User%20Module/User%20Profile%20Application/#HEditPreferences). For example:
	![editor-user.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/editor-user.png?rev=1.1)
7. Then, if no preferred editor to use has been defined for the current user, XWiki will check the default editor set up in the Page Administration (XWiki.XWikiPreferences of the page). Could be set because of [XWIKI-17324](https://jira.xwiki.org/browse/XWIKI-17324). For example:
	![editor-space-preference-object.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/editor-space-preference-object.png?rev=1.1)
8. Then, if no editor has been defined, XWiki will check the [default editor set up in the Administration UI](https://extensions.xwiki.org/xwiki/bin/view/Extension/Administration%20Application#HEditing). For example:
	![editor-admin.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/editor-admin.png?rev=1.1)

## Default WYSIWYG editor

You can configure the [default WYSIWYG editor to use](https://extensions.xwiki.org/xwiki/bin/view/Extension/CKEditor%20Integration/#HAdministrationSection).

See the [WYSIWYG Editor Configuration](https://extensions.xwiki.org/xwiki/bin/view/Extension/CKEditor%20Integration/#HConfiguretheEditor) page to find out how to enable or disable editing features.

## Section Editing

By default, section editing is limited to level 1 and level 2 sections. This can be controlled by editing xwiki.cfg:

```
#-# This parameter controls the depth of sections that have section editing.
#-# By default level 1 and level 2 sections have section editing.
xwiki.section.depth=2
```

You can also enable/disable section editing with:

```
#-# This parameter will activate the sectional editing.
xwiki.section.edit=1
```

## Editing Conflicts

The [Edit Conflict feature](https://www.xwiki.org/xwiki/bin/view/Documentation/UserGuide/Features/PageEditing/#HEditconflict) can be disabled since XWiki 11.3.1+, 11.4+

from the xwiki.properties file by setting edit.conflictChecking.enabled = false:

```
#-# Indicate if the mechanism to detect and handle edition conflicts should be enabled or not.
#-# If disabled, it means that in case of edition conflicts, the latest save will be always take into account, and
#-# erase previous data (which can always be recovered in the history of the document).
#-# This option is provided because the feature is still experimental and it could be useful is some specific usecases
#-# to switch it off. However it is not recommended to do so.
#-#
#-# The default is:
# edit.conflictChecking.enabled = true
```

## In-place Editing

To disable the in-place WYSIWYG editing mode (and thus default to the Standalone WYSIWYG editing mode), modify the xwiki.properties file and set edit.document.inPlaceEditing.enabled = false:

```
#-# Indicate if the XWiki documents should be edited in-place, without leaving the view mode, whenever possible (e.g. if
#-# the default edit mode for that document and the preferred editor both support in-place editing). When enabled,
#-# clicking on the document Edit button makes the document title and content editable in-place, without leaving the
#-# view mode. When disabled, clicking on the document Edit button loads the default (stand-alone) edit mode for that
#-# document.
#-#
#-# The default is:
# edit.document.inPlaceEditing.enabled = true
```

## Delete Pages

This section is hidden when the [recycle bin is not activated](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDocumentrecyclebin).

## Enabling Advanced users to skip the recycle bin

Advanced users can choose to skip the recycle bin (and remove the pages permanently) when deleting pages.

To do so, search for the "Delete" section and set "can skip the recycle bin" to Yes. The default value is No.

![skip_recycle_bin_admin_cropped.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/skip_recycle_bin_admin_cropped.png?rev=1.1)

The configuration is resolved by looking in three locations, from the most specific to the least specific:

- In the configuration of the current wiki
- In the configuration of the main wiki
- In xwiki.properties (see the property details below)

If the default value is found in one location, the next one is tried. If no value is found, the recycle bin skipping is not activated.

Details of the configuration on xwiki.properties:

```
#-# Indicates whether skipping the recycle bin when deleting pages is allowed for Advanced users.
#-# It is disabled by default.
#-# This setting is only used if the wiki has a recycle bin activated (xwiki.recyclebin=1 in xwiki.cfg).
#-# This setting can be overloaded:
#-# * By the main wiki in the Refactoring.Code.RefactoringConfigurationClass class of the
#-#   Refactoring.Code.RefactoringConfiguration document of the main wiki.
#-# * By sub-wikis in the Refactoring.Code.RefactoringConfigurationClass class of the
#-#   Refactoring.Code.RefactoringConfiguration document of the sub-wikis (itself overloading the main wiki's
#-#   configuration).
#-#
#-# The default value is:
# refactoring.isRecycleBinSkippingActivated = false
```

## Readonly

In order to configure your XWiki instance to be readonly (useful when doing an upgrade by setting up a new instance and you don't want new content to be created, for example).

To achieve this, you need to edit the xwiki.cfg configuration file and set the xwiki.readonly property to true and restart XWiki.

If you want to turn on the readonly mode live without a restart, you can also execute a small snippet with a user having programming rights (a restart of XWiki will remove the readonly mode in this case), while waiting for a future feature (see issue [XWIKI-10119](https://jira.xwiki.org/browse/XWIKI-10119)):

```
{{groovy}}
def xwiki = xcontext.getXWiki()
xwiki.isReadOnly = true
{{/groovy}}
```

Note that this flag doesn't prevent against any modifications in your wiki, there're still some places where it's not taken into account (see issue [XWIKI-18437](https://jira.xwiki.org/browse/XWIKI-18437))).

## Sample xwiki.cfg

See [xwiki.cfg.vm](http://www.github.com/xwiki/xwiki-platform/tree/master/xwiki-platform-tools/xwiki-platform-tool-configuration-resources/src/main/resources/xwiki.cfg.vm)

Note that we generate the default xwiki.cfg file from this template file by applying Velocity during the build, so all $<something> properties you see in this file are replaced at build time.

## Sample xwiki.properties

See [xwiki.properties.vm](http://www.github.com/xwiki/xwiki-platform/tree/master/xwiki-platform-tools/xwiki-platform-tool-configuration-resources/src/main/resources/xwiki.properties.vm)

Note that we generate the default xwiki.properties file from this template file by applying Velocity during the build, so all $<something> properties that you see in this file are replaced at build time.

from the xwiki.properties file by setting edit.conflictChecking.enabled = false:

```
#-# Indicate if the mechanism to detect and handle edition conflicts should be enabled or not.
#-# If disabled, it means that in case of edition conflicts, the latest save will be always take into account, and
#-# erase previous data (which can always be recovered in the history of the document).
#-# This option is provided because the feature is still experimental and it could be useful is some specific usecases
#-# to switch it off. However it is not recommended to do so.
#-#
#-# The default is:
# edit.conflictChecking.enabled = true
```

## In-place Editing

To disable the in-place WYSIWYG editing mode (and thus default to the Standalone WYSIWYG editing mode), modify the xwiki.properties file and set edit.document.inPlaceEditing.enabled = false:

```
#-# Indicate if the XWiki documents should be edited in-place, without leaving the view mode, whenever possible (e.g. if
#-# the default edit mode for that document and the preferred editor both support in-place editing). When enabled,
#-# clicking on the document Edit button makes the document title and content editable in-place, without leaving the
#-# view mode. When disabled, clicking on the document Edit button loads the default (stand-alone) edit mode for that
#-# document.
#-#
#-# The default is:
# edit.document.inPlaceEditing.enabled = true
```

## Delete Pages

This section is hidden when the [recycle bin is not activated](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDocumentrecyclebin).

## Enabling Advanced users to skip the recycle bin

Advanced users can choose to skip the recycle bin (and remove the pages permanently) when deleting pages.

To do so, search for the "Delete" section and set "can skip the recycle bin" to Yes. The default value is No.

![skip_recycle_bin_admin_cropped.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/skip_recycle_bin_admin_cropped.png?rev=1.1)

The configuration is resolved by looking in three locations, from the most specific to the least specific:

- In the configuration of the current wiki
- In the configuration of the main wiki
- In xwiki.properties (see the property details below)

If the default value is found in one location, the next one is tried. If no value is found, the recycle bin skipping is not activated.

Details of the configuration on xwiki.properties:

```
#-# Indicates whether skipping the recycle bin when deleting pages is allowed for Advanced users.
#-# It is disabled by default.
#-# This setting is only used if the wiki has a recycle bin activated (xwiki.recyclebin=1 in xwiki.cfg).
#-# This setting can be overloaded:
#-# * By the main wiki in the Refactoring.Code.RefactoringConfigurationClass class of the
#-#   Refactoring.Code.RefactoringConfiguration document of the main wiki.
#-# * By sub-wikis in the Refactoring.Code.RefactoringConfigurationClass class of the
#-#   Refactoring.Code.RefactoringConfiguration document of the sub-wikis (itself overloading the main wiki's
#-#   configuration).
#-#
#-# The default value is:
# refactoring.isRecycleBinSkippingActivated = false
```

## Readonly

In order to configure your XWiki instance to be readonly (useful when doing an upgrade by setting up a new instance and you don't want new content to be created, for example).

To achieve this, you need to edit the xwiki.cfg configuration file and set the xwiki.readonly property to true and restart XWiki.

If you want to turn on the readonly mode live without a restart, you can also execute a small snippet with a user having programming rights (a restart of XWiki will remove the readonly mode in this case), while waiting for a future feature (see issue [XWIKI-10119](https://jira.xwiki.org/browse/XWIKI-10119)):

```
{{groovy}}
def xwiki = xcontext.getXWiki()
xwiki.isReadOnly = true
{{/groovy}}
```

Note that this flag doesn't prevent against any modifications in your wiki, there're still some places where it's not taken into account (see issue [XWIKI-18437](https://jira.xwiki.org/browse/XWIKI-18437))).

## Sample xwiki.cfg

See [xwiki.cfg.vm](http://www.github.com/xwiki/xwiki-platform/tree/master/xwiki-platform-tools/xwiki-platform-tool-configuration-resources/src/main/resources/xwiki.cfg.vm)

Note that we generate the default xwiki.cfg file from this template file by applying Velocity during the build, so all $<something> properties you see in this file are replaced at build time.

## Sample xwiki.properties

See [xwiki.properties.vm](http://www.github.com/xwiki/xwiki-platform/tree/master/xwiki-platform-tools/xwiki-platform-tool-configuration-resources/src/main/resources/xwiki.properties.vm)

Note that we generate the default xwiki.properties file from this template file by applying Velocity during the build, so all $<something> properties that you see in this file are replaced at build time.

from the xwiki.properties file by setting edit.conflictChecking.enabled = false:

```
#-# Indicate if the mechanism to detect and handle edition conflicts should be enabled or not.
#-# If disabled, it means that in case of edition conflicts, the latest save will be always take into account, and
#-# erase previous data (which can always be recovered in the history of the document).
#-# This option is provided because the feature is still experimental and it could be useful is some specific usecases
#-# to switch it off. However it is not recommended to do so.
#-#
#-# The default is:
# edit.conflictChecking.enabled = true
```

## In-place Editing

To disable the in-place WYSIWYG editing mode (and thus default to the Standalone WYSIWYG editing mode), modify the xwiki.properties file and set edit.document.inPlaceEditing.enabled = false:

```
#-# Indicate if the XWiki documents should be edited in-place, without leaving the view mode, whenever possible (e.g. if
#-# the default edit mode for that document and the preferred editor both support in-place editing). When enabled,
#-# clicking on the document Edit button makes the document title and content editable in-place, without leaving the
#-# view mode. When disabled, clicking on the document Edit button loads the default (stand-alone) edit mode for that
#-# document.
#-#
#-# The default is:
# edit.document.inPlaceEditing.enabled = true
```

## Delete Pages

This section is hidden when the [recycle bin is not activated](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDocumentrecyclebin).

## Enabling Advanced users to skip the recycle bin

Advanced users can choose to skip the recycle bin (and remove the pages permanently) when deleting pages.

To do so, search for the "Delete" section and set "can skip the recycle bin" to Yes. The default value is No.

![skip_recycle_bin_admin_cropped.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/skip_recycle_bin_admin_cropped.png?rev=1.1)

The configuration is resolved by looking in three locations, from the most specific to the least specific:

- In the configuration of the current wiki
- In the configuration of the main wiki
- In xwiki.properties (see the property details below)

If the default value is found in one location, the next one is tried. If no value is found, the recycle bin skipping is not activated.

Details of the configuration on xwiki.properties:

```
#-# Indicates whether skipping the recycle bin when deleting pages is allowed for Advanced users.
#-# It is disabled by default.
#-# This setting is only used if the wiki has a recycle bin activated (xwiki.recyclebin=1 in xwiki.cfg).
#-# This setting can be overloaded:
#-# * By the main wiki in the Refactoring.Code.RefactoringConfigurationClass class of the
#-#   Refactoring.Code.RefactoringConfiguration document of the main wiki.
#-# * By sub-wikis in the Refactoring.Code.RefactoringConfigurationClass class of the
#-#   Refactoring.Code.RefactoringConfiguration document of the sub-wikis (itself overloading the main wiki's
#-#   configuration).
#-#
#-# The default value is:
# refactoring.isRecycleBinSkippingActivated = false
```

## Readonly

In order to configure your XWiki instance to be readonly (useful when doing an upgrade by setting up a new instance and you don't want new content to be created, for example).

To achieve this, you need to edit the xwiki.cfg configuration file and set the xwiki.readonly property to true and restart XWiki.

If you want to turn on the readonly mode live without a restart, you can also execute a small snippet with a user having programming rights (a restart of XWiki will remove the readonly mode in this case), while waiting for a future feature (see issue [XWIKI-10119](https://jira.xwiki.org/browse/XWIKI-10119)):

```
{{groovy}}
def xwiki = xcontext.getXWiki()
xwiki.isReadOnly = true
{{/groovy}}
```

Note that this flag doesn't prevent against any modifications in your wiki, there're still some places where it's not taken into account (see issue [XWIKI-18437](https://jira.xwiki.org/browse/XWIKI-18437))).

## Sample xwiki.cfg

See [xwiki.cfg.vm](http://www.github.com/xwiki/xwiki-platform/tree/master/xwiki-platform-tools/xwiki-platform-tool-configuration-resources/src/main/resources/xwiki.cfg.vm)

Note that we generate the default xwiki.cfg file from this template file by applying Velocity during the build, so all $<something> properties you see in this file are replaced at build time.

## Sample xwiki.properties

See [xwiki.properties.vm](http://www.github.com/xwiki/xwiki-platform/tree/master/xwiki-platform-tools/xwiki-platform-tool-configuration-resources/src/main/resources/xwiki.properties.vm)

Note that we generate the default xwiki.properties file from this template file by applying Velocity during the build, so all $<something> properties that you see in this file are replaced at build time.

from the xwiki.properties file by setting edit.conflictChecking.enabled = false:

```
#-# Indicate if the mechanism to detect and handle edition conflicts should be enabled or not.
#-# If disabled, it means that in case of edition conflicts, the latest save will be always take into account, and
#-# erase previous data (which can always be recovered in the history of the document).
#-# This option is provided because the feature is still experimental and it could be useful is some specific usecases
#-# to switch it off. However it is not recommended to do so.
#-#
#-# The default is:
# edit.conflictChecking.enabled = true
```

## In-place Editing

To disable the in-place WYSIWYG editing mode (and thus default to the Standalone WYSIWYG editing mode), modify the xwiki.properties file and set edit.document.inPlaceEditing.enabled = false:

```
#-# Indicate if the XWiki documents should be edited in-place, without leaving the view mode, whenever possible (e.g. if
#-# the default edit mode for that document and the preferred editor both support in-place editing). When enabled,
#-# clicking on the document Edit button makes the document title and content editable in-place, without leaving the
#-# view mode. When disabled, clicking on the document Edit button loads the default (stand-alone) edit mode for that
#-# document.
#-#
#-# The default is:
# edit.document.inPlaceEditing.enabled = true
```

## Delete Pages

This section is hidden when the [recycle bin is not activated](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/Configuration/#HDocumentrecyclebin).

## Enabling Advanced users to skip the recycle bin

Advanced users can choose to skip the recycle bin (and remove the pages permanently) when deleting pages.

To do so, search for the "Delete" section and set "can skip the recycle bin" to Yes. The default value is No.

![skip_recycle_bin_admin_cropped.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/Configuration/WebHome/skip_recycle_bin_admin_cropped.png?rev=1.1)

The configuration is resolved by looking in three locations, from the most specific to the least specific:

- In the configuration of the current wiki
- In the configuration of the main wiki
- In xwiki.properties (see the property details below)

If the default value is found in one location, the next one is tried. If no value is found, the recycle bin skipping is not activated.

Details of the configuration on xwiki.properties:

```
#-# Indicates whether skipping the recycle bin when deleting pages is allowed for Advanced users.
#-# It is disabled by default.
#-# This setting is only used if the wiki has a recycle bin activated (xwiki.recyclebin=1 in xwiki.cfg).
#-# This setting can be overloaded:
#-# * By the main wiki in the Refactoring.Code.RefactoringConfigurationClass class of the
#-#   Refactoring.Code.RefactoringConfiguration document of the main wiki.
#-# * By sub-wikis in the Refactoring.Code.RefactoringConfigurationClass class of the
#-#   Refactoring.Code.RefactoringConfiguration document of the sub-wikis (itself overloading the main wiki's
#-#   configuration).
#-#
#-# The default value is:
# refactoring.isRecycleBinSkippingActivated = false
```

## Readonly

In order to configure your XWiki instance to be readonly (useful when doing an upgrade by setting up a new instance and you don't want new content to be created, for example).

To achieve this, you need to edit the xwiki.cfg configuration file and set the xwiki.readonly property to true and restart XWiki.

If you want to turn on the readonly mode live without a restart, you can also execute a small snippet with a user having programming rights (a restart of XWiki will remove the readonly mode in this case), while waiting for a future feature (see issue [XWIKI-10119](https://jira.xwiki.org/browse/XWIKI-10119)):

```
{{groovy}}
def xwiki = xcontext.getXWiki()
xwiki.isReadOnly = true
{{/groovy}}
```

Note that this flag doesn't prevent against any modifications in your wiki, there're still some places where it's not taken into account (see issue [XWIKI-18437](https://jira.xwiki.org/browse/XWIKI-18437))).

## Sample xwiki.cfg

See [xwiki.cfg.vm](http://www.github.com/xwiki/xwiki-platform/tree/master/xwiki-platform-tools/xwiki-platform-tool-configuration-resources/src/main/resources/xwiki.cfg.vm)

Note that we generate the default xwiki.cfg file from this template file by applying Velocity during the build, so all $<something> properties you see in this file are replaced at build time.

## Sample xwiki.properties

See [xwiki.properties.vm](http://www.github.com/xwiki/xwiki-platform/tree/master/xwiki-platform-tools/xwiki-platform-tool-configuration-resources/src/main/resources/xwiki.properties.vm)

Note that we generate the default xwiki.properties file from this template file by applying Velocity during the build, so all $<something> properties that you see in this file are replaced at build time.

- Today
- Yesterday
- Last 7 days
- Last 30 days
- This month
- Last month
- Custom Range