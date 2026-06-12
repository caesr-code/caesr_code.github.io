ORION — RUN INSTRUCTIONS
=========================

This folder contains everything Orion needs:
  - Orion_Author_1_4.html   (the app)
  - orion_single.onnx       (model, weights included — single file)
  - vocab.json              (188-word core vocabulary)
  - training_corpus.txt     (fallback corpus for text generation)
  - brain/                  (genre-specific corpora used to steer style)
  - host_orion.py           (local server, works on Mac/Windows/Linux)
  - start_orion.command     (Mac double-click launcher)
  - start_orion.pyw         (Windows double-click launcher)

IMPORTANT: Do NOT double-click the HTML file directly. Browsers block
local file loading (fetch) when opened as file://, which causes errors
like:
    SyntaxError: ... "<!DOCTYPE " ... is not valid JSON

You must run a local server first (see below), then open the page
through http://localhost:8000/...


WINDOWS
-------
Requires Python 3 installed (https://python.org — check "Add to PATH"
during install).

Double-click "start_orion.pyw".
  - This starts a local server in the background and opens your
    default browser to http://localhost:8000/Orion_Author_1_4.html
  - No console window will appear (this is normal).
  - To stop the server, find and close the "python" process in Task
    Manager, or just close all browser tabs and restart your PC later.

If double-clicking does nothing, open Command Prompt in this folder
and run:
    python host_orion.py


MAC
---
Double-click "start_orion.command".
  - If macOS blocks it: right-click -> Open -> "Open anyway"

Or manually:
    python3 host_orion.py


LINUX / MANUAL (ANY OS)
------------------------
Open a terminal in this folder and run:
    python3 host_orion.py

Then open the printed URL (http://localhost:8000/Orion_Author_1_4.html)
in your browser.


WHAT TO EXPECT
--------------
On the welcome screen you should see:
    "✅ Orion's brain is ready (188 words ...)"

This can take a few seconds the first time, since the ~18MB model
needs to load into the browser.

To stop the server: press Ctrl+C in the terminal window (Mac/Linux),
or close the python process (Windows).
