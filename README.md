# GRIMOIRE-v1.3---A-private-offline-RAG-LLM-tool
GRIMOIRE is a fully local, offline desktop application for searching and chatting with your personal documents. It indexes your files into a local vector store and uses Ollama (with Mistral) to generate grounded answers — no cloud, no data leaving your machine. It is designed as a portable app — just unzip and run. No Python installation required.

Originally started building this to handle my own private data and projects without the use of clouds or subscriptions to talk to my docs. 
As a QA professional, this tool is intended to be used as a way to identify gaps in test coverage, documentation, and even make suggestions for improvements.

GRIMOIRE can be used for ANY purposes. Private data, finances, project details, etc... Whatever you feed GRIM will becomes it's brain, you have full control of the system prompt to decided how efficient it is.

You can select your choice of LLM and embedding LLM upon launching the app. 
You can change these at any time while GRIM is open. This allows you to change models and edit it's system prompt without too much interruption. 
Depending on your LLMs directives and guard rails, it will respond with upmost efficiency.

I built this tool with the intention of making it work really well with smaller LLMs, such as Mistral, to prove they can still be efficient without all the extra billions in parameters.

If you want to keep this small in size, my recommended LLMs are
- Mistral
- nomic-embed-text
