---
title: "XWiki Keyboard Shortcuts (XWiki.org)"
source: "https://www.xwiki.org/xwiki/bin/view/Documentation/UserGuide/Features/KeyboardShortcuts"
author:
published:
created: 2025-11-13
description: "XWiki Keyboard Shortcuts"
tags:
---
## XWiki Keyboard Shortcuts

## Using keyboard shortcuts

See [[Keyboard Shortcuts Available when Viewing a Page (for Users) |Keyboard Shortcuts Available when Viewing a Page (for Users)]]. 
See [[Keyboard Shortcuts Available when Viewing a Page (for Administrators)|Keyboard Shortcuts Available when Viewing a Page (for Administrators)]].

## Edit Mode

See [Keyboard Shortcuts Available when Editing a Page](https://www.xwiki.org/xwiki/bin/view/Doc/xs/user/base/page/edit-page/keyboard-shortcuts-editing-page/)

## Preview Mode

See [Keyboard Shortcuts Available when Previewing a Page](https://www.xwiki.org/xwiki/bin/view/Doc/xs/user/base/page/edit-page/keyboard-shortcuts-previewing-page/).

## Annotations

See [Keyboard Shortcuts Available when Viewing a Page (for Users)](https://www.xwiki.org/xwiki/bin/view/Doc/xs/user/base/page/view-page/keyboard-shortcuts-viewing-page/).

## Navigation

See [Keyboard Shortcuts for Navigation](https://www.xwiki.org/xwiki/bin/view/Doc/xs/user/base/page/all-ways-navigate-page/keyboard-shortcuts-navigation/).

## Developer shortcuts

See [Global Keyboard Shortcuts](https://www.xwiki.org/xwiki/bin/view/Doc/xs/user/base/page/global-keyboard-shortcurts/).

## Configuring keyboard shortcuts

## Modifying keyboard shortcuts

- Create a new page in your wiki, for example XWiki.KeyboardShortcuts and paste the following content inside:
- Modify entries in this list at your convenience
- Save the page
- Edit the page in [object mode](https://www.xwiki.org/xwiki/bin/view/Documentation/UserGuide/Features/PageEditing/#HObjectseditingmode) and add an XWiki.TranslationDocumentClass xobject
	- Select the wiki scope for the new translations (i.e. the new keyboard shortcuts) to apply to the whole wiki. You'll need to have Admin permissions for it to work

## Adding your own shortcuts

You can add your own keyboard shortcuts in a few javascript lines. You can do that, for example, by adding a [JavaScript StyleSheet Extension](https://www.xwiki.org/xwiki/bin/view/Documentation/DevGuide/Tutorials/SkinExtensionsTutorial/) and putting the following content:

```javascript
shortcut.add("Ctrl+Alt+n", function() { alert("Hey there! Congratulations on typing this one ;)"); });
```

Also check the [complete documentation](https://dmauro.github.io/Keypress/).

## Removing keyboard shortcuts

To remove a shortcut adapt the following snippet to your needs and use by putting it in a [JavaScript StyleSheet Extension](https://www.xwiki.org/xwiki/bin/view/Documentation/DevGuide/Tutorials/SkinExtensionsTutorial/):

```javascript
shortcut.remove("Ctrl+Alt+n");
```

## Removing all shortcuts at once

```javascript
for (binding in shortcut.all_shortcuts()) {
  shortcut.remove(binding.keys.join(' '));
}
```

## Credits

XWiki keyboard shortcuts are powered by [Keypress JS shortcut library](https://dmauro.github.io/Keypress/).

- Today
- Yesterday
- Last 7 days
- Last 30 days
- This month
- Last month
- Custom Range