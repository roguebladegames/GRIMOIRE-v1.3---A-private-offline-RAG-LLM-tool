================================================================================
  GRIMOIRE — Local QA Lantern (portable build)
================================================================================

GRIMOIRE is a desktop app for searching and asking questions over your local
documentation and test materials. It runs fully on your machine: documents
are indexed into a local vector store, and answers come from Ollama (not a
cloud API).

The assistant persona is Mothman — short, grounded answers from the archive
only (unless you change the system prompt).


--------------------------------------------------------------------------------
  WHAT YOU NEED
--------------------------------------------------------------------------------

  1. Windows
  2. Ollama installed and running  →  https://ollama.com
  3. Minimum recommended models:

       ollama pull mistral              (chat / answers)
       ollama pull nomic-embed-text     (embeddings / search)

  On startup, GRIMOIRE opens an LLM setup screen:
  - Checks whether Ollama is reachable
  - Lists installed models
  - Lets you choose chat + embedding models (saved for next launch)
  - Optional SYSTEM PROMPT editor (default Mothman prompt kept if unchanged)

  Re-open setup anytime with "LLM models…"
  Edit the directive anytime with "SYSTEM PROMPT"


--------------------------------------------------------------------------------
  FIRST RUN
--------------------------------------------------------------------------------

  1. Install Ollama; pull mistral and nomic-embed-text
  2. Keep this whole app folder together (EXE + _internal + docs)
  3. Double-click GRIMOIRE.exe
  4. Pick models → optional system prompt → Continue
  5. Choose documents folder → check files → Index → chat


--------------------------------------------------------------------------------
  SUPPORTED FILE TYPES
--------------------------------------------------------------------------------

  .pdf   .txt   .md   .docx   .csv

  Notes:
  - Markdown uses the .md extension only.
  - CSV is one row per chunk (column: value) for retrieval.
  - Legacy binary .doc is NOT supported; convert to .docx first.
  - Only files you check and index are embedded.


--------------------------------------------------------------------------------
  HOW TO USE (THREE PANES)
--------------------------------------------------------------------------------

  LEFT — Folder tree + tools
  - Choose Documents Folder…
  - LLM models…  (chat / embed models)
  - SYSTEM PROMPT  (assistant directive; Reset to default available)

  MIDDLE — Files & archive
  - Lists supported files under the selected folder
  - Type checkboxes bulk-select by extension (enabled when files of that
    type are present in the current list)
  - Check files → Index into the local archive

  RIGHT — Chat
  - Enter to send (or click Send)
  - Answers use retrieved context from indexed files only


--------------------------------------------------------------------------------
  INDEX LOCATION
--------------------------------------------------------------------------------

  Index data for a docs folder is stored under:

       <your docs folder>\.grimoire_index\

  Delete that folder to rebuild the archive from scratch.


--------------------------------------------------------------------------------
  PRIVACY
--------------------------------------------------------------------------------

  - Documents and the vector index stay on your machine.
  - Chat goes to local Ollama only.
  - No automatic upload of your archive to the cloud.


--------------------------------------------------------------------------------
  TROUBLESHOOTING
--------------------------------------------------------------------------------

  Chat / connection errors
    → Confirm Ollama is running
    → ollama list  (need chat + embed models)
    → LLM models… → Refresh models

  Empty answers
    → Index the relevant files first
    → Ask with a C-ID, Bug/Issue ID, or clear feature name

  Embedding model changed
    → Re-index for best search quality


================================================================================
  RogueBlade / GRIMOIRE — local documentation QA
================================================================================
