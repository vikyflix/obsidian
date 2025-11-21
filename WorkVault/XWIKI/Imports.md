---
title: "Imports"
source: "https://www.xwiki.org/xwiki/bin/view/Documentation/UserGuide/Features/Imports"
author:
published:
created: 2025-11-13
description: "Imports"
tags:
---
## Imports

There are several kinds of imports that can be done inside XWiki:

- [Importing XWiki pages](https://www.xwiki.org/xwiki/bin/view/Documentation/UserGuide/Features/#HImportingXWikipages)
- [Importing Office documents](https://www.xwiki.org/xwiki/bin/view/Documentation/UserGuide/Features/#HImportingOfficedocuments)
- [Importing from another wiki](https://www.xwiki.org/xwiki/bin/view/Documentation/UserGuide/Features/#HImportingfromanotherwiki)
- [Importing other type of data](https://www.xwiki.org/xwiki/bin/view/Documentation/UserGuide/Features/#HImportingothertypeofdata)

## Importing XWiki pages

This feature is available from the Administration and is described in the [Import/Export page of the Admin Guide](https://www.xwiki.org/xwiki/bin/view/Documentation/AdminGuide/ImportExport).

![importpage.png](https://www.xwiki.org/xwiki/bin/download/Documentation/AdminGuide/ImportExport/importpage.png?rev=1.4)

## Importing Office documents

This feature is available from the [Office Importer Application](https://extensions.xwiki.org/xwiki/bin/view/Extension/Office%20Importer%20Application).

![OfficeImporter.png](https://extensions.xwiki.org/xwiki/bin/download/Extension/Office%20Importer%20Application/OfficeImporter.png?rev=1.2)

## Importing from another wiki

There are several options with more or less tooling. The best tool is the [Filter Application](https://extensions.xwiki.org/xwiki/bin/view/Extension/Filter%20Application). It currently has a module for [importing wiki pages from Confluence](https://extensions.xwiki.org/xwiki/bin/view/Extension/Filter%20Confluence%20XML%20module).

Also note that XWiki supports writing wiki pages in various syntaxes (HTML, wiki syntaxes, etc) and thus it's also possible to directly copy the content of your pages from another wiki into an XWiki page (provided [the syntax used for that other wiki is supported by XWiki](https://rendering.xwiki.org/xwiki/bin/view/Main/#HSupportedSyntaxes)). However this would mean importing your content page by page. In addition the XWiki WYSIWYG editor only supports the XWiki syntax at this point so you'd have to use the wiki editor to edit those pages.

There are also [various extensions related to importing wiki content](https://extensions.xwiki.org/xwiki/bin/view/Main/Tags?do=viewTag&tag=migration).

In addition if you're importing from MediaWiki there's also a [Google Summer of Code application for doing so](https://github.com/xwiki-contrib/sandbox/tree/master/xwiki-wikiimporter) which has never been released and that you'll need to build from sources.

## Importing other type of data

There are [several extensions related to importing data into XWiki](https://extensions.xwiki.org/xwiki/bin/view/Main/Tags?do=viewTag&tag=import):

- Microsoft Excel
- CSV
- SharePoint Blogs

- Today
- Yesterday
- Last 7 days
- Last 30 days
- This month
- Last month
- Custom Range