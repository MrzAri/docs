---
title: 'DirectoryEntrySync'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
summary: "This interface represents a directory on a file system.\n"
tags:
  - API_Objects
  - API
  - FileSystemAPI
uri: apis/filesystem/DirectoryEntrySync

---
## Summary

This interface represents a directory on a file system.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

## Properties

*No properties.*

## Methods

[createReader](/apis/filesystem/DirectoryEntrySync/createReader)
:   Creates a new DirectoryReaderSync to read EntrySyncs from this DirectorySync.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[getDirectory](/apis/filesystem/DirectoryEntrySync/getDirectory)
:   Creates or looks up a directory.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[getFile](/apis/filesystem/DirectoryEntrySync/getFile)
:   Creates or looks up a file.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[removeRecursively](/apis/filesystem/DirectoryEntrySync/removeRecursively)
:   Deletes a directory and all of its contents, if any. In the event of an error [e.g. trying to delete a directory that contains a file that cannot be removed], some of the contents of the directory may be deleted. It is an error to attempt to delete the root directory of a filesystem.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

## Events

*No events.*

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
