
# Azure File Movement

## AzCopy

CLI to copy files to or from storage account.

## Azure Storage Explorer

GUI to manage files and blobs. Uses AzCopy as a backend.

## Azure File Sync

Bi-directionally synchronises files between a Windows server and Azure files. The Windows server can
act as a cache / CDN.

Azure File Sync provides,
- Any protocol usage
- Ability to have many caches across world
- Configure cloud tiering
    - Store most accessed files locally
    - Infrequent files are kept in cloud until needed.

