
<div align="center">

# AnnotAI Viewer

### A multilingual browser-based viewer, annotator, presenter, URL loader, and launcher for documents, media, AI tools, and social platforms.

<p>
  <strong>Open files. Load URLs. Annotate visually. Present ideas. Launch AI and media platforms from one floating workspace.</strong>
</p>

<p>
  <img src="https://img.shields.io/badge/Use%20in-Browser-2563eb?style=for-the-badge" alt="Use in Browser">
  <img src="https://img.shields.io/badge/No%20Desktop%20Install-16a34a?style=for-the-badge" alt="No Desktop Install">
  <img src="https://img.shields.io/badge/Documents-PDF%20%7C%20DOCX%20%7C%20XLSX%20%7C%20TXT-f59e0b?style=for-the-badge" alt="Documents">
  <img src="https://img.shields.io/badge/Tools-Annotation%20%7C%20Presentation%20%7C%20AI%20Launchers-7c3aed?style=for-the-badge" alt="Tools">
</p>

</div>

---

## Overview

**AnnotAI Viewer** is a lightweight web app that runs directly in a browser. It combines document viewing, media preview, visual annotation, presentation support, URL loading, multilingual interface controls, and quick launchers for popular English and Chinese AI and social platforms.

Instead of switching between several apps, users can work from one floating panel to:

- open local files,
- paste and load URLs,
- draw on top of documents or media,
- highlight important areas,
- use a laser pointer during presentation,
- zoom in and out,
- save annotations as JSON,
- reload annotation JSON later,
- export annotated views as PNG where supported,
- launch AI tools and social/media platforms.

AnnotAI Viewer is suitable for:

<table>
  <thead>
    <tr>
      <th>User group</th>
      <th>Example uses</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Teachers and educators</td>
      <td>Present worksheets, annotate PDFs, explain diagrams, and use a laser pointer during lessons.</td>
    </tr>
    <tr>
      <td>Students and learners</td>
      <td>Read lecture notes, highlight important points, annotate study materials, and open AI tools for explanations.</td>
    </tr>
    <tr>
      <td>Researchers and academics</td>
      <td>Review papers, mark citations, inspect data files, and open research URLs.</td>
    </tr>
    <tr>
      <td>Business users</td>
      <td>Review reports, annotate proposals, present spreadsheets, and mark charts during meetings.</td>
    </tr>
    <tr>
      <td>Designers and creative teams</td>
      <td>Review screenshots, annotate images, mark design changes, and export visual feedback.</td>
    </tr>
    <tr>
      <td>Content creators</td>
      <td>Review media files, compare social platforms, annotate video frames, and prepare content ideas.</td>
    </tr>
    <tr>
      <td>Multilingual teams</td>
      <td>Switch interface languages, compare multilingual content, and open English or Chinese AI tools.</td>
    </tr>
  </tbody>
</table>

---

## Quick Start

## Open It

This project is hosted on GitHub Pages, open:

```text
https://jameszeng8503.github.io/AnnotAI/
```

---

## Download and Run Locally
If you downloaded the project and run it locally, follow the instructions below.

Download or clone the project, then open a terminal in the project folder and run:

```bash
python3 -m http.server 8080
```

Then open:

```text
http://localhost:8080/index.html
```

> For best results, run the app through a local web server instead of opening `index.html` directly with `file://`.

---

## Project File Structure

The current project structure is:

```text
annotai-viewer/
├── index.html
├── manifest.json
├── sw.js
├── apple-touch-icon.png
├── LICENSE
├── README.md
└── icons/
    ├── icon-192.png
    ├── icon-512.png
    └── maskable-512.png
```

### File and Folder Description

<table>
  <thead>
    <tr>
      <th>File / folder</th>
      <th>Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>index.html</code></td>
      <td>The main AnnotAI Viewer web app.</td>
    </tr>
    <tr>
      <td><code>manifest.json</code></td>
      <td>Web app manifest used by browsers for installable app metadata and icons.</td>
    </tr>
    <tr>
      <td><code>sw.js</code></td>
      <td>Service worker file for web app caching or progressive web app behavior where supported.</td>
    </tr>
    <tr>
      <td><code>apple-touch-icon.png</code></td>
      <td>Icon used by Apple devices when the web app is saved to the Home Screen.</td>
    </tr>
    <tr>
      <td><code>icons/</code></td>
      <td>Application icon files used by the manifest and browser UI.</td>
    </tr>
    <tr>
      <td><code>README.md</code></td>
      <td>This user-facing project guide.</td>
    </tr>
    <tr>
    <tr>
      <td><code>LICENSE</code></td>
      <td>Project license information.</td>
    </tr>
  </tbody>
</table>

---

## Main Features

## 1. Browser-Based Viewer

AnnotAI Viewer runs in a modern web browser. No traditional desktop installation is required.

Users can open many common file types directly in the app.

<table>
  <thead>
    <tr>
      <th>Category</th>
      <th>Supported examples</th>
      <th>Use case</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Images</td>
      <td><code>PNG</code>, <code>JPG</code>, <code>JPEG</code>, <code>GIF</code>, <code>WEBP</code>, <code>SVG</code></td>
      <td>Review images, screenshots, diagrams, charts, and visual content.</td>
    </tr>
    <tr>
      <td>Videos</td>
      <td><code>MP4</code>, <code>WEBM</code>, <code>OGG</code>, <code>MOV</code></td>
      <td>Play videos and annotate around media content where supported by the browser.</td>
    </tr>
    <tr>
      <td>PDF</td>
      <td><code>PDF</code></td>
      <td>Read, scroll, annotate, present, and export views where supported.</td>
    </tr>
    <tr>
      <td>Documents</td>
      <td><code>DOCX</code>, <code>TXT</code>, <code>RTF</code>, <code>CSV</code></td>
      <td>Preview text and document content in the browser.</td>
    </tr>
    <tr>
      <td>Spreadsheets</td>
      <td><code>XLS</code>, <code>XLSX</code>, <code>CSV</code></td>
      <td>View spreadsheet content as browser-readable tables.</td>
    </tr>
    <tr>
      <td>Archives and eBooks</td>
      <td><code>ZIP</code>, <code>EPUB</code></td>
      <td>Inspect ZIP contents and preview simplified EPUB content.</td>
    </tr>
  </tbody>
</table>

Some formats, such as `DOC`, `PPT`, `PPTX`, `RAR`, and `MOBI`, may be detected but can require conversion or additional processing for full preview support.

---

## 2. PDF Viewing and Annotation

AnnotAI Viewer uses browser-based PDF rendering to display PDF pages.

Users can:

- open PDF files,
- scroll through pages,
- annotate individual pages,
- use pen and highlighter tools,
- erase annotations,
- use laser pointer mode during presentation,
- save annotations as JSON,
- reload saved annotations later,
- export annotated views as PNG where supported.

This is useful for reviewing:

- reports,
- lecture notes,
- academic papers,
- contracts,
- manuals,
- worksheets,
- PDF slides,
- teaching materials.

---

## 3. Document and Spreadsheet Preview

AnnotAI Viewer supports browser-side preview of common documents and spreadsheet files.

Examples include:

- reviewing DOCX reports,
- reading text files,
- opening CSV data,
- viewing XLS/XLSX spreadsheets,
- checking ZIP archive contents,
- previewing simplified EPUB eBook content.

This helps users inspect files quickly without switching between multiple office or media applications.

---

## 4. URL Loading

Users can paste a URL into AnnotAI Viewer and attempt to load it inside the workspace.

Supported URL examples include:

- direct image URLs,
- direct video URLs,
- direct PDF URLs,
- text file URLs,
- online office document URLs,
- general webpages where iframe embedding is allowed.

If a webpage blocks embedded viewing, users can open it externally in a new browser tab using the **Open External** button.

This is useful for:

- online teaching,
- web research,
- content review,
- comparing online sources,
- keeping annotation tools nearby while browsing.

---

## 5. Floating Annotation AI Tools Panel

AnnotAI Viewer includes a floating toolbar panel named **Annotation AI Tools**.

The panel can be:

- opened from a floating dot,
- collapsed when not needed,
- dragged around the screen,
- resized horizontally and vertically,
- widened or narrowed,
- made taller or shorter,
- scrolled to reveal all tools,
- remembered across sessions using local browser storage.

This flexible design keeps the workspace clean while still giving quick access to the main tools.

---

## 6. Annotation Tools

AnnotAI Viewer includes practical tools for visual explanation and review.

### OFF / Interact Mode

Use this mode when you want to interact with the content normally.

Good for:

- scrolling documents,
- using video controls,
- clicking embedded pages,
- moving around zoomed content,
- interacting with iframe content,
- navigating the workspace.

### Pen Tool

The Pen tool is used for freehand drawing.

Good for:

- marking key points,
- writing quick notes,
- drawing arrows,
- circling important areas,
- explaining ideas visually.

### Highlighter Tool

The Highlighter tool creates semi-transparent strokes.

Good for:

- highlighting text,
- emphasizing spreadsheet cells,
- marking important document areas,
- teaching and reviewing content.

### Eraser Tool

The Eraser removes annotation strokes.

Good for:

- correcting mistakes,
- cleaning up a page,
- removing old markings,
- updating explanations during presentation.

### Laser Pointer

The Laser tool works as a temporary pointer for presentations.

Good for:

- teaching live classes,
- presenting documents,
- pointing at chart areas,
- guiding audience attention,
- reviewing media frames.

> Laser marks are temporary and are not saved as permanent annotations.

---

## 7. AI Tool Launchers

AnnotAI Viewer includes dropdown launchers for popular AI tools.

The app provides separate launcher groups for:

- **AI Tools EN**
- **AI Tools CN**

Examples of English/global AI tools include:

- ChatGPT,
- Claude,
- Gemini,
- Microsoft Copilot,
- Perplexity,
- NotebookLM,
- Grok,
- Poe,
- Mistral Le Chat,
- Meta AI.

Examples of Chinese AI tools include:

- DeepSeek,
- Kimi,
- Qwen / Tongyi Qianwen,
- ERNIE Bot / Wenxin Yiyan,
- Doubao,
- Zhipu Qingyan,
- iFlytek Spark,
- Tencent Yuanbao,
- Hailuo AI,
- StepFun Yuewen.

These launchers help users quickly access AI assistants for:

- summarizing documents,
- translating content,
- asking questions,
- writing explanations,
- coding,
- research,
- creating lesson plans,
- generating discussion points,
- comparing ideas,
- improving productivity.

The selected tool opens in a new browser tab, preserving the current AnnotAI Viewer workspace.

---

## 8. Social Media and Media Platform Launchers

AnnotAI Viewer also includes dropdown launchers for English and Chinese social media or media platforms.

The app provides:

- **Media EN**
- **Media CN**

Examples of English/global platforms include:

- YouTube,
- Facebook,
- Instagram,
- TikTok,
- X / Twitter,
- LinkedIn,
- Reddit,
- Snapchat,
- Pinterest,
- WhatsApp.

Examples of Chinese platforms include:

- WeChat,
- Douyin,
- Xiaohongshu / RedNote,
- Weibo,
- Bilibili,
- Kuaishou,
- QQ,
- Zhihu,
- Baidu Tieba,
- Toutiao.

These launchers are useful for:

- content research,
- social media review,
- teaching with online examples,
- media comparison,
- marketing research,
- creator workflows,
- cross-platform content planning.

---

## 9. Multilingual Interface

AnnotAI Viewer includes a multilingual interface designed for international users.

Users can change the interface language from the Settings area. The selected language can be saved locally so the app remembers the preferred language across sessions.

The interface includes support for common global languages such as:

- English,
- Chinese,
- Arabic,
- Bengali,
- French,
- German,
- Hindi,
- Indonesian,
- Italian,
- Japanese,
- Korean,
- Portuguese,
- Russian,
- Spanish,
- Turkish,
- Urdu,
- Vietnamese.

> Some language coverage may vary depending on the section or feature.

---

## 10. Zoom and Fit Controls

AnnotAI Viewer includes zoom controls for detailed review and presentation.

Users can:

- zoom in,
- zoom out,
- reset zoom,
- fit content to width.

This is useful for:

- reading small text,
- inspecting images,
- reviewing charts,
- presenting on different screen sizes,
- using the app on tablets or mobile devices.

---

## 11. Save, Load, and Export

AnnotAI Viewer supports annotation persistence and export.

Users can:

- save annotations as JSON,
- load annotation JSON later,
- export the current annotated view as PNG where possible.

This helps users:

- continue review work later,
- share annotated screenshots,
- keep teaching records,
- keep meeting records,
- save visual feedback.

> Browser security may prevent exporting some cross-origin embedded content.

---

## Interface Guide

### Floating Dot

When the app starts, the toolbar may appear as a small floating dot.

Click or tap the dot to expand the tool panel.

### Annotation AI Tools Panel

The expanded panel contains the main tools, including:

- Open File,
- URL input,
- Load URL,
- Open External,
- Settings,
- Help,
- Language selector,
- AI launchers,
- Media launchers,
- annotation modes,
- color selector,
- stroke size slider,
- zoom controls,
- undo / redo,
- clear annotations,
- save / load JSON,
- export PNG.

### Panel Resizing

The panel can be adjusted in several ways:

- drag the panel header to move it,
- use the resize handle to resize it,
- use Wider / Narrower buttons,
- use Taller / Shorter buttons,
- scroll inside the panel if tools are hidden.

---

## Keyboard Shortcuts

AnnotAI Viewer includes keyboard shortcuts for faster use.

<table>
  <thead>
    <tr>
      <th>Shortcut</th>
      <th>Action</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>O</code></td>
      <td>OFF / Interact mode</td>
    </tr>
    <tr>
      <td><code>P</code></td>
      <td>Pen tool</td>
    </tr>
    <tr>
      <td><code>H</code></td>
      <td>Highlighter tool</td>
    </tr>
    <tr>
      <td><code>E</code></td>
      <td>Eraser tool</td>
    </tr>
    <tr>
      <td><code>L</code></td>
      <td>Laser pointer</td>
    </tr>
    <tr>
      <td><code>Ctrl / Cmd + Z</code></td>
      <td>Undo</td>
    </tr>
    <tr>
      <td><code>Ctrl / Cmd + Y</code></td>
      <td>Redo</td>
    </tr>
    <tr>
      <td><code>Ctrl / Cmd + +</code></td>
      <td>Zoom in</td>
    </tr>
    <tr>
      <td><code>Ctrl / Cmd + -</code></td>
      <td>Zoom out</td>
    </tr>
    <tr>
      <td><code>Ctrl / Cmd + 0</code></td>
      <td>Reset zoom</td>
    </tr>
  </tbody>
</table>

> Some shortcuts may depend on browser focus, operating system, keyboard layout, or the currently active panel.

---

## Common Use Cases

### Classroom Teaching

A teacher opens a PDF worksheet, uses the highlighter to mark key points, switches to laser pointer mode during explanation, and opens an AI tool for lesson support.

### Academic Research

A researcher opens a journal PDF, highlights important paragraphs, saves annotations as JSON, and opens an AI assistant to help summarize or compare ideas.

### Business Meeting

A manager opens a spreadsheet report, circles important numbers with the Pen tool, uses Fit Width for presentation, and exports an annotated PNG for meeting notes.

### Content Review

A creator opens a video file, pauses on a frame, uses annotations to mark changes, and opens YouTube or TikTok for platform comparison.

### Multilingual Collaboration

A team switches the interface language, opens a bilingual document, annotates wording issues, and launches English or Chinese AI tools for writing support.

### Design Feedback

A designer opens a UI screenshot, marks layout issues, adds visual feedback, and exports the annotated view for teammates.

---

## Browser and Platform Notes

AnnotAI Viewer is designed to work in modern browsers.

Recommended browsers:

- Google Chrome,
- Microsoft Edge,
- Mozilla Firefox,
- Safari.

Mobile browsers may work depending on file support, screen size, touch behavior, and browser limitations.

Because AnnotAI Viewer is browser-based, some features depend on browser security rules and device capabilities.

---

## External Libraries

AnnotAI Viewer uses browser-side libraries to support several file types.

Examples include:

<table>
  <thead>
    <tr>
      <th>Library</th>
      <th>Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>PDF.js</td>
      <td>PDF rendering in the browser.</td>
    </tr>
    <tr>
      <td>Mammoth.js</td>
      <td>DOCX to HTML conversion.</td>
    </tr>
    <tr>
      <td>SheetJS / XLSX</td>
      <td>Spreadsheet reading and HTML table generation.</td>
    </tr>
    <tr>
      <td>JSZip</td>
      <td>ZIP and EPUB extraction support.</td>
    </tr>
  </tbody>
</table>

If these libraries are loaded from external CDNs, internet access may be required for related features.

---

## Privacy and Security

AnnotAI Viewer is designed to work mostly inside the browser.

<table>
  <thead>
    <tr>
      <th>Action</th>
      <th>Privacy note</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Opening local files</td>
      <td>Files are selected by the user and loaded in the browser. The app cannot freely browse your file system.</td>
    </tr>
    <tr>
      <td>Annotations</td>
      <td>Annotations are handled in the browser and can be saved by the user as JSON.</td>
    </tr>
    <tr>
      <td>AI launchers</td>
      <td>AI tools open in separate tabs and are governed by their own privacy policies and terms.</td>
    </tr>
    <tr>
      <td>Social/media launchers</td>
      <td>External platforms are governed by their own accounts, policies, and terms of service.</td>
    </tr>
    <tr>
      <td>Export PNG</td>
      <td>Some embedded or cross-origin content may be blocked from export by browser security rules.</td>
    </tr>
  </tbody>
</table>

Users should avoid uploading sensitive documents to external AI or social platforms unless they understand the privacy implications.

---

## Important Limitations

AnnotAI Viewer is powerful, but browser-based apps have natural limitations.

### Local File Access

The app can only access files selected by the user.

It cannot freely browse local folders or automatically access files on the computer.

If the page is refreshed, local file object URLs may be lost, and the file may need to be opened again.

### Website Embedding

Some websites block iframe embedding for security reasons.

If a webpage does not load inside the viewer, use **Open External**.

Common causes include:

```text
X-Frame-Options
Content-Security-Policy
```

### Cross-Origin Content

Some cross-origin images, videos, or embedded webpages may not be exportable to PNG because of browser security restrictions.

### Office and Special Formats

DOCX and spreadsheets are supported through browser-side conversion. Complex formatting may not be perfectly preserved.

Formats like DOC, PPT, PPTX, RAR, and MOBI may require conversion or additional libraries for reliable preview.

### Offline Use

Some file preview features may depend on external browser libraries. If those libraries are loaded from CDNs, internet access may be needed.

For full offline use, these libraries need to be bundled locally and referenced from the project.

---

## Installation and Deployment

AnnotAI Viewer can be used as a standalone static web app.

It can be hosted on static hosting services such as:

- GitHub Pages,
- Gitee Pages,
- Netlify,
- Vercel,
- Cloudflare Pages,
- Firebase Hosting,
- AWS S3 static hosting.

---

## Deploy to GitHub Pages

### 1. Upload the project files

Make sure the repository contains:

```text
index.html
manifest.json
sw.js
apple-touch-icon.png
LICENSE
README.md
icons/icon-192.png
icons/icon-512.png
icons/maskable-512.png
```

### 2. Enable GitHub Pages

Go to:

```text
Repository → Settings → Pages
```

Select:

```text
Source: Deploy from branch
Branch: main
Folder: /root
```

### 3. Open the GitHub Pages URL

Your site will be available at:

```text
https://YOUR_USERNAME.github.io/REPOSITORY_NAME/
```

---

## Progressive Web App Notes

AnnotAI Viewer includes common web app files such as:

- `manifest.json`,
- `sw.js`,
- app icons,
- Apple touch icon.

These files help browsers recognize the project as a web app where supported.

On some devices, users may be able to add AnnotAI Viewer to the Home Screen or install it like a lightweight app.

---

## Troubleshooting

### The app does not work when double-clicking `index.html`

Do not use:

```text
file://...
```

Instead, run:

```bash
python3 -m http.server 8080
```

Then open:

```text
http://localhost:8080/index.html
```

---

### The page looks outdated after editing

Hard refresh the browser.

macOS:

```text
Command + Shift + R
```

Windows / Linux:

```text
Ctrl + Shift + R
```

---

### A website does not load inside the viewer

Some websites do not allow embedding inside another webpage.

Use **Open External** to open the site in a new tab.

---

### PNG export does not include embedded website content

This can happen because browsers block exporting cross-origin iframe content for security reasons.

This is a browser security limitation.

---

### Some document formats do not preview perfectly

Browser-side document conversion may not preserve all complex formatting.

For best results, convert difficult files to PDF before opening them in AnnotAI Viewer.

---

## Frequently Asked Questions

<details>
<summary><strong>Do I need to install AnnotAI Viewer?</strong></summary>

No traditional desktop installation is required. AnnotAI Viewer runs in a browser.

For local use, start a simple local server:

```bash
python3 -m http.server 8080
```

Then open:

```text
http://localhost:8080/index.html
```

</details>

<details>
<summary><strong>Can I use AnnotAI Viewer from GitHub Pages?</strong></summary>

Yes. AnnotAI Viewer is a static web app and can be hosted with GitHub Pages.

</details>

<details>
<summary><strong>Are my local files uploaded automatically?</strong></summary>

No. Local files selected through the browser are handled by the browser. AnnotAI Viewer does not automatically upload them.

However, external AI and social platforms opened from the launchers have their own privacy policies.

</details>

<details>
<summary><strong>Can I save my annotations?</strong></summary>

Yes. Use the JSON save/load tools to save annotation data and reload it later.

</details>

<details>
<summary><strong>Can I export annotated content?</strong></summary>

You can export annotated views as PNG where supported. Some cross-origin embedded content may be blocked by browser security rules.

</details>

<details>
<summary><strong>Why do some websites not open inside the viewer?</strong></summary>

Some websites block iframe embedding using browser security policies such as `X-Frame-Options` or `Content-Security-Policy`.

Use **Open External** to open them in a new browser tab.

</details>

<details>
<summary><strong>Does AnnotAI Viewer work offline?</strong></summary>

The static app files can be opened from local hosting, but some preview features may depend on external libraries if they are loaded from CDNs.

For full offline support, the related libraries need to be hosted locally.

</details>

---

## Why Use AnnotAI Viewer?

AnnotAI Viewer brings together tools that are often spread across different applications:

- file viewing,
- PDF reading,
- image and video review,
- annotation,
- presentation,
- URL loading,
- AI launcher,
- social media launcher,
- multilingual interface,
- save/load/export tools.

It is especially helpful when users need to:

- explain,
- review,
- teach,
- compare,
- annotate,
- present,
- research,
- work with AI tools.

---

## Project Summary

AnnotAI Viewer is a flexible, multilingual, browser-based productivity tool for viewing, annotating, presenting, and launching AI or social platforms.

It is useful for teachers, students, researchers, business users, designers, creators, translators, developers, trainers, and anyone who works with documents, media, URLs, or AI-assisted workflows.

With its movable and resizable floating panel, practical annotation tools, multilingual interface, and quick access to English and Chinese AI and media platforms, AnnotAI Viewer provides a convenient all-in-one workspace for modern digital learning, reviewing, presenting, and content exploration.

---

## License

Please check the `LICENSE` file in this repository before redistributing or modifying the project.

---

<div align="center">

## AnnotAI Viewer

<strong>View. Annotate. Present. Launch. Learn.</strong>

</div>

