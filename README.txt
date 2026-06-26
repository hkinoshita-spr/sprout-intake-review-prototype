Sprout Intake Review 2.0 — Prototype (static build)
====================================================

This folder contains a pre-built static version of the prototype.
No npm install, no node modules needed — just a tiny HTTP server.


HOW TO RUN
----------

Option 1 — one-liner with Node (any recent Node 18+):

    npx serve .

Then open the URL it prints (usually http://localhost:3000).


Option 2 — Python (no Node required):

    python3 -m http.server 8000

Then open http://localhost:8000.


Option 3 — any other static server.

The folder is a plain static SPA. Point any static server at the folder
containing index.html and it just works.


WHAT TO EXPLORE
---------------

The default load is the MetLife LTC scenario (US long-term-care reimbursement).
Switch experiences using the URL query parameter ?experience=<id>:

   ?experience=us-ltc-draft               (default — LTC curation review)
   ?experience=us-ltc-completed           (LTC after submit — review history)
   ?experience=jp-surgery-cholecystectomy (NEW — JP inpatient surgery, K672-2)
   ?experience=tss-decisioning            (TSS Health, 4-stage Kenya outpatient)
   ?experience=ho-covered                 (US Homeowners — coverage check)
   ?experience=real                       (JP Medical claim — multi-doc)

The Settings panel (cog in the document toolbar) also exposes a scenario picker.


NOTES
-----

* Click a field card on the right to navigate the document viewer + show the
  bounding box on the source.
* The Recommendation stage on TSS and the Decisioning stage on JP Surgery
  show the full rule + lineage UI.
* The Final / Coverage stage on JP Surgery shows grouped rule cards.
* Hover the doc thumbnails for per-page review counts.
* All review actions are local-state demos — nothing persists past a reload.
