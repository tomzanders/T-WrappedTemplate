# Year in Review Template

A standalone, "Spotify Wrapped"-style web presentation template. This single-file HTML application allows you to create an engaging, animated year-in-review summary with zero dependencies.

## Features

* **Slide-Based Storytelling:** Supports Intro, Statistics, Lists, and Outro slides.
* **Interactive Background:** Floating SVG particles that drift and react to the screen boundaries.
* **Animations:** Smooth CSS transitions for text entry, ranking lists, and progress bars.
* **Responsive:** Optimized for both desktop (keyboard navigation) and mobile (tap navigation).
* **Zero Dependencies:** No build tools, Node.js, or servers required. Just standard HTML/CSS/JS.

## Quick Start

1.  **Save the file:** Save the provided code as `index.html`.
2.  **Add a Logo:** Place a transparent image named `logo.png` in the same directory (or update the `<img>` tag in the HTML to point to your specific URL).
3.  **Run:** Open `index.html` in any modern web browser.

## Configuration

All content and settings are managed directly within the `<script>` tag at the bottom of the file.

### 1. Editing the Slides (`wrappedData`)
Find the `wrappedData` array in the JavaScript section (approx. line 130). Add objects to this array to define your story.

**Supported Slide Types:**

* **Intro/Outro:** Standard title cards.
    ```javascript
    { type: 'intro', title: "2025", subtitle: "My Year in Review" }
    ```
* **Statistic:** A large, emphasized number with a label and subtext.
    ```javascript
    { type: 'stat', title: "Coffees Drunk", value: "4,200", subtitle: "That's a lot of caffeine!" }
    ```
* **List:** A ranked list (Top 5, Top 10, etc.).
    ```javascript
    { type: 'list', title: "Top Songs", items: ["Song A", "Song B", "Song C"] }
    ```

### 2. Customizing Icons (`svgIcons`)
The background particles are generated from SVG strings. Locate the `svgIcons` array to customize the shapes floating in the background.

```javascript
const svgIcons = [
    // Paste your SVG strings here
    '<svg ...>...</svg>', 
];
