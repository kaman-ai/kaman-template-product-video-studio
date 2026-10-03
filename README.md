# Product Video Studio

The app of the **Product Video Studio** template in the Kaman marketplace.

A video producer agent that turns a short brief, and optionally a product photo, into a finished narrated video: it writes the script, voices every scene with the platform's text-to-speech, builds 3D scenes with Remotion and three.js, renders an MP4 in the sandbox and shows it in the chat. Ads, explainers, launch teasers; 16:9, 9:16 or 1:1.

It is installed as a code project of yours when you install the template,
and it is a thin layer: the work is done by the template's agents and
workflow, on your own systems through the connections you chose at install.

## How it is wired

`kaman.app.json` names the agents and workflow the app uses, and the
actions it offers. The ids in this repository are the template's own.
**Install rewrites the file**: each id becomes the id of your installed
copy. Nothing else is rewritten.

The app talks to Kaman only from its server route (`app/api/action/[id]`),
through `@yoctotta/kaman-sdk/app`, with `KAMAN_BASE_URL` and
`KAMAN_API_KEY` — which a Kaman preview injects. The key never reaches the
browser.

## Publishing a new version

Push here, then republish the template pinned to the new commit. Installs
always take the pinned commit, never the tip of `main`.
