---
# This page was generated from the add-on.
title: Import/Export
type: userguide
weight: 1
cascade:
  addon:
    id: exim
    version: 0.8.0
---

# Copy URLs to Clipboard

A context menu item to Copy URLs to the system clipboard.

# Save Selected Entries as HAR (HTTP Archive File)

A context menu item to save the selected HTTP messages in HAR format.

# Save Raw Message

Provides a context menu to save content of HTTP messages as binary. (While the files will probably open in a simple editor it may have null characters or malformed bytes.)

# Save XML Message

Provides a context menu to save content of HTTP messages as XML.

# Import HAR (HTTP Archive File)

An option to import messages from a HTTP Archive (HAR), available via the 'Import' menu.

# Import Log File

Allows you to import log files from ModSecurity and files previously exported from ZAP.

# Import URLs

An option to import a file of URLs is available via the 'Import' menu ('Import a File Containing URLs'). The file must be plain text with one URL per line. Blank lines and lines starting with # will be ignored.   

It also supports the [Automation Framework](/docs/desktop/addons/import-export/automation/).

# Export

The add-on also adds a top level "Export" menu, providing the following functionality.

## Export Messages to File...

This allows you to save requests and responses to a text file.   
Select the messages to save in the History tab (including multi-select).

## Export Response to File... This allows you to save a specific responses to a file.
Select the relevant message in the History tab - note that binary responses (such as images) can be saved as well as text responses.

## Export All URLs to File...

This allows you to save all of the URLs accessed to a text or HTML file.   
This can be used, amongst other things, to compare the URLs available to users with different roles or permissions on the same system. (Also consider leveraging the Access Control Testing add-on.) This functionality is also available via the right-click context menu.

## Export Selected URLs to File...

Based on the selection (including multi-select) in the Sites tree all URLs and child URLs of selected nodes are exported. This functionality is also available via the right-click context menu.

## Export URLs for Context

All URLs in the Sites tree that fall within the selected context are exported. This functionality is also available from the right-click menu when used on a Context node in the Sites tree panel.

# ZAP API

This add-on also exposes various ZAP API endpoints to facilitate programmatic use of the functionality.

* `/exim/action/importHar (filePath*)`
* `/exim/action/importModsec2Logs (filePath*)`
* `/exim/action/importUrls (filePath*)`
* `/exim/action/importZapLogs (filePath*)`
* ---
* `/exim/other/exportHar (baseurl start count)`
* `/exim/other/exportHarById (ids*)`
* `/exim/other/sendHarRequest (request* followRedirects)`
