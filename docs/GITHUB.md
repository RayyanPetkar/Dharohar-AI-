# GitHub copy and local installation

Repository: https://github.com/RayyanPetkar/Dharohar-AI-

## Included

The repository contains the React interface source, FastAPI backend, ingestion and OCR code, conversation/translation/voice services, tests, setup/launch scripts, dependency lockfiles, public source manifests, model checksums, documentation and development evaluation reports.

## Files that stay on the original computer

- `.env` and private credentials. `.env.example` contains configuration names and empty placeholder values only.
- `data/`: downloaded PDF/audio originals, the SQLite archive database, model weights, caches and logs.
- `runtime/`: downloaded platform executables and machine-specific interpreter/process records.
- `.venv/`, `node_modules/` and the generated `frontend/dist/` build. Setup recreates dependencies and builds the interface.
- `work/`, bytecode, test caches and temporary files.

This is the complete application source, not a backup of the populated local archive. Those local files have not been deleted or moved. Keep a separate private backup of the archive and source inputs if you need to preserve the exact installed state. If backing up SQLite while the service is running, use SQLite's backup facility; copying only the main database file can omit pending WAL contents.

## Set up another computer

1. Clone the repository using Git.
2. Follow `SETUP.md` for Python, Node.js and Docker prerequisites and run the setup script. Downloads use the pinned model manifests.
3. Keep `.env` private. Configure a provider key only when cloud features are wanted; the template defaults to local providers.
4. Supply the corrected writing PDFs and debate-link CSVs, update the source-folder setting in `scripts/import_archive.py`, and run the import and processing scripts. Public provenance/manifests are in `sources/`.
5. Start the application and open http://127.0.0.1:8010.

Publishing this repository does not host the application. It also does not grant redistribution rights to archive recordings or downloaded voice models. Individual assets retain their existing terms; no blanket project licence has been added automatically.
