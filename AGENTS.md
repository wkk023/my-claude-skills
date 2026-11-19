# Instructions for all AI bots

<!-- REPO-FILE-INTAKE-RULE START -->
## Repository file intake rule / 文件入庫規則

User rule, effective 2026-11-19. Applies to every bot/agent saving, uploading, importing or archiving documents into any repository.

1. Before saving a document, inspect the repository's current file list and any document inventory/manifest. Confirm the manifest's scope, completeness and freshness; a file tree or partial manifest is not a complete SHA-256 inventory.
2. Compare SHA-256 of the original file bytes with existing documents, regardless of filenames or folders. An identical SHA-256 means reuse/link the existing file; do not save a duplicate. A filename, Git blob SHA-1, file size or matching extracted text is not a substitute for SHA-256.
3. If the content changed, save an explicitly labelled version (date/revision plus source), record its SHA-256 and relationship to the previous version, and keep the version history. Update the inventory after a successful save.
4. If no suitable inventory exists, or it is incomplete/stale, first tell the user what is missing and propose creating/completing it. Do not claim a complete inventory already exists or silently bypass the prerequisite to save a new document.
5. If an existing binary cannot be retrieved/hashed, report that duplicate checking is incomplete; never describe the file as unique or checked. Do not change repository visibility or permissions to perform this check.

原則：先查清單及 SHA-256；完全相同不重複存；內容有變標明版本；未有清單先提出，不假設已建立。
<!-- REPO-FILE-INTAKE-RULE END -->
