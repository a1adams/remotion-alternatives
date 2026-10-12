# Remotion Alternatives: 8 Video Frameworks and APIs Compared (2026)

This list compares 8 Remotion alternatives, each checked against its vendor's own docs on 11 October 2026 and ranked by how little rendering code and infrastructure it leaves you to own. Wireflow is first because its Video Editor node is Remotion-based and renders on hosted compute. Of the 8 entries, 4 are hosted services and 4 are MIT-licensed libraries you run yourself.

1. **Wireflow**: Best overall for generating the footage and hosting the render, a node canvas with a Remotion-based editor node
2. **Shotstack**: Best for developers who keep video as JSON, a hosted editing API with AI generation in the render
3. **Creatomate**: Best for many versions of one designed template, a template editor with a REST API
4. **JSON2Video**: Best for narrated and captioned clips from data, a REST API that renders movie JSON
5. **Revideo**: Best for keeping video as code under a permissive licence, an MIT TypeScript framework with headless rendering
6. **Motion Canvas**: Best for hand-built explainer animations, an MIT TypeScript library with a live editor
7. **Editly**: Best for cutting existing clips from one spec file, an MIT tool built on Node.js and ffmpeg
8. **FFCreator**: Best for slideshow-style short videos, an MIT Node.js library with ready-made transitions

The Wireflow team maintains this list, so read entry 1 with that in mind. [Wireflow's AI video workflow page](https://www.wireflow.ai/features/ai-video-workflow) shows the product in the vendor's own words, and every other entry links to its vendor's pages so that each cell can be checked.

The tables below are generated from [`data/tools.json`](data/tools.json). Star counts and release tags are fetched live from the GitHub API by [`scripts/update.js`](scripts/update.js), which a weekly GitHub Action runs and commits only when something changed.

<!-- LAST-CHECKED:START -->
Live repository data last checked **2026-10-12** by [`scripts/update.js`](scripts/update.js), which runs weekly via GitHub Actions.
<!-- LAST-CHECKED:END -->

Maintained by [a1adams](https://github.com/a1adams). Corrections are welcome, see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [The data](#the-data)
- [Capability scores](#capability-scores)
- [Comparison table](#comparison-table)
- [The tools](#the-tools)
  - [Wireflow](#1-wireflow)
  - [Shotstack](#2-shotstack)
  - [Creatomate](#3-creatomate)
  - [JSON2Video](#4-json2video)
  - [Revideo](#5-revideo)
  - [Motion Canvas](#6-motion-canvas)
  - [Editly](#7-editly)
  - [FFCreator](#8-ffcreator)
- [Remotion, the baseline](#remotion-the-baseline)
- [What each check means](#what-each-check-means)
- [How this list is maintained](#how-this-list-is-maintained)
- [FAQ](#faq)
- [Contributing](#contributing)
- [License](#license)

## The data

One row per tool, one column per thing people actually check before committing. Columns with nothing verified behind them are dropped rather than filled with guesses.

<!-- DATA-TABLE:START -->
| Tool | REST API | Free tier | Pricing | Open-source SDK / MCP |
|---|---|---|---|---|
| **[Wireflow](#1-wireflow)** | Yes | [check](https://www.wireflow.ai/pricing) | [pricing](https://www.wireflow.ai/pricing) | n/a |
| **[Shotstack](#2-shotstack)** | Yes | [check](https://shotstack.io/pricing/) | [pricing](https://shotstack.io/pricing/) | n/a |
| **[Creatomate](#3-creatomate)** | Yes | [check](https://creatomate.com/pricing) | [pricing](https://creatomate.com/pricing) | [Creatomate/creatomate-node](https://github.com/Creatomate/creatomate-node), 9 ★, 1.2.1 |
| **[JSON2Video](#4-json2video)** | Yes | Yes | [pricing](https://json2video.com/pricing/) | [JSON2Video/json2video-nodejs-sdk](https://github.com/JSON2Video/json2video-nodejs-sdk), 22 ★, v2.0.4 |
| **[Revideo](#5-revideo)** | n/a | Yes | n/a | [midrender/revideo](https://github.com/midrender/revideo), 4,098 ★, pushed 2026-07-15 |
| **[Motion Canvas](#6-motion-canvas)** | n/a | Yes | n/a | [motion-canvas/motion-canvas](https://github.com/motion-canvas/motion-canvas), 19,293 ★, v3.17.2 |
| **[Editly](#7-editly)** | n/a | Yes | n/a | [mifi/editly](https://github.com/mifi/editly), 5,523 ★, v0.15.0-rc.1 |
| **[FFCreator](#8-ffcreator)** | n/a | Yes | n/a | [tnfe/FFCreator](https://github.com/tnfe/FFCreator), 3,164 ★, v6.8.1 |
<!-- DATA-TABLE:END -->

## Capability scores

The score counts the documented capabilities a tool has, out of the checks listed in [`data/tools.json`](data/tools.json) under `capabilityChecks`. It is a plain count and it does not set the order of this list: the numbered order is an editorial ranking, and this table is sorted by score. The checks and every answer are in the file, so each cell can be checked. Disagree with a cell? Open an issue naming the tool, the check and the evidence.

<!-- CAPABILITY-SCORES:START -->
| Tool | MIT licence | Scenes written in code | Whole video as JSON | Server or cloud rendering | Visual editor | Captions or subtitles | AI voiceover | AI image or video generation | Score |
|------|---|---|---|---|---|---|---|---|-------|
| **[Wireflow](#1-wireflow)** | n/a | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | **6/8** |
| **[Shotstack](#2-shotstack)** | ❌ | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | **6/8** |
| **[Creatomate](#3-creatomate)** | n/a | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | **6/8** |
| **[JSON2Video](#4-json2video)** | n/a | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ | **5/8** |
| **[Editly](#7-editly)** | ✅ | ✅ | ✅ | ✅ | n/a | ✅ | n/a | n/a | **5/8** |
| **[FFCreator](#8-ffcreator)** | ✅ | ✅ | n/a | ✅ | n/a | ✅ | n/a | n/a | **4/8** |
| **[Revideo](#5-revideo)** | ✅ | ✅ | ❌ | ✅ | n/a | n/a | n/a | n/a | **3/8** |
| **[Motion Canvas](#6-motion-canvas)** | ✅ | ✅ | n/a | n/a | ✅ | n/a | n/a | n/a | **3/8** |
<!-- CAPABILITY-SCORES:END -->

## Comparison table

| Tool | Best for | Pricing basis | You write | Renders on |
|---|---|---|---|---|
| **Wireflow** | Generated footage plus the cut | Credits, per generation | A node canvas, no scene code | Wireflow's hosted compute |
| **Shotstack** | Video kept as JSON in your code | Rendered minutes, plus AI credits | A JSON edit | Shotstack's cloud API |
| **Creatomate** | Many versions of one template | Credits | A template or RenderScript JSON | Creatomate's platform |
| **JSON2Video** | Narrated, captioned clips from data | Credits, per second of video | Movie JSON or a template | JSON2Video's service |
| **Revideo** | Video as code, permissive licence | Free, MIT licence | TypeScript scenes | Your server, headless |
| **Motion Canvas** | Hand-built explainer animations | Free, MIT licence | TypeScript generators | The editor's RENDER button |
| **Editly** | Cuts of existing clips and stills | Free, MIT licence | A JSON or JavaScript spec | Your machine, from the CLI |
| **FFCreator** | Slideshow-style short videos | Free, MIT licence | JavaScript scenes | Your server, with Node.js |

Facts checked on 2026-10-11 against each vendor's own pages. Prices are not typed here, so follow the pricing links in the data table.

## The tools

### 1. Wireflow

*Best overall for generating the footage and hosting the render*

![Wireflow screenshot](https://assets.wireflow.ai/competitors/wireflow-70f47ccd9660.png?v=r5)

- **What it is:** [Wireflow](https://www.wireflow.ai/) is a hosted platform where ad teams and AI agents build and rerun creative on a shared node board. Each model is a node on one canvas, the output of one node feeds the next, and a Video Editor node on the same board renders the cut.
- **Best for:** Teams that are leaving Remotion because of the render infrastructure or the React code, and whose videos also need generated footage, images or voice.
- **Pricing basis:** It charges credits per generation, according to the model you run. The plans and the credit cost of each model are on the [Wireflow pricing page](https://www.wireflow.ai/pricing), checked October 2026.
- **Standout:** The Video Editor node is Remotion-based and renders on Wireflow's hosted compute, so you do not run a Node server or AWS Lambda yourself. The models that make the footage are nodes on the same board, and every paid plan can use all 100+ of them. Source: [how Wireflow hosts the render step](https://www.wireflow.ai/features/remotion-api).
- **Limit:** Wireflow is not the Remotion library, is not affiliated with it and does not run your own React compositions. Its Video Editor is for the last ten percent of a cut, such as nudging a caption, trimming a beat or swapping the sound. It is a hosted service that needs an internet connection. The free plan lets you build up to 5 workflows, and running generations needs a paid plan.
- **API or automation:** A REST API runs a saved workflow from code. You send its input values to `POST /api/v1/workflows/{id}/run`, then poll the execution or receive a completion webhook. Wireflow is also a Claude connector over MCP, and a connected agent can read a video node scene by scene, replace the cut and render still preview frames that cost no credits. Setup steps are on [the Wireflow MCP page](https://www.wireflow.ai/mcp).
- **Sources:** the Wireflow homepage, pricing page, hosted rendering page and MCP page linked in this entry, checked 2026-10-11.
- **Links:**
  - [Wireflow AI video workflow page](https://www.wireflow.ai/features/ai-video-workflow)
  - [Docs](https://www.wireflow.ai/docs/api/overview)

Pick Wireflow when one board should generate the footage, hold the cut and render it, and when a person, an agent and your own code all need to run it. If your reason for leaving Remotion is the licence and you still want scenes as code, start at entry 5.

Add the Wireflow connector to Claude Code, from the wireflowINC/skills README. Then run /mcp to sign in.
```bash
claude mcp add --transport http wireflow https://www.wireflow.ai/api/mcp
```
Or run a saved workflow from code: send its input values to this endpoint with an API key, then poll the execution. The request format is in the API reference linked under Docs.
```text
POST /api/v1/workflows/{id}/run
```

### 2. Shotstack

*Best for developers who keep video as JSON*

![Shotstack screenshot](https://assets.wireflow.ai/competitors/shotstack-20773e3dbcf5.png?v=r5)

- **What it is:** [Shotstack](https://shotstack.io/) is a cloud video editing API. Every video starts as an edit, which is JSON that describes the timeline, tracks and clips, and you POST that edit to a render endpoint. Its Studio shows the same edit on a visual timeline.
- **Best for:** Developers who want the whole video described as data in their own codebase, with the rendering handed to a hosted API.
- **Pricing basis:** It charges for minutes of rendered video, bought pay as you go or on a monthly plan, and AI generation is charged per model in credits. See the [Shotstack pricing page](https://shotstack.io/pricing/), checked October 2026.
- **Standout:** Video, image, speech and music assets can be generated from a text prompt inside a render. Generation runs on your Shotstack API key and credits, so there is no separate AI provider account to open. Source: [Shotstack's generative AI guide](https://shotstack.io/docs/guide/generating-assets/generative-ai/).
- **Limit:** Pay as you go and the Starter plan are capped at 1080p and include no team seats. The Studio SDK source is published under the PolyForm Shield License 1.0.0, which has a noncompete section, so it is not a permissive open-source licence. Source: [the Studio SDK licence file](https://github.com/shotstack/shotstack-studio-sdk/blob/main/LICENSE).
- **API or automation:** A REST API renders the JSON edit. SDKs exist for Node.js, Python, PHP and Ruby, and there are integrations for Make, Zapier and n8n. Captions can be animated word by word and generated from the audio, as the [rich captions guide](https://shotstack.io/docs/guide/architecting-an-application/rich-captions/) describes.
- **Note:** No repository is listed for Shotstack in the data table, because its Studio SDK source is under the PolyForm Shield License 1.0.0 (see Limit).
- **Sources:** [Shotstack core concepts](https://shotstack.io/docs/guide/getting-started/core-concepts/), checked 2026-10-11.

Pick Shotstack over Wireflow when you want one JSON document per video in your own repository and you do not need a node canvas.

Render a JSON edit in the sandbox, from Shotstack's Hello World guide. The file hello.json is the edit from that guide.
```bash
curl -X POST \
  -H "Content-Type: application/json" \
  -H "x-api-key: $SHOTSTACK_API_KEY" \
  -d @hello.json \
  https://api.shotstack.io/edit/stage/render
```

### 3. Creatomate

*Best for many versions of one designed template*

![Creatomate screenshot](https://assets.wireflow.ai/competitors/creatomate-7a17a26bb658.png?v=r5)

- **What it is:** [Creatomate](https://creatomate.com/) is a platform for creating videos and images through automation. You design a template in its online editor, then fill it through a REST API, a spreadsheet or a no-code tool.
- **Best for:** Developers and no-code teams that produce many versions of one designed template.
- **Pricing basis:** It charges credits, and one image is always one credit. The credits for a video depend on its resolution, frame rate and length. A free trial has 50 credits with no card. See the [Creatomate pricing page](https://creatomate.com/pricing), checked October 2026.
- **Standout:** The API is available on every plan, and a template can also be written directly as RenderScript, a JSON-based format that describes the whole video. Source: [Creatomate's RenderScript page](https://creatomate.com/docs/fundamentals/getting-started/what-is-render-script).
- **Limit:** AI speech and image steps run on your own provider keys (ElevenLabs, OpenAI or Stability AI), which you set in the project settings. Rendered files are hosted for up to 30 days and then deleted. Source: [Creatomate's AI provider notes](https://creatomate.com/llms/providers.md).
- **API or automation:** A REST API renders a template with modifications or a full RenderScript document, and there are official integrations for Zapier, Make and n8n. Subtitles are generated at render time, as the [subtitle reference](https://creatomate.com/llms/subtitles.md) describes.
- **Note:** The linked repository is the official Node.js SDK. Rendering is a hosted service.
- **Sources:** [Creatomate introduction](https://creatomate.com/docs/fundamentals/getting-started/introduction), checked 2026-10-11.
- **Links:**
  - [Creatomate/creatomate-node](https://github.com/Creatomate/creatomate-node)

Pick Creatomate over Shotstack when a designer should own the template in a visual editor and the data comes from a spreadsheet or a no-code tool.

Render a template with modifications, from the example on the Creatomate homepage. Use your own template ID and API key.
```bash
curl -X POST https://api.creatomate.com/v2/renders \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer API_KEY" \
  -d '{
    "template_id": "58c1163e-f250-49df-b98d-e8c4aad01a2d",
    "modifications": {
      "Title": "Your Text And Video Here",
      "Title.fill_color": "#4980f1",
      "Background-Video": "https://example.com/video.mp4"
    }
  }'
```

### 4. JSON2Video

*Best for narrated and captioned clips from data*

![JSON2Video screenshot](https://assets.wireflow.ai/competitors/json2video-601b1388401f.png?v=r5)

- **What it is:** [JSON2Video](https://json2video.com/) is a REST API that creates and edits videos from JSON. You submit a movie made of scenes and elements, or a saved template with variables, and get back a rendered MP4.
- **Best for:** Developers who build templated videos with subtitles and voiceovers from code.
- **Pricing basis:** It charges credits per second of rendered video, on a free plan, pre-paid plans and subscription plans. See the [JSON2Video pricing page](https://json2video.com/pricing/), checked October 2026.
- **Standout:** Voiceover and subtitles are element types in the same JSON as the video. A voice element turns text into speech with Azure or ElevenLabs voices, and a subtitles element adds automatic captions. Source: [the JSON2Video API overview](https://json2video.com/llms.txt).
- **Limit:** The pricing page says JSON2Video does not natively support AI image generation, AI video generation, avatar generation or face-swap. Videos made on the free plan carry a watermark.
- **API or automation:** A REST API takes the movie JSON and returns a project ID to poll. SDKs are listed for PHP and Node.js, with no-code integrations for Make, Zapier, n8n and Pabbly, and templates can also be changed in the [JSON2Video visual editor](https://json2video.com/tools/visual-editor/).
- **Note:** The linked repository is the official Node.js SDK. Rendering is a hosted service.
- **Sources:** [JSON2Video getting started docs](https://json2video.com/docs/v2/getting-started), checked 2026-10-11.
- **Links:**
  - [JSON2Video/json2video-nodejs-sdk](https://github.com/JSON2Video/json2video-nodejs-sdk)

Pick JSON2Video over Creatomate when the job is narrated, captioned clips made from data and one small JSON schema is enough.

Create a video from movie JSON, from the JSON2Video API overview. The response returns a project ID to poll.
```bash
curl -X POST https://api.json2video.com/v2/movies \
  -H "x-api-key: YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "resolution": "full-hd",
    "scenes": [{
      "elements": [{
        "type": "video",
        "src": "https://example.com/video.mp4"
      }]
    }]
  }'
```

### 5. Revideo

*Best for keeping video as code under a permissive licence*

![Revideo screenshot](https://assets.wireflow.ai/competitors/revideo-6014707564e6.png?v=r5)

- **What it is:** [Revideo](https://midrender.com/revideo) is an open-source TypeScript framework for creating and editing videos in code. Its own page describes it as a fork of Motion Canvas, entry 6 on this list, that adds headless rendering, audio support and a library-first API.
- **Best for:** Developers who are leaving Remotion because of its licence and still want scenes as code, rendered on their own infrastructure.
- **Pricing basis:** It is free and open source under the MIT licence, and no price is published for the framework. Source: [the Revideo licence file](https://github.com/midrender/revideo/blob/main/LICENSE).
- **Standout:** Rendering is headless, so `renderVideo()` renders a project to a file and the CLI can expose a render endpoint from your project. The README says it runs anywhere Node and a headless browser run, including serverless platforms such as Google Cloud Run. Source: [the Revideo README](https://github.com/midrender/revideo).
- **Limit:** The team behind Revideo now works mainly on Midrender, a separate visual editor built on the same engine, and recent engine changes have not yet been upstreamed to the open-source repository. The README describes a preview player, not a visual editor, and captions are not documented.
- **API or automation:** It has a TypeScript API (`renderVideo()` and `renderPartialVideo()`) and a render endpoint that you host yourself. It counts rendered videos through anonymous telemetry unless you set `DISABLE_TELEMETRY=true`.
- **Note:** The repository moved from redotvideo/revideo to midrender/revideo. It has no tagged GitHub release, so the data table shows the date of the last push.
- **Sources:** [Revideo documentation](https://midrender.com/revideo/docs), checked 2026-10-11.

Pick Revideo over the hosted entries above when the code has to stay yours under a permissive licence. Check the recent activity in its repository first, because development has moved to Midrender.

Create a project, from the Revideo README.
```bash
npm init @revideo@latest
```

### 6. Motion Canvas

*Best for hand-built explainer animations*

![Motion Canvas screenshot](https://assets.wireflow.ai/competitors/motion-canvas-93840e46f7d6.png?v=r5)

- **What it is:** [Motion Canvas](https://motion-canvas.io/) is a TypeScript library for creating animated videos with the Canvas API, with an editor that previews the animation in real time.
- **Best for:** Developers who script informative vector animations in code and synchronize them with a voice-over.
- **Pricing basis:** It is free and open source under the MIT licence. Source: [the Motion Canvas licence file](https://github.com/motion-canvas/motion-canvas/blob/main/LICENSE).
- **Standout:** Animations are written as TypeScript generator functions, and a web-based editor syncs them with audio and lets you edit certain aspects of the animation by hand. Source: [the Motion Canvas README](https://github.com/motion-canvas/motion-canvas).
- **Limit:** Rendering starts from the RENDER button in the editor's Video Settings tab. The [Motion Canvas rendering docs](https://motion-canvas.io/docs/rendering/) describe no headless or cloud render, and captions and AI steps are not documented.
- **API or automation:** An API for automated renders is not published. The docs describe a project scaffold (`npm init @motion-canvas@latest`), a built-in image sequence exporter and an FFmpeg video exporter, all used from the editor.
- **Sources:** [Motion Canvas quickstart](https://motion-canvas.io/docs/quickstart/), checked 2026-10-11.

Pick Motion Canvas over Revideo when a person will craft each animation and watch it in the editor. Pick Revideo when a server has to render with nobody clicking a button.

Scaffold a project, from the Motion Canvas quickstart. It asks for Node.js version 16 or greater.
```bash
npm init @motion-canvas@latest
```

### 7. Editly

*Best for cutting existing clips from one spec file*

![Editly screenshot](https://assets.wireflow.ai/competitors/editly-e2d8693cc43d.png?v=r5)

- **What it is:** [Editly](https://github.com/mifi/editly) is a tool and framework for declarative video editing with Node.js and ffmpeg. You describe the whole edit as a JSON or JavaScript spec and run it from a CLI or a JavaScript API.
- **Best for:** Developers who script simple edits from clips, images, audio and titles and already run their own servers.
- **Pricing basis:** It is free and open source under the MIT licence, and the README says the project will always remain free and open source.
- **Standout:** The whole edit is one JSON or JSON5 file that the CLI turns into an MP4 or a GIF. It has a subtitle layer type, and the README lists automatic audio crossfading, ducking and normalization.
- **Limit:** It needs Node.js with ffmpeg and ffprobe on the PATH, and Linux servers may need extra steps for headless-gl. The README says the project is maintained by one person, and it documents no visual editor.
- **API or automation:** It has a CLI (`editly my-spec.json5`) and a JavaScript API. You run it on your own machine or server, and the README documents a Docker setup.
- **Sources:** the Editly README linked above and [the Editly licence file](https://github.com/mifi/editly/blob/master/LICENSE), checked 2026-10-11.

Pick Editly over Revideo when the video is a cut of existing clips and stills, and one JSON file is enough to describe it.

Install, then render from a JSON5 edit spec, from the Editly README. It needs ffmpeg and ffprobe on the PATH.
```bash
npm i -g editly
editly my-spec.json5 --fast --keep-source-audio --out output.gif
```

### 8. FFCreator

*Best for slideshow-style short videos*

![FFCreator screenshot](https://assets.wireflow.ai/competitors/ffcreator-234eadffb08e.png?v=r5)

- **What it is:** [FFCreator](https://github.com/tnfe/FFCreator) is a lightweight Node.js library for building short videos from pictures, music, video clips and text.
- **Best for:** Developers who render album or slideshow videos in Node.js without a hosted service.
- **Pricing basis:** It is free and open source under the MIT licence.
- **Standout:** It includes nearly 100 scene transition effects and converts most animate.css effects into video. It also has subtitle and chart components.
- **Limit:** It needs Node.js and a regular FFmpeg install, and a server without a display must start it with `xvfb-run`. A drag-and-drop builder and an AI video generator exist only as separate projects that the README links to.
- **API or automation:** It has a JavaScript API, in which you build scenes from `FFScene`, `FFImage`, `FFText` and `FFVideo` objects and call `creator.start()`. A REST API is not published for it.
- **Sources:** the FFCreator README linked above and [the FFCreator documentation site](https://tnfe.github.io/FFCreator/), checked 2026-10-11.

Pick FFCreator over Editly when ready-made transitions and animation presets matter more than a JSON spec. Check its latest release in the data table before you commit to it.

Install the package, from the FFCreator README. It needs a regular FFmpeg install.
```bash
npm install ffcreator --save
```

## Remotion, the baseline

Remotion is the framework this list is measured against, so it is described here and not ranked. These lines come from Remotion's own pages, checked 2026-10-11.

- **What it is:** [Remotion](https://www.remotion.dev/) is a framework for creating videos and motion graphics with React.
- **Licence:** It uses its own Remotion License, not the MIT licence. The file says free use covers "an individual", "a for-profit organization with up to 3 employees" and non-profits, and that "a company license is required for for-profit organizations of a certain size". It also says the licence will change slightly in Remotion 5.0. Source: [the Remotion licence file](https://github.com/remotion-dev/remotion/blob/main/LICENSE.md).
- **Rendering:** You render from Remotion Studio or the CLI, through a server-side rendering API, on AWS Lambda, in a GitHub Action, or on Google Cloud Run in an alpha version, as the [Remotion render docs](https://www.remotion.dev/docs/render) list.
- **Captions:** Captions and subtitles are documented, with the `@remotion/captions` package. Source: [the Remotion captions docs](https://www.remotion.dev/docs/captions/).
- **Visual editing:** Remotion Studio previews the video and can render it, and the Editor Starter is a template you buy to build your own editor. Source: [the Editor Starter docs](https://www.remotion.dev/docs/editor-starter).

## What each check means

A check means the vendor's own source documents it. A cross means the source says it works another way. A dash means not published, or not verified for this list, which is not proof that it is absent.

- **MIT licence:** The source code is published under the MIT licence. A cross means the vendor publishes source under a licence with added conditions. A hosted service with no published source gets a dash.
- **Scenes written in code:** You write the video as JavaScript or TypeScript code.
- **Whole video as JSON:** The full edit can be sent as one JSON document, with no scene code to write.
- **Server or cloud rendering:** The docs describe rendering with nobody in a desktop app or an editor, on your own server or on the vendor's cloud.
- **Visual editor:** The product ships an editor where you change the video visually, not only a preview player.
- **Captions or subtitles:** Captions or subtitles are a documented, built-in feature.
- **AI voiceover:** Text to speech is documented as a step inside the product.
- **AI image or video generation:** The product can generate images or video clips inside a render or a workflow.

## How this list is maintained

Every cell comes from the vendor's own docs, pricing page, README or licence file, last checked on 11 October 2026. The numbered order is editorial and uses 4 checks: who hosts the render, what you have to write, whether media generation is included, and how recently the repository was pushed to. Entries that leave you the least rendering code and infrastructure to own come first. The capability score is a separate plain count of documented checks, and it does not set the order. Nothing here was benchmarked, so no render was timed and no price was tested.

Remotion is the baseline and is not ranked. The list is capped at 8 entries that each render a complete video from code, JSON or a canvas, and anything we had not checked against vendor docs by that date is left out.

To correct a cell, open an issue or a pull request with the tool, the check and a link to the vendor page that proves it. PRs are welcome, including corrections to entry 1. A longer written comparison is on the Wireflow blog, which covers [eight Remotion API tools](https://www.wireflow.ai/blog/best-remotion-api-tools-in-2026).

- [`data/tools.json`](data/tools.json) is the source of truth. The tables in this README are generated from it and are overwritten on every run, so edit the JSON, not the tables.
- [`scripts/update.js`](scripts/update.js) fetches star counts and latest release tags from the GitHub API for the tools that publish an official repo, stamps the check date, and regenerates the tables. `--offline` regenerates without the network; `--check` exits non-zero if the README has drifted from the data.
- [`.github/workflows/refresh.yml`](.github/workflows/refresh.yml) runs it weekly and on manual dispatch, and commits only when the data actually changed.
- Prices are deliberately not stored as numbers. A stale price in a comparison table is worse than no price, so the table links to each vendor's own pricing page.

## FAQ

<details>
<summary><strong>What is the best Remotion alternative?</strong></summary>

It depends on why you are leaving Remotion. If the reason is the company licence and you still want scenes as code, Revideo and Motion Canvas are MIT-licensed. If the reason is render infrastructure, the 4 hosted entries render for you, and Wireflow is listed first because its editor node is Remotion-based.

</details>

<details>
<summary><strong>Is Remotion free?</strong></summary>

Remotion is free for some users and paid for others. Its licence file says an individual, a for-profit organization with up to 3 employees and a non-profit can use it for free, and other organizations need a company licence. Read the licence itself before you decide.

</details>

<details>
<summary><strong>What is the closest open source alternative to Remotion?</strong></summary>

Revideo is the closest on this list. Scenes are TypeScript, rendering is headless and the licence is MIT. Its team now works mainly on Midrender, so check the recent activity in the repository first. Motion Canvas is the other MIT option when a person will craft each animation in an editor.

</details>

<details>
<summary><strong>Can I replace Remotion without writing code?</strong></summary>

Yes, the 4 hosted entries each have a visual editor. Creatomate and JSON2Video have visual template editors, the Shotstack Studio shows the edit on a timeline, and Wireflow builds the video on a node canvas. Each of the 4 also has a REST API for the day you want to automate the work.

</details>

<details>
<summary><strong>Do I have to run my own render pipeline?</strong></summary>

You only run your own pipeline with the 4 open-source libraries. Revideo, Motion Canvas, Editly and FFCreator run on your own machine or server, while Wireflow, Shotstack, Creatomate and JSON2Video render on the vendor's infrastructure and return a file. The Wireflow blog has [a guide to rendering without self-hosting](https://www.wireflow.ai/blog/best-remotion-without-self-hosting-tools-in-2026).

</details>

<details>
<summary><strong>Do any of these generate the video content itself?</strong></summary>

Three of the 8 document it. Wireflow has image and video model nodes on the same board, Shotstack generates assets from a prompt inside a render, and Creatomate generates images on your own provider keys. The JSON2Video pricing page says it does not natively support AI image or video generation.

</details>

<details>
<summary><strong>Does Wireflow run my Remotion React code?</strong></summary>

No, Wireflow does not run Remotion code. It is not the Remotion library and does not run your own React compositions. Its Video Editor node is Remotion-based, and you work on it from the board or through the connector. If you have a Remotion codebase to keep, stay on Remotion, and this guide covers [where to find Remotion templates](https://www.wireflow.ai/blog/remotion-templates).

</details>

## The short version

Pick Wireflow when the footage has to be generated as well as cut and you want the render hosted. Pick Shotstack, the next entry, when you would rather keep each video as a JSON document in your own code. If the licence is the only problem and you want to keep writing code, go to Revideo or Motion Canvas. Before you commit, rebuild one real video in your two finalists and note what a text change costs you in each. For the first option, the next page to read is [a worked text to video example](https://www.wireflow.ai/features/remotion-alternative).

## Contributing

Corrections and additions are welcome, including corrections to the entry for the tool that maintains this list. Open an issue with the tool name, a working link, one line on what it does that the tools already listed do not, and one line on where it stops. Entries are judged on whether they are usable today, not on popularity. Full rules in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC0 1.0 Universal](LICENSE), public domain. Take the data, fork the list, no attribution required.

---

Maintained by [a1adams](https://github.com/a1adams).
