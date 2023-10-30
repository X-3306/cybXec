<!DOCTYPE html>
<html><head>
			
		<title>Configuring Tor Browser for Proxy Server Country Exclusion</title>
		<base href="./">
		<meta id="root-path" root-path="./">

		<link rel="icon" sizes="96x96" href="https://publish-01.obsidian.md/access/f786db9fac45774fa4f0d8112e232d67/favicon-96x96.png">
		<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes, minimum-scale=1.0, maximum-scale=5.0">
		<meta charset="UTF-8">
		<script src="https://code.iconify.design/iconify-icon/1.0.3/iconify-icon.min.js"></script>
			
			<!-- Obsidian App Styles / Other Built-in Styles -->
			<style> .callout
{
	mix-blend-mode: normal !important;
}

@media print 
{
    
    html body> :not(.print) 
    {
        display: unset !important;
    }

    .collapse-indicator
    {
        display: none !important;
    }

    .is-collapsed > element > .collapse-indicator
    {
        display: unset !important;
    }
}

cu {
  font-weight: 700
}

cg {
  color: green;
  font-weight: 700
}

cr {
  color: red;
  font-weight: 700
}

.list-collapse-indicator
{
    display: none !important;
}

@font-face
{
    font-family: MJXZERO;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Zero.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Main-Regular.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-B;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Main-Bold.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-I;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Math-Italic.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-MI;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Main-Italic.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-BI;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Math-BoldItalic.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-S1;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Size1-Regular.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-S2;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Size2-Regular.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-S3;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Size3-Regular.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-S4;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Size4-Regular.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-A;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_AMS-Regular.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-C;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Calligraphic-Regular.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-CB;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Calligraphic-Bold.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-FR;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Fraktur-Regular.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-FRB;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Fraktur-Bold.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-SS;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_SansSerif-Regular.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-SSB;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_SansSerif-Bold.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-SSI;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_SansSerif-Italic.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-SC;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Script-Regular.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-T;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Typewriter-Regular.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-V;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Vector-Regular.woff") format("woff");
}

@font-face
{
    font-family: MJXTEX-VB;
    src: url("https://publish.obsidian.md/lib/mathjax/output/chtml/fonts/woff-v2/MathJax_Vector-Bold.woff") format("woff");
}

@font-face {
    font-family: 'Avenir Next';
    font-weight: normal;
    font-style: normal;
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/94f2f163d4b698242fef.otf');
}

@font-face {
    font-family: 'Inter';
    font-style: normal;
    font-weight: 200;
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/72505e6a122c6acd5471.woff2') format('woff2');
}

@font-face {
    font-family: 'Inter';
    font-style: normal;
    font-weight: 300;
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/2d5198822ab091ce4305.woff2') format('woff2');
}

@font-face {
    font-family: 'Inter';
    font-weight: 400;
    font-style: normal;
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/c8ba52b05a9ef10f4758.woff2');
}

@font-face {
    font-family: 'Inter';
    font-weight: 400;
    font-style: italic;
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/cb10ffd7684cd9836a05.woff2');
}

@font-face {
    font-family: 'Inter';
    font-weight: 600;
    font-style: normal;
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/b5f0f109bc88052d4000.woff2');
}

@font-face {
    font-family: 'Inter';
    font-weight: 800;
    font-style: normal;
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/cbe0ae49c52c920fd563.woff2');
}

@font-face {
    font-family: 'Inter';
    font-weight: 800;
    font-style: italic;
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/535a6cf662596b3bd6a6.woff2');
}

@font-face {
    font-family: 'Source Code Pro';
    font-weight: normal;
    font-style: normal;
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/70cc7ff27245e82ad414.ttf');
}

@font-face {
    font-family: 'Source Code Pro';
    font-weight: normal;
    font-style: italic;
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/454577c22304619db035.ttf');
}

@font-face {
    font-family: 'Source Code Pro';
    font-weight: bold;
    font-style: normal;
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/52ac8f3034507f1d9e53.ttf');
}

@font-face {
    font-family: 'Source Code Pro';
    font-weight: bold;
    font-style: italic;
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/05b618077343fbbd92b7.ttf');
}

@font-face {
    font-family: 'Flow Circular';
    font-display: swap;
    src: url('https://publish.obsidian.md/public/fonts/853ff76f08786ae44ca0.woff');
}

.collapse-icon::before 
{ 
    /* content: "​" !important;  */
    content: "" !important;
    visibility: hidden !important;
}
body { --anim-duration-none: 0; --anim-duration-superfast: 70ms; --anim-duration-fast: 140ms; --anim-duration-moderate: 300ms; --anim-duration-slow: 560ms; --anim-motion-smooth: cubic-bezier(0.45, 0.05, 0.55, 0.95); --anim-motion-delay: cubic-bezier(0.65, 0.05, 0.36, 1); --anim-motion-jumpy: cubic-bezier(0.68, -0.55, 0.27, 1.55); --anim-motion-swing: cubic-bezier(0, 0.55, 0.45, 1); --blockquote-border-thickness: 2px; --blockquote-border-color: var(--interactive-accent); --blockquote-font-style: normal; --blockquote-color: inherit; --blockquote-background-color: transparent; --bold-weight: var(--font-semibold); --bold-color: inherit; --border-width: 1px; --button-radius: var(--input-radius); --callout-border-width: 0px; --callout-border-opacity: 0.25; --callout-padding: var(--size-4-3) var(--size-4-3) var(--size-4-3) var(--size-4-6); --callout-radius: var(--radius-s); --callout-blend-mode: var(--highlight-mix-blend-mode); --callout-title-color: inherit; --callout-title-padding: 0; --callout-title-size: inherit; --callout-content-padding: 0; --callout-content-background: transparent; --callout-bug: var(--color-red-rgb); --callout-default: var(--color-blue-rgb); --callout-error: var(--color-red-rgb); --callout-example: var(--color-purple-rgb); --callout-fail: var(--color-red-rgb); --callout-important: var(--color-cyan-rgb); --callout-info: var(--color-blue-rgb); --callout-question: var(--color-yellow-rgb); --callout-success: var(--color-green-rgb); --callout-summary: var(--color-cyan-rgb); --callout-tip: var(--color-cyan-rgb); --callout-todo: var(--color-blue-rgb); --callout-warning: var(--color-orange-rgb); --callout-quote: 158, 158, 158; --canvas-background: var(--background-primary); --canvas-card-label-color: var(--text-faint); --canvas-color-1: var(--color-red-rgb); --canvas-color-2: var(--color-orange-rgb); --canvas-color-3: var(--color-yellow-rgb); --canvas-color-4: var(--color-green-rgb); --canvas-color-5: var(--color-cyan-rgb); --canvas-color-6: var(--color-purple-rgb); --canvas-dot-pattern: var(--color-base-30); --checkbox-radius: var(--radius-s); --checkbox-size: var(--font-text-size); --checkbox-marker-color: var(--background-primary); --checkbox-color: var(--interactive-accent); --checkbox-color-hover: var(--interactive-accent-hover); --checkbox-border-color: var(--text-faint); --checkbox-border-color-hover: var(--text-muted); --checklist-done-decoration: line-through; --checklist-done-color: var(--text-muted); --code-white-space: pre-wrap; --code-size: var(--font-smaller); --code-background: var(--background-primary-alt); --code-normal: var(--text-muted); --code-comment: var(--text-faint); --code-function: var(--color-yellow); --code-important: var(--color-orange); --code-keyword: var(--color-pink); --code-operator: var(--color-red); --code-property: var(--color-cyan); --code-punctuation: var(--text-muted); --code-string: var(--color-green); --code-tag: var(--color-red); --code-value: var(--color-purple); --collapse-icon-color: var(--text-faint); --collapse-icon-color-collapsed: var(--text-accent); --cursor: default; --cursor-link: pointer; --dialog-width: 560px; --dialog-max-width: 80vw; --dialog-max-height: 85vh; --divider-color: var(--background-modifier-border); --divider-color-hover: var(--interactive-accent); --divider-width: 1px; --divider-width-hover: 3px; --divider-vertical-height: calc(100% - var(--header-height)); --drag-ghost-background: rgba(0, 0, 0, 0.85); --drag-ghost-text-color: #fff; --embed-max-height: 4000px; --embed-canvas-max-height: 400px; --embed-background: inherit; --embed-border-left: 2px solid var(--interactive-accent); --embed-border-right: none; --embed-border-top: none; --embed-border-bottom: none; --embed-padding: 0 0 0 var(--size-4-6); --embed-font-style: inherit; --embed-block-shadow-hover: 0 0 0 1px var(--background-modifier-border), inset 0 0 0 1px var(--background-modifier-border); --file-line-width: 700px; --file-folding-offset: 24px; --file-margins: var(--size-4-8); --file-header-font-size: var(--font-ui-small); --file-header-font-weight: 400; --file-header-border: var(--border-width) solid transparent; --file-header-justify: center; --font-smallest: 0.8em; --font-smaller: 0.875em; --font-small: 0.933em; --font-ui-smaller: 12px; --font-ui-small: 13px; --font-ui-medium: 15px; --font-ui-large: 20px; --font-thin: 100; --font-extralight: 200; --font-light: 300; --font-normal: 400; --font-medium: 500; --font-semibold: 600; --font-bold: 700; --font-extrabold: 800; --font-black: 900; --footnote-size: var(--font-smaller); --graph-controls-width: 240px; --graph-text: var(--text-normal); --graph-line: var(--color-base-35, var(--background-modifier-border-focus)); --graph-node: var(--text-muted); --graph-node-unresolved: var(--text-faint); --graph-node-focused: var(--text-accent); --graph-node-tag: var(--color-green); --graph-node-attachment: var(--color-yellow); --heading-formatting: var(--text-faint); --h1-color: inherit; --h2-color: inherit; --h3-color: inherit; --h4-color: inherit; --h5-color: inherit; --h6-color: inherit; --h1-font: inherit; --h2-font: inherit; --h3-font: inherit; --h4-font: inherit; --h5-font: inherit; --h6-font: inherit; --h1-line-height: 1.2; --h2-line-height: 1.2; --h3-line-height: 1.3; --h4-line-height: 1.4; --h5-line-height: var(--line-height-normal); --h6-line-height: var(--line-height-normal); --h1-size: 2em; --h2-size: 1.6em; --h3-size: 1.37em; --h4-size: 1.25em; --h5-size: 1.12em; --h6-size: 1.12em; --h1-style: normal; --h2-style: normal; --h3-style: normal; --h4-style: normal; --h5-style: normal; --h6-style: normal; --h1-variant: normal; --h2-variant: normal; --h3-variant: normal; --h4-variant: normal; --h5-variant: normal; --h6-variant: normal; --h1-weight: 700; --h2-weight: 600; --h3-weight: 600; --h4-weight: 600; --h5-weight: 600; --h6-weight: 600; --header-height: 40px; --hr-color: var(--background-modifier-border); --hr-thickness: 2px; --icon-size: var(--icon-m); --icon-stroke: var(--icon-m-stroke-width); --icon-xs: 14px; --icon-s: 16px; --icon-m: 18px; --icon-l: 18px; --icon-xl: 32px; --icon-xs-stroke-width: 2px; --icon-s-stroke-width: 2px; --icon-m-stroke-width: 1.75px; --icon-l-stroke-width: 1.75px; --icon-xl-stroke-width: 1.25px; --icon-color: var(--text-muted); --icon-color-hover: var(--text-muted); --icon-color-active: var(--text-accent); --icon-color-focused: var(--text-normal); --icon-opacity: 0.85; --icon-opacity-hover: 1; --icon-opacity-active: 1; --clickable-icon-radius: var(--radius-s); --indentation-guide-width: 1px; --indentation-guide-color: rgba(var(--mono-rgb-100), 0.12); --indentation-guide-color-active: rgba(var(--mono-rgb-100), 0.3); --inline-title-color: var(--h1-color); --inline-title-font: var(--h1-font); --inline-title-line-height: var(--h1-line-height); --inline-title-size: var(--h1-size); --inline-title-style: var(--h1-style); --inline-title-variant: var(--h1-variant); --inline-title-weight: var(--h1-weight); --input-height: 30px; --input-radius: 5px; --input-font-weight: var(--font-normal); --input-border-width: 1px; --italic-color: inherit; --layer-cover: 5; --layer-sidedock: 10; --layer-status-bar: 15; --layer-popover: 30; --layer-slides: 45; --layer-modal: 50; --layer-notice: 60; --layer-menu: 65; --layer-tooltip: 70; --layer-dragged-item: 80; --line-height-normal: 1.5; --line-height-tight: 1.3; --link-color: var(--text-accent); --link-color-hover: var(--text-accent-hover); --link-decoration: underline; --link-decoration-hover: underline; --link-decoration-thickness: auto; --link-external-color: var(--text-accent); --link-external-color-hover: var(--text-accent-hover); --link-external-decoration: underline; --link-external-decoration-hover: underline; --link-external-filter: none; --link-unresolved-color: var(--text-accent); --link-unresolved-opacity: 0.7; --link-unresolved-filter: none; --link-unresolved-decoration-style: solid; --link-unresolved-decoration-color: hsla(var(--interactive-accent-hsl), 0.3); --list-indent: 2em; --list-spacing: 0.075em; --list-marker-color: var(--text-faint); --list-marker-color-hover: var(--text-muted); --list-marker-color-collapsed: var(--text-accent); --list-bullet-border: none; --list-bullet-radius: 50%; --list-bullet-size: 0.3em; --list-bullet-transform: none; --list-numbered-style: decimal; --nav-item-size: var(--font-ui-small); --nav-item-color: var(--text-muted); --nav-item-color-hover: var(--text-normal); --nav-item-color-active: var(--text-normal); --nav-item-color-selected: var(--text-normal); --nav-item-color-highlighted: var(--text-accent-hover); --nav-item-background-hover: var(--background-modifier-hover); --nav-item-background-active: var(--background-modifier-hover); --nav-item-background-selected: hsla(var(--color-accent-hsl), 0.15); --nav-item-padding: var(--size-4-1) var(--size-4-2); --nav-item-parent-padding: var(--nav-item-padding); --nav-item-children-padding-left: var(--size-4-2); --nav-item-children-margin-left: var(--size-4-3); --nav-item-weight: inherit; --nav-item-weight-hover: inherit; --nav-item-weight-active: inherit; --nav-item-white-space: nowrap; --nav-indentation-guide-width: var(--indentation-guide-width); --nav-indentation-guide-color: var(--indentation-guide-color); --nav-collapse-icon-color: var(--collapse-icon-color); --nav-collapse-icon-color-collapsed: var(--text-faint); --modal-background: var(--background-primary); --modal-width: 90vw; --modal-height: 85vh; --modal-max-width: 1100px; --modal-max-height: 1000px; --modal-max-width-narrow: 800px; --modal-border-width: var(--border-width); --modal-border-color: var(--color-base-40, var(--background-modifier-border-focus)); --modal-radius: var(--radius-l); --modal-community-sidebar-width: 280px; --popover-width: 450px; --popover-height: 400px; --popover-max-height: 70vh; --popover-pdf-width: 600px; --popover-pdf-height: 800px; --popover-font-size: var(--font-text-size); --prompt-width: 700px; --prompt-max-width: 80vw; --prompt-max-height: 70vh; --prompt-border-width: var(--border-width); --prompt-border-color: var(--color-base-40, var(--background-modifier-border-focus)); --radius-s: 4px; --radius-m: 8px; --radius-l: 10px; --radius-xl: 16px; --ribbon-background: var(--background-secondary); --ribbon-background-collapsed: var(--background-primary); --ribbon-width: 44px; --ribbon-padding: var(--size-4-2) var(--size-4-1) var(--size-4-3); --scrollbar-active-thumb-bg: rgba(var(--mono-rgb-100), 0.2); --scrollbar-bg: rgba(var(--mono-rgb-100), 0.05); --scrollbar-thumb-bg: rgba(var(--mono-rgb-100), 0.1); --search-clear-button-color: var(--text-muted); --search-clear-button-size: 13px; --search-icon-color: var(--text-muted); --search-icon-size: 18px; --search-result-background: var(--background-primary); --size-2-1: 2px; --size-2-2: 4px; --size-2-3: 6px; --size-4-1: 4px; --size-4-2: 8px; --size-4-3: 12px; --size-4-4: 16px; --size-4-5: 20px; --size-4-6: 24px; --size-4-8: 32px; --size-4-9: 36px; --size-4-12: 48px; --size-4-16: 64px; --size-4-18: 72px; --sidebar-markdown-font-size: calc(var(--font-text-size) * 0.9); --sidebar-tab-text-display: none; --slider-thumb-border-width: 1px; --slider-thumb-border-color: var(--background-modifier-border-hover); --slider-thumb-height: 18px; --slider-thumb-width: 18px; --slider-thumb-y: -6px; --slider-thumb-radius: 50%; --slider-s-thumb-size: 15px; --slider-s-thumb-position: -5px; --slider-track-background: var(--background-modifier-border); --slider-track-height: 3px; --status-bar-background: var(--background-secondary); --status-bar-border-color: var(--divider-color); --status-bar-border-width: 1px 0 0 1px; --status-bar-font-size: var(--font-ui-smaller); --status-bar-text-color: var(--text-muted); --status-bar-position: fixed; --status-bar-radius: var(--radius-m) 0 0 0; --status-bar-scroll-padding: calc(var(--status-bar-font-size) + 18px); --swatch-radius: 14px; --swatch-height: 24px; --swatch-width: 24px; --swatch-shadow: inset 0 0 0 1px rgba(var(--mono-rgb-100), 0.15); --tab-background-active: var(--background-primary); --tab-text-color: var(--text-faint); --tab-text-color-active: var(--text-muted); --tab-text-color-focused: var(--text-muted); --tab-text-color-focused-active: var(--text-muted); --tab-text-color-focused-highlighted: var(--text-accent); --tab-text-color-focused-active-current: var(--text-normal); --tab-font-size: var(--font-ui-small); --tab-font-weight: inherit; --tab-container-background: var(--background-secondary); --tab-divider-color: var(--background-modifier-border-hover); --tab-outline-color: var(--divider-color); --tab-outline-width: 1px; --tab-curve: 6px; --tab-radius: var(--radius-s); --tab-radius-active: 6px 6px 0 0; --tab-width: 200px; --tab-max-width: 320px; --tab-stacked-pane-width: 700px; --tab-stacked-header-width: var(--header-height); --tab-stacked-font-size: var(--font-ui-small); --tab-stacked-font-weight: 400; --tab-stacked-text-align: left; --tab-stacked-text-transform: rotate(0deg); --tab-stacked-text-writing-mode: vertical-lr; --tab-stacked-shadow: -8px 0 8px 0 rgba(0, 0, 0, 0.05); --table-background: transparent; --table-border-width: 1px; --table-border-color: var(--background-modifier-border); --table-white-space: normal; --table-header-background: var(--table-background); --table-header-background-hover: inherit; --table-header-border-width: var(--table-border-width); --table-header-border-color: var(--table-border-color); --table-header-font: inherit; --table-header-size: var(--font-text-size); --table-header-weight: var(--bold-weight); --table-header-color: var(--text-normal); --table-text-size: inherit; --table-text-color: inherit; --table-column-max-width: none; --table-column-alt-background: var(--table-background); --table-column-first-border-width: var(--table-border-width); --table-column-last-border-width: var(--table-border-width); --table-row-background-hover: var(--table-background); --table-row-alt-background: var(--table-background); --table-row-last-border-width: var(--table-border-width); --tag-size: var(--font-smaller); --tag-color: var(--text-accent); --tag-color-hover: var(--text-accent); --tag-decoration: none; --tag-decoration-hover: none; --tag-background: hsla(var(--interactive-accent-hsl), 0.1); --tag-background-hover: hsla(var(--interactive-accent-hsl), 0.2); --tag-border-color: hsla(var(--interactive-accent-hsl), 0.15); --tag-border-color-hover: hsla(var(--interactive-accent-hsl), 0.15); --tag-border-width: 0px; --tag-padding-x: 0.65em; --tag-padding-y: 0.25em; --tag-radius: 2em; --titlebar-background: var(--background-secondary); --titlebar-background-focused: var(--background-secondary-alt); --titlebar-border-width: 0px; --titlebar-border-color: var(--background-modifier-border); --titlebar-text-color: var(--text-muted); --titlebar-text-color-focused: var(--text-normal); --titlebar-text-weight: var(--font-bold); --toggle-border-width: 2px; --toggle-width: 40px; --toggle-radius: 18px; --toggle-thumb-color: white; --toggle-thumb-radius: 18px; --toggle-thumb-height: 18px; --toggle-thumb-width: 18px; --toggle-s-border-width: 2px; --toggle-s-width: 34px; --toggle-s-thumb-height: 15px; --toggle-s-thumb-width: 15px; --vault-name-font-size: var(--font-ui-small); --vault-name-font-weight: var(--font-medium); --vault-name-color: var(--text-normal); --workspace-background-translucent: rgba(var(--mono-rgb-0), 0.6); --accent-h: 254; --accent-s: 80%; --accent-l: 68%; --background-primary: var(--color-base-00); --background-primary-alt: var(--color-base-10); --background-secondary: var(--color-base-20); --background-modifier-hover: rgba(var(--mono-rgb-100), 0.075); --background-modifier-active-hover: hsla(var(--interactive-accent-hsl), 0.15); --background-modifier-border: var(--color-base-30); --background-modifier-border-hover: var(--color-base-35); --background-modifier-border-focus: var(--color-base-40); --background-modifier-error-rgb: var(--color-red-rgb); --background-modifier-error: var(--color-red); --background-modifier-error-hover: var(--color-red); --background-modifier-success-rgb: var(--color-green-rgb); --background-modifier-success: var(--color-green); --background-modifier-message: rgba(0, 0, 0, 0.9); --background-modifier-form-field: var(--color-base-00); --text-normal: var(--color-base-100); --text-muted: var(--color-base-70); --text-faint: var(--color-base-50); --text-on-accent: white; --text-on-accent-inverted: black; --text-error: var(--color-red); --text-success: var(--color-green); --text-selection: hsla(var(--color-accent-hsl), 0.2); --text-accent: var(--color-accent); --text-accent-hover: var(--color-accent-2); --interactive-normal: var(--color-base-00); --interactive-hover: var(--color-base-10); --interactive-accent-hsl: var(--color-accent-hsl); --interactive-accent: var(--color-accent-1); --interactive-accent-hover: var(--color-accent-2); }
.theme-light { color-scheme: light; --highlight-mix-blend-mode: darken; --mono-rgb-0: 255, 255, 255; --mono-rgb-100: 0, 0, 0; --color-red-rgb: 233, 49, 71; --color-red: #E93147; --color-green-rgb: 8, 185, 78; --color-green: #08B94E; --color-orange-rgb: 236, 117, 0; --color-orange: #ec7500; --color-yellow-rgb: 224, 172, 0; --color-yellow: #e0ac00; --color-cyan-rgb: 0, 191, 188; --color-cyan: #00bfbc; --color-blue-rgb: 8, 109, 221; --color-blue: #086DDD; --color-purple-rgb: 120, 82, 238; --color-purple: #7852EE; --color-pink-rgb: 213, 57, 132; --color-pink: #D53984; --color-base-00: #ffffff; --color-base-05: #fcfcfc; --color-base-10: #fafafa; --color-base-20: #f6f6f6; --color-base-25: #e3e3e3; --color-base-30: #e0e0e0; --color-base-35: #d4d4d4; --color-base-40: #bdbdbd; --color-base-50: #ababab; --color-base-60: #707070; --color-base-70: #5a5a5a; --color-base-100: #222222; --color-accent-hsl: var(--accent-h), var(--accent-s), var(--accent-l); --color-accent: hsl(var(--accent-h), var(--accent-s), var(--accent-l)); --color-accent-1: hsl(var(--accent-h), var(--accent-s), calc(var(--accent-l) + 2.5%)); --color-accent-2: hsl(var(--accent-h), var(--accent-s), calc(var(--accent-l) + 5%)); --background-secondary-alt: var(--color-base-05); --background-modifier-box-shadow: rgba(0, 0, 0, 0.1); --background-modifier-cover: rgba(220, 220, 220, 0.4); --text-highlight-bg: rgba(255, 208, 0, 0.4); --text-highlight-bg-active: rgba(255, 128, 0, 0.4); --input-shadow: inset 0 0 0 1px rgba(0, 0, 0, 0.12), 0 2px 3px 0 rgba(0,0,0,0.05), 0 1px 1.5px 0 rgba(0,0,0,0.03), 0 1px 2px 0 rgba(0,0,0,0.04), 0 0 0 0 transparent; --input-shadow-hover: inset 0 0 0 1px rgba(0, 0, 0, 0.17), 0 2px 3px 0 rgba(0,0,0,0.1), 0 1px 1.5px 0 rgba(0,0,0,0.03), 0 1px 2px 0 rgba(0,0,0,0.04), 0 0 0 0 transparent; --shadow-s: 0px 1px 2px rgba(0, 0, 0, 0.028), 0px 3.4px 6.7px rgba(0, 0, 0, 0.042), 0px 15px 30px rgba(0, 0, 0, 0.07); --shadow-l: 0px 1.8px 7.3px rgba(0, 0, 0, 0.071), 0px 6.3px 24.7px rgba(0, 0, 0, 0.112), 0px 30px 90px rgba(0, 0, 0, 0.2); }
.theme-dark { color-scheme: dark; --highlight-mix-blend-mode: lighten; --mono-rgb-0: 0, 0, 0; --mono-rgb-100: 255, 255, 255; --color-red-rgb: 251, 70, 76; --color-red: #fb464c; --color-orange-rgb: 233, 151, 63; --color-orange: #E9973F; --color-yellow-rgb: 224, 222, 113; --color-yellow: #E0DE71; --color-green-rgb: 68, 207, 110; --color-green: #44CF6E; --color-cyan-rgb: 83, 223, 221; --color-cyan: #53DFDD; --color-blue-rgb: 2, 122, 255; --color-blue: #027aff; --color-purple-rgb: 168, 130, 255; --color-purple: #a882ff; --color-pink-rgb: 250, 153, 205; --color-pink: #FA99CD; --color-base-00: #1e1e1e; --color-base-10: #242424; --color-base-20: #262626; --color-base-25: #2a2a2a; --color-base-30: #363636; --color-base-35: #3F3F3F; --color-base-40: #555; --color-base-50: #666; --color-base-60: #999; --color-base-70: #bababa; --color-base-100: #dadada; --color-accent-hsl: var(--accent-h), var(--accent-s), var(--accent-l); --color-accent: hsl(var(--accent-h), var(--accent-s), var(--accent-l)); --color-accent-1: hsl(var(--accent-h), var(--accent-s), calc(var(--accent-l) - 3.8%)); --color-accent-2: hsl(var(--accent-h), var(--accent-s), calc(var(--accent-l) + 3.8%)); --background-modifier-form-field: var(--color-base-25); --background-secondary-alt: var(--color-base-30); --interactive-normal: var(--color-base-30); --interactive-hover: var(--color-base-35); --background-modifier-box-shadow: rgba(0, 0, 0, 0.3); --background-modifier-cover: rgba(10, 10, 10, 0.4); --text-highlight-bg: rgba(255, 208, 0, 0.4); --text-highlight-bg-active: rgba(255, 128, 0, 0.4); --text-selection: hsla(var(--interactive-accent-hsl), 0.25); --input-shadow: inset 0 0.5px 0.5px 0.5px rgba(255, 255, 255, 0.09), 0 2px 4px 0 rgba(0,0,0,0.15), 0 1px 1.5px 0 rgba(0,0,0,0.1), 0 1px 2px 0 rgba(0,0,0,0.2), 0 0 0 0 transparent; --input-shadow-hover: inset 0 0.5px 1px 0.5px rgba(255, 255, 255, 0.16), 0 2px 3px 0 rgba(0,0,0,0.3), 0 1px 1.5px 0 rgba(0,0,0,0.2), 0 1px 2px 0 rgba(0,0,0,0.4), 0 0 0 0 transparent; --shadow-s: 0px 1px 2px rgba(0, 0, 0, 0.121), 0px 3.4px 6.7px rgba(0, 0, 0, 0.179), 0px 15px 30px rgba(0, 0, 0, 0.3); --shadow-l: 0px 1.8px 7.3px rgba(0, 0, 0, 0.071), 0px 6.3px 24.7px rgba(0, 0, 0, 0.112), 0px 30px 90px rgba(0, 0, 0, 0.2); }
iframe { color-scheme: normal; }
@media print {
  .theme-dark { --highlight-mix-blend-mode: darken; }
}
body { --font-default: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Inter", "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Microsoft YaHei Light", sans-serif; --font-monospace-default: Menlo, SFMono-Regular, Consolas, "Roboto Mono", "Source Code Pro", monospace; --font-interface-override: "??"; --font-interface-theme: "??"; --font-interface: var(--font-interface-override), var(--font-interface-theme), var(--default-font, "??"), var(--font-default); --font-text-override: "??"; --font-text-theme: "??"; --font-text: var(--font-text-override), var(--font-text-theme), var(--font-interface); --font-monospace-override: "??"; --font-monospace-theme: "??"; --font-monospace: var(--font-monospace-override), var(--font-monospace-theme), var(--font-monospace-default); --font-text-size: 16px; --font-mermaid: var(--font-text); }
@media print {
  html, body { padding-top: 0px !important; overflow: auto !important; height: auto !important; }
  iframe, .titlebar, .app-container, .progress-bar, .popover, .markdown-embed-link { display: none !important; }
  body > :not(.print) { display: none !important; }
  .print .markdown-preview-view { -webkit-print-color-adjust: exact; color: initial; }
  .print .markdown-preview-view mark { color: initial; }
  .print .markdown-preview-view .frontmatter-container { display: none; }
  .print .markdown-preview-view .markdown-embed-content { max-height: none; overflow: visible; }
  .print .markdown-preview-view .callout-content { display: inherit !important; }
  .print .external-link { background: none; padding-right: 0px; }
  * { text-shadow: none !important; }
  webview { display: none; }
  ::-webkit-scrollbar { display: none; }
  body { --font-text: "Inter"  !important; }
}
* { box-sizing: border-box; }
html, body { margin: 0px; padding: 0px; height: 100%; width: 100%; overflow: hidden; }
body { text-rendering: optimizelegibility; font-family: var(--font-interface); line-height: var(--line-height-tight); font-size: var(--font-ui-medium); background-color: var(--background-primary); color: var(--text-normal); -webkit-tap-highlight-color: rgba(255, 255, 255, 0); }
body.is-translucent { background-color: transparent; }
body { user-select: none; overflow: hidden; }
body [contenteditable="true"], body [contenteditable=""] { user-select: text; }
body.is-grabbing, body.is-grabbing :not(.workspace-leaf-resize-handle) { cursor: grabbing !important; }
body.is-grabbing iframe:not(.is-controlled), body.is-grabbing webview { pointer-events: none; }
.app-container { display: flex; height: 100%; width: 100%; position: relative; flex-direction: column; }
.app-container.no-transition * { transition: none 0s ease 0s !important; }
.horizontal-main-container { width: 100%; display: flex; overflow: hidden; flex: 1 0 0px; }
:focus { outline: none; }
.is-text-garbled * { font-family: "Flow Circular", sans-serif !important; line-height: 1.45em !important; }
@-webkit-keyframes blink { 
  50% { background-color: transparent; }
}
@keyframes blink { 
  50% { background-color: transparent; }
}
div.CodeMirror span.CodeMirror-matchingbracket { color: rgb(0, 187, 0); }
div.CodeMirror span.CodeMirror-nonmatchingbracket { color: rgb(170, 34, 34); }
div.CodeMirror-cursors { visibility: hidden; position: relative; z-index: 3; }
div.CodeMirror-dragcursors { visibility: visible; }
@media print {
  .CodeMirror div.CodeMirror-cursors { visibility: hidden; }
}
span.CodeMirror-selectedtext { background: none; }
.markdown-source-view { font-size: var(--font-text-size); font-family: var(--font-text); }
.markdown-source-view.mod-cm5 { height: 100%; }
.workspace-leaf-content.is-read-mode .markdown-source-view { z-index: 0; }
.markdown-source-view.is-readable-line-width .CodeMirror { max-width: var(--file-line-width); margin-left: auto; margin-right: auto; }
.drag-ghost { position: fixed; font-size: var(--font-ui-small); color: var(--drag-ghost-text-color); padding: var(--size-2-3) var(--size-4-2); border-radius: var(--radius-s); background-color: var(--drag-ghost-background); box-shadow: 0 2px 8px var(--background-modifier-box-shadow); z-index: var(--layer-dragged-item); max-width: 300px; font-weight: var(--font-medium); pointer-events: none; }
.drag-ghost.mod-leaf { display: flex; z-index: var(--layer-tooltip); }
.drag-ghost-icon { margin-right: var(--size-2-3); position: relative; }
.drag-reorder-ghost { position: fixed; border-radius: var(--radius-s); background-color: var(--background-primary); box-shadow: 0 2px 8px var(--background-modifier-box-shadow); z-index: var(--layer-dragged-item); pointer-events: none; }
.drag-ghost-self { display: flex; }
.drag-ghost-self > .svg-icon { --icon-size: var(--icon-xs); --icon-stroke: var(--icon-xs-stroke-width); opacity: 0.7; vertical-align: middle; align-self: center; margin-right: var(--size-2-2); flex-shrink: 0; }
.drag-ghost-self span { overflow: hidden; white-space: nowrap; text-overflow: ellipsis; }
.drag-ghost-action { padding: var(--size-2-1) 0 0 0; font-size: var(--font-ui-smaller); opacity: 0.7; overflow: hidden; white-space: nowrap; text-overflow: ellipsis; }
.drag-ghost-hidden { visibility: hidden; position: relative; }
.drag-ghost-hidden::before { content: " "; position: absolute; inset: 0px; visibility: visible; border-radius: 5px; background-color: hsla(var(--interactive-accent-hsl), 0.3); }
.markdown-source-view.mod-cm6 { height: 100%; display: flex; flex-direction: column; }
.markdown-source-view.mod-cm6 ::selection { background-color: var(--text-selection); }
.markdown-source-view.mod-cm6 .cm-line .cm-selection, .markdown-source-view.mod-cm6 .cm-line .cm-inline-code .cm-selection { background-color: var(--text-selection); }
.markdown-source-view.mod-cm6 .cm-selectionBackground { background-color: var(--text-selection); }
.markdown-source-view.mod-cm6.is-readable-line-width .cm-sizer { max-width: var(--file-line-width); margin-left: auto; margin-right: auto; }
.markdown-source-view.mod-cm6.is-readable-line-width .cm-content { max-width: var(--file-line-width); }
.markdown-source-view.mod-cm6.is-readable-line-width .cm-line { max-width: var(--file-line-width); }
.markdown-source-view.mod-cm6.is-readable-line-width .cm-line.HyperMD-table-row { max-width: 100%; }
.markdown-source-view.mod-cm6 .cm-editor { flex: 1 1 0px; min-height: 0px; }
.markdown-source-view.mod-cm6 .cm-editor.cm-focused { outline: none; }
.markdown-source-view.mod-cm6 .cm-editor .cm-selectionBackground { background: var(--text-selection); }
.markdown-source-view.mod-cm6 .cm-scroller { font-family: var(--font-text); line-height: var(--line-height-normal); scroll-padding-block-end: var(--status-bar-scroll-padding); }
.markdown-source-view.mod-cm6 .cm-sizer { display: flex; flex-direction: column; align-items: stretch; width: 100%; min-height: 100%; }
.markdown-source-view.mod-cm6 .cm-contentContainer { flex: 1 1 auto; display: flex; align-items: stretch; overflow-x: visible; }
.markdown-source-view.mod-cm6 .cm-content { width: 0px; caret-color: var(--text-normal); min-height: unset; flex-basis: unset !important; }
.is-mobile.is-ios .markdown-source-view.mod-cm6 .cm-content { -webkit-user-modify: read-write; }
.markdown-source-view.mod-cm6 .cm-content > * { display: block; margin: 0px !important; }
.markdown-source-view.mod-cm6 .cm-content > [contenteditable="false"] { contain: paint !important; }
.markdown-source-view.mod-cm6 .cm-gutters { flex: 0 0 auto; background-color: transparent; padding-inline-end: var(--file-folding-offset); font-size: var(--font-ui-smaller); z-index: 1; font-variant: tabular-nums; color: var(--text-faint)  !important; border-right: none !important; }
.markdown-source-view.mod-cm6 .cm-line > * { text-indent: 0px; }
.markdown-source-view.mod-cm6 .cm-transparent { color: transparent; }
.markdown-source-view.mod-cm6 .cm-html-embed, .markdown-source-view.mod-cm6 .cm-callout, .markdown-source-view.mod-cm6 .cm-table-widget { white-space: normal; overflow-wrap: normal; word-break: normal; }
.markdown-source-view.mod-cm6 .cm-line { position: relative; padding: 0px; }
.markdown-source-view.mod-cm6 .edit-block-button { padding: var(--size-2-2) var(--size-2-3); position: absolute; top: var(--size-2-2); right: var(--size-2-2); display: flex; opacity: 0; color: var(--text-muted); border-radius: var(--radius-s); cursor: var(--cursor); }
@media (hover: hover) {
  .markdown-source-view.mod-cm6 .edit-block-button:hover { background-color: var(--background-modifier-hover); }
}
.markdown-source-view.mod-cm6 .cm-panels { background-color: inherit; color: inherit; }
.markdown-source-view.mod-cm6 img.cm-widgetBuffer { display: inline !important; width: 0px !important; border: 0px !important; margin: 0px !important; padding: 0px !important; }
.view-content > .markdown-source-view.mod-cm6 > .cm-editor > .cm-scroller { padding: var(--file-margins); }
.empty-state { position: absolute; height: 100%; width: 100%; top: 0px; left: 0px; display: flex; align-items: center; justify-content: center; flex-direction: column; }
.empty-state-container { max-width: 480px; max-height: 280px; margin: 20px; text-align: center; }
.empty-state-title { margin: 20px 0px; font-weight: var(--h2-weight); font-size: var(--h2-size); line-height: var(--line-height-tight); position: relative; }
.empty-state-action-list { font-size: var(--font-text-size); line-height: var(--line-height-tight); color: var(--text-muted); margin-top: 20px; }
.empty-state-action { cursor: var(--cursor); line-height: 36px; color: var(--text-accent); }
@media (hover: hover) {
  .empty-state-action:hover { color: var(--text-accent-hover); }
}
.empty-state-close-button { display: none; }
body { --zoom-factor: 1; --titlebar-height: 30px; }
.mod-macos { --frame-left-space: calc(80px - var(--ribbon-width)); --frame-right-space: 0px; }
.mod-macos.is-popout-window { --frame-left-space: 80px; }
.mod-windows, .mod-linux { --frame-left-space: 0px; --frame-right-space: 126px; }
body.is-frameless:not(.is-hidden-frameless) { padding-top: calc(var(--titlebar-height) / var(--zoom-factor)); }
body.is-frameless:not(.is-hidden-frameless) .titlebar { height: var(--titlebar-height); zoom: calc(1 / var(--zoom-factor)); }
body.is-frameless:not(.is-hidden-frameless):not(.is-maximized) .titlebar { padding-top: 2px; }
body.is-frameless.is-hidden-frameless .titlebar { height: calc(var(--header-height) - 1px); }
body.is-frameless.is-hidden-frameless.starter .titlebar { height: var(--titlebar-height); }
.is-fullscreen .titlebar { display: none; }
.sidebar-toggle-button, .workspace-tabs.mod-top { --tab-container-background: var(--titlebar-background); }
body.is-focused .titlebar, body.is-focused .workspace-ribbon.mod-left { --titlebar-background: var(--titlebar-background-focused); }
body.is-focused .sidebar-toggle-button, body.is-focused .workspace-tabs.mod-top { --tab-container-background: var(--titlebar-background-focused); }
.is-hidden-frameless { --divider-vertical-height: 100%; }
.workspace-ribbon .sidebar-toggle-button { position: absolute; top: 0px; left: 0px; width: var(--ribbon-width); justify-content: center; }
.titlebar-button.mod-logo { width: var(--ribbon-width); justify-content: center; }
.is-hidden-frameless:not(.starter) .titlebar { app-region: no-drag; }
.is-hidden-frameless .titlebar-button.mod-logo { display: none; }
.is-hidden-frameless:not(.is-fullscreen) .workspace-tab-header-container { transition: padding-left 275ms var(--anim-motion-swing), padding-right 275ms var(--anim-motion-swing); }
.is-hidden-frameless:not(.is-fullscreen) .workspace-tabs.mod-top-left-space .workspace-tab-header-container { padding-left: var(--frame-left-space); }
.is-hidden-frameless:not(.is-fullscreen) .workspace-tabs.mod-top-left-space .workspace-tab-header-container::before { app-region: no-drag; content: ""; height: 100%; left: 0px; top: 0px; position: absolute; width: var(--frame-left-space); }
.is-hidden-frameless:not(.is-fullscreen) .workspace-tabs.mod-top-right-space .workspace-tab-header-container { padding-right: var(--frame-right-space); }
.is-hidden-frameless:not(.is-fullscreen) .workspace-tabs.mod-top-right-space .workspace-tab-header-container::after { app-region: no-drag; content: ""; height: 100%; right: 0px; top: 0px; position: absolute; width: var(--frame-right-space); }
.is-hidden-frameless:not(.is-fullscreen) .titlebar-button-container.mod-right { background-color: var(--titlebar-background); }
.is-hidden-frameless:not(.is-fullscreen).is-focused .titlebar-button-container.mod-right { background-color: var(--titlebar-background-focused); }
.titlebar-button.mod-logo:hover .logo-wireframe, .titlebar-button.mod-logo:not(:hover) .logo-full { display: none; }
body.is-frameless:not(.mod-macos) > .app-container ~ * { app-region: no-drag; }
body.is-frameless:not(.mod-macos) .modal-container, body.is-frameless:not(.mod-macos) .suggestion-bg { app-region: initial; }
body.is-frameless:not(.mod-macos) .modal { app-region: no-drag; }
.loader-cube { width: 40px; height: 40px; margin: 100px auto; }
.loader-cube .sk-cube { width: 33%; height: 33%; background-color: var(--interactive-accent); float: left; animation: 1.3s ease-in-out 0s infinite normal none running sk-cubeGridScaleDelay; }
.loader-cube .sk-cube1 { animation-delay: 0.2s; }
.loader-cube .sk-cube2 { animation-delay: 0.3s; }
.loader-cube .sk-cube3 { animation-delay: 0.4s; }
.loader-cube .sk-cube4 { animation-delay: 0.1s; }
.loader-cube .sk-cube5 { animation-delay: 0.2s; }
.loader-cube .sk-cube6 { animation-delay: 0.3s; }
.loader-cube .sk-cube7 { animation-delay: 0s; }
.loader-cube .sk-cube8 { animation-delay: 0.1s; }
.loader-cube .sk-cube9 { animation-delay: 0.2s; }
@-webkit-keyframes sk-cubeGridScaleDelay { 
  0%, 70%, 100% { transform: scale3d(1, 1, 1); }
  35% { transform: scale3d(0, 0, 1); }
}
@keyframes sk-cubeGridScaleDelay { 
  0%, 70%, 100% { transform: scale3d(1, 1, 1); }
  35% { transform: scale3d(0, 0, 1); }
}
.is-loading { position: relative; }
.is-loading::before { content: " "; position: absolute; top: 0px; width: 0px; height: 3px; background-color: var(--interactive-accent); animation: 1000ms ease-in-out 300ms infinite normal none running progress-bar; }
.pane-empty { color: var(--text-faint); font-size: var(--font-ui-small); margin: var(--size-4-2) auto; text-align: center; }
.view-header { height: var(--header-height); display: none; border-bottom: var(--file-header-border); background-color: var(--background-primary); z-index: 1; position: relative; gap: var(--size-4-2); padding: 0 var(--size-4-3); }
body.is-phone .view-header, .show-view-header .view-header { display: flex; }
.is-focused .workspace-leaf.mod-active .view-header { background-color: var(--background-primary); }
.workspace-split.mod-left-split .view-header, .workspace-split.mod-right-split .view-header, .workspace-fake-target-overlay.is-in-sidebar .view-header { display: none; }
.view-header.is-highlighted::after { content: " "; position: absolute; width: 100%; height: 100%; top: 0px; left: 0px; background-color: hsla(var(--interactive-accent-hsl), 0.5); }
.view-header .view-header-icon { display: none; padding: var(--size-2-2); margin-right: var(--size-2-3); color: var(--text-muted); align-self: center; cursor: grab; }
.view-header .view-header-icon:active { cursor: grabbing; }
.view-header-title { font-size: var(--file-header-font-size); font-weight: var(--file-header-font-weight); flex: 1 1 0px; max-width: max-content; overflow: auto; padding: 0 var(--size-4-1); white-space: pre; overflow-wrap: normal; color: var(--text-muted); scroll-padding-inline-end: 20px; }
.is-focused .workspace-leaf.mod-active .view-header-title { color: var(--text-normal); }
.view-header-title::-webkit-scrollbar { display: none; }
.view-header-title-container { flex-grow: 1; overflow: hidden; position: relative; justify-content: var(--file-header-justify); display: flex; align-items: center; gap: 0px; white-space: nowrap; }
.view-header-title-container:not(.mod-at-start)::before { content: " "; position: absolute; top: 0px; left: 0px; width: 30px; height: 100%; background: linear-gradient(to right, var(--background-primary), transparent); }
.view-header-title-container:not(.mod-at-end)::after { content: " "; position: absolute; top: 0px; right: 0px; width: 30px; height: 100%; background: linear-gradient(to right, transparent, var(--background-primary)); }
.view-header-title-parent { font-size: var(--file-header-font-size); color: var(--text-muted); min-width: 0px; display: flex; gap: 0px; overflow: hidden; }
.view-header-title-parent .view-header-breadcrumb { padding: 2px 4px; border-radius: var(--radius-s); }
@media (hover: hover) {
  .view-header-title-parent .view-header-breadcrumb:hover { background-color: var(--background-modifier-hover); color: var(--text-normal); }
}
.view-header-title-parent .view-header-breadcrumb-separator { padding: 2px 1px; color: var(--text-faint); }
.view-content { width: 100%; height: calc(100% - var(--header-height)); }
.workspace-split.mod-root .view-content { background-color: var(--background-primary); }
.workspace-split.mod-root .workspace-fake-target-overlay .view-content { background-color: transparent; }
.workspace-split.mod-left-split .view-content, .workspace-split.mod-right-split .view-content { height: 100%; overflow: auto; }
.inline-title { font-weight: var(--inline-title-weight); font-size: var(--inline-title-size); line-height: var(--inline-title-line-height); font-style: var(--inline-title-style); font-variant: var(--inline-title-variant); font-family: var(--inline-title-font); padding-bottom: 0.5em; letter-spacing: -0.015em; color: var(--inline-title-color); }
.hover-popover .inline-title, .inline-embed .inline-title { display: none; }
body:not(.show-inline-title) .inline-title:not([data-level]) { display: none; }
::selection { background-color: var(--text-selection); }
.markdown-reading-view { display: flex; flex-direction: column; }
.markdown-preview-view { font-size: var(--font-text-size); font-family: var(--font-text); line-height: var(--line-height-normal); width: 100%; height: 100%; padding: var(--file-margins); position: relative; overflow-y: auto; overflow-wrap: break-word; color: var(--text-normal); user-select: text; }
.workspace-leaf-content.is-read-mode .markdown-preview-view { width: 100%; left: 0px; background-color: var(--background-primary); }
.markdown-preview-view.is-readable-line-width .markdown-preview-sizer { max-width: var(--file-line-width); margin-left: auto; margin-right: auto; }
.markdown-rendered.rtl { direction: rtl; }
.workspace-ribbon.mod-left { margin-top: var(--header-height); }
.workspace-ribbon.mod-left::before { position: absolute; left: 0px; top: 0px; background-color: var(--titlebar-background); content: " "; border-bottom: var(--tab-outline-width) solid var(--tab-outline-color); height: calc(var(--header-height) - var(--tab-outline-width)); width: var(--ribbon-width); }
.workspace-ribbon { width: var(--ribbon-width); flex: 0 0 var(--ribbon-width); display: flex; flex-direction: column; overflow: hidden; background-color: var(--ribbon-background); z-index: var(--layer-sidedock); color: var(--text-muted); padding: var(--ribbon-padding); gap: var(--size-4-1); border-right: var(--divider-width) solid var(--divider-color); }
.workspace-ribbon.mod-left.is-collapsed { transition: background-color 250ms ease-in-out 95ms; background-color: var(--ribbon-background-collapsed); border-right-color: var(--divider-color); }
.workspace-ribbon.mod-right { display: none; }
.workspace-ribbon.is-hidden { display: none; }
.workspace-ribbon.is-collapsed { background-color: var(--background-secondary); }
.side-dock-settings, .side-dock-actions { flex-direction: column; }
.side-dock-settings .side-dock-ribbon-action, .side-dock-actions .side-dock-ribbon-action { margin: 0px auto; }
.side-dock-settings { margin-top: auto; }
.release-notes-view { padding: var(--file-margins); }
.release-notes-view .markdown-preview-view { overflow: visible; }
.release-notes-view .is-readable-line-width { max-width: var(--file-line-width); margin-left: auto; margin-right: auto; }
.setting { display: flex; align-items: center; }
.setting-text { flex-grow: 1; }
.setting-title { font-size: var(--font-ui-large); line-height: var(--line-height-normal); }
.setting-explanation { color: var(--text-muted); }
.modal.mod-new-editor { max-width: 600px; }
.modal.mod-trust-folder { max-width: 700px; }
.modal.mod-settings .vertical-tab-header { flex: 0 0 25%; min-width: 180px; max-width: 250px; overflow: auto; border-right: 1px solid var(--divider-color); }
.modal.mod-settings .modal-content { margin-top: 0px; overflow: hidden; }
.modal.mod-plugin-options .modal-content { margin: var(--size-4-6) 0; }
.setting-item { display: flex; align-items: center; padding: 0.75em 0px; border-top: 1px solid var(--background-modifier-border); }
.setting-item + .setting-item-heading { margin-top: 0.75em; }
.setting-item:first-child { padding-top: 0px; border-top: none; }
.setting-item > :first-child { margin-right: var(--size-4-4); }
.setting-item > :last-child { margin-right: 0px; }
.setting-item.mod-cta { justify-content: center; }
.setting-item-heading { font-weight: var(--font-semibold); border-top: none; }
.setting-item-heading .setting-item-info { flex-grow: 0; margin-right: 0px; }
.setting-item-heading .setting-item-description { font-weight: var(--font-normal); }
.setting-item-info { flex: 1 1 auto; }
.setting-item-description { color: var(--text-muted); font-size: var(--font-ui-smaller); padding-top: var(--size-4-1); line-height: var(--line-height-tight); }
.setting-item-description:empty { display: none; }
.setting-item-description code { font-family: var(--font-monospace); font-size: var(--font-smaller); border-radius: var(--radius-s); padding: 0px 3px 2px; position: relative; bottom: 1px; }
.setting-item-description ul { margin: var(--size-4-1) 0; padding-left: var(--size-4-6); }
.setting-item-name { color: var(--text-normal); font-size: var(--font-ui-medium); line-height: var(--line-height-tight); }
.setting-item-control { flex: 1 1 auto; text-align: right; display: flex; justify-content: flex-end; align-items: center; gap: var(--size-4-2); }
.setting-item-control.mod-vertical { flex-direction: column; }
.setting-item-control.mod-vertical > :not(:last-child) { margin-bottom: 10px; margin-right: 0px; }
.setting-item-control.mod-hotkey { padding-top: 0px; cursor: default; }
.setting-item-control.mod-hotkey input { font-family: var(--font-monospace); font-size: var(--font-smaller); }
.setting-item-control.mod-hotkey input:focus { background-color: var(--interactive-accent); color: var(--text-on-accent); }
.setting-item-control select { width: inherit; max-width: 400px; }
.setting-command-hotkeys { display: flex; flex-direction: column; }
.setting-hotkey { font-family: -apple-system, BlinkMacSystemFont, var(--font-monospace); font-size: var(--font-ui-small); background-color: var(--background-modifier-hover); border-radius: 4px; padding: 2px 4px 2px 8px; align-self: flex-end; white-space: nowrap; display: flex; align-items: center; gap: 4px; }
.theme-dark .setting-hotkey.has-conflict, .theme-light .setting-hotkey.has-conflict { background-color: var(--background-modifier-error); color: var(--text-on-accent); }
.setting-hotkey.mod-active { background-color: var(--interactive-accent); color: var(--text-on-accent); }
.setting-hotkey.mod-empty { padding-right: var(--size-4-2); }
.setting-hotkey:not(:first-child) { margin-top: var(--size-4-2); }
.setting-hotkey-icon { display: flex; align-items: center; cursor: var(--cursor); border-radius: 50%; line-height: 1; text-align: center; }
.setting-hotkey-icon .svg-icon { width: 16px; height: 16px; stroke-width: 2px; opacity: 0.6; }
@media (hover: hover) {
  .setting-hotkey-icon:hover .svg-icon { opacity: 1; }
}
@media (hover: hover) {
  .setting-delete-hotkey:hover { background-color: var(--background-modifier-error); color: var(--text-on-accent); }
}
.setting-add-hotkey-button, .setting-restore-hotkey-button { padding: var(--size-2-2); border-radius: var(--radius-s); color: var(--text-faint); cursor: var(--cursor); height: calc(var(--icon-l) + var(--size-2-2) + var(--size-2-2)); }
.setting-add-hotkey-button.mod-active, .setting-restore-hotkey-button.mod-active { color: var(--text-accent); }
@media (hover: hover) {
  .setting-add-hotkey-button:hover, .setting-restore-hotkey-button:hover { background-color: var(--background-modifier-hover); color: var(--text-normal); }
}
.setting-editor-extra-setting-button { line-height: 0; }
.setting-message { font-size: var(--font-ui-small); }
.setting-font-list { margin: 1.5em 0px 0.75em; }
.hotkey-settings-container { display: flex; flex-direction: column; }
.hotkey-settings-container .setting-item-description { padding-top: 0px; }
.hotkey-settings-container hr { margin: 20px 0px 10px; }
.hotkey-list-container { overflow: auto; }
.hotkey-search-container { padding-bottom: 20px; display: flex; flex-wrap: wrap; }
.modal.mod-image-lightbox { max-width: 90vw; max-height: 90vh; padding: 0px; }
.modal.mod-image-lightbox .modal-content { padding: var(--size-4-12) var(--size-4-3) var(--size-4-2) var(--size-4-3); text-align: center; }
.login-field { max-width: 500px; margin: 1em auto; }
.spellchecker-dictionary-container { max-height: 60vh; overflow: auto; }
.spellchecker-dictionary-item { display: flex; margin-bottom: 10px; }
.spellchecker-dictionary-word { flex-grow: 1; }
.spellchecker-dictionary-remove-button { cursor: var(--cursor); color: var(--text-muted); margin-right: 10px; }
@media (hover: hover) {
  .spellchecker-dictionary-remove-button:hover { color: var(--text-normal); }
}
.modal.mod-new-editor .card, .modal.mod-restricted-mode .card { flex: 1 0 0px; }
.mod-macos .community-modal-controls { app-region: drag; }
.mod-community-modal .modal-sidebar .setting-item { max-width: var(--modal-community-sidebar-width); padding: 0 var(--size-4-3) var(--size-4-1); border: none; gap: var(--size-4-2); }
.mod-community-modal .modal-sidebar .setting-item:first-child { max-width: 500px; gap: 0px; margin-bottom: var(--size-4-2); }
.mod-community-modal .modal-sidebar .setting-item-name { font-size: var(--font-ui-small); padding-left: var(--size-4-1); }
.mod-community-modal .modal-sidebar .setting-item-info { margin: 0px; flex-grow: 0; }
.mod-community-modal .modal-sidebar .search-input-container { width: 100%; }
.mod-community-modal .modal-sidebar button.clickable-icon { padding: 6px 10px; display: flex; align-items: center; color: var(--text-normal); }
.community-modal-details-empty-state { padding: 0px; text-align: center; }
.community-modal-search-summary { font-size: var(--font-ui-small); padding: var(--size-4-1) var(--size-4-3) var(--size-4-3) var(--size-4-4); }
.community-modal-search-results-wrapper { flex: 1 0 auto; overflow: auto; border-top: var(--border-width) solid var(--divider-color); scroll-padding: var(--size-4-3); contain: strict; }
.community-modal-search-results { display: grid; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr)); gap: var(--size-4-3); padding: var(--size-4-3); }
.community-item { position: relative; background-color: var(--background-primary); padding: var(--size-4-3); cursor: var(--cursor); border-radius: var(--radius-m); border: 1px solid var(--background-modifier-border); display: flex; flex-direction: column; gap: var(--size-2-1); }
.community-item:last-child { margin-bottom: 0px; }
.community-item .suggestion-highlight { background-color: var(--text-highlight-bg); }
.community-item.is-selected, .community-item.is-selected:hover { border-color: var(--interactive-accent); background-color: var(--interactive-accent); color: var(--text-on-accent); }
.community-item.is-selected .community-item-author, .community-item.is-selected:hover .community-item-author, .community-item.is-selected .community-item-repo, .community-item.is-selected:hover .community-item-repo, .community-item.is-selected .community-item-downloads, .community-item.is-selected:hover .community-item-downloads, .community-item.is-selected .community-item-updated, .community-item.is-selected:hover .community-item-updated { color: var(--text-on-accent); opacity: 0.8; }
.community-item.is-selected .flair, .community-item.is-selected:hover .flair { color: var(--text-on-accent); background-color: transparent; }
@media (hover: hover) {
  .community-item:hover { border-color: var(--background-modifier-border-hover); }
}
.is-mobile .community-item { max-width: 500px; }
.community-item .flair { margin-left: var(--size-4-1); background-color: var(--tag-background); color: var(--tag-color); vertical-align: middle; top: -1px; }
.community-item-name { font-size: var(--font-ui-medium); line-height: var(--line-height-tight); font-weight: var(--font-medium); }
.community-item-author { font-size: var(--font-ui-smaller); line-height: var(--line-height-tight); color: var(--text-muted); }
.community-item-downloads { font-size: var(--font-ui-smaller); color: var(--text-muted); --icon-color: var(--text-faint); --icon-size: var(--icon-xs); --icon-stroke: var(--icon-xs-stroke-width); }
.community-item-downloads svg { vertical-align: text-bottom; }
.community-item-updated { font-size: var(--font-ui-smaller); color: var(--text-muted); margin-bottom: var(--size-4-2); }
.community-item-downloads-text { margin-left: var(--size-2-2); }
.community-item-desc { font-size: var(--font-ui-small); line-height: var(--line-height-tight); margin-top: 4px; }
.community-item-badge.mod-update { --icon-size: var(--icon-xs); --icon-stroke: var(--icon-xs-stroke-width); color: var(--interactive-accent); position: absolute; top: var(--size-4-3); right: var(--size-4-3); }
.community-item-screenshot { max-width: 100%; object-fit: cover; border-radius: var(--radius-s); aspect-ratio: 16 / 9; image-rendering: -webkit-optimize-contrast; margin-top: var(--size-4-1); }
.community-item-screenshot.mod-unavailable { text-align: center; color: var(--text-muted); }
.community-item-screenshot .placeholder-icon { display: flex; align-items: center; justify-content: center; height: 100%; }
.community-item-screenshot .placeholder-icon .svg-icon { color: var(--text-faint); width: var(--size-4-8); height: var(--size-4-8); }
.community-modal-info-name { font-size: var(--h2-size); font-weight: var(--font-semibold); line-height: var(--line-height-tight); margin-bottom: var(--size-4-6); }
.community-modal-info-author, .community-modal-info-repo, .community-modal-info-version { font-size: var(--font-ui-small); line-height: var(--line-height-tight); color: var(--text-muted); }
.community-modal-info-desc { font-size: var(--font-ui-small); line-height: var(--line-height-tight); margin-top: 4px; }
.community-modal-details { flex: 1 1 calc(var(--modal-max-width) - var(--modal-community-sidebar-width)); overflow: auto; display: flex; flex-direction: column; border-left: 1px solid var(--divider-color); }
.community-modal-info { flex: 1 1 0px; overflow-y: auto; padding: var(--size-4-8) var(--size-4-16); scroll-padding: var(--size-4-4); }
.community-readme { overflow-y: visible; height: auto; padding: var(--size-4-4) 0; }
.community-readme video, .community-readme img { max-width: 100%; }
.community-modal-info-desc { font-size: var(--font-ui-medium); line-height: var(--line-height-tight); margin-top: var(--size-4-2); }
.community-modal-button-container { display: flex; flex-wrap: wrap; gap: var(--size-4-2); margin: 1.5em 0px; }
.community-modal-info-downloads { color: var(--text-muted); margin-top: var(--size-4-1); display: inline-block; --icon-size: var(--icon-xs); --icon-stroke: var(--icon-xs-stroke-width); }
.community-modal-info-downloads-text { margin-left: var(--size-4-1); position: relative; top: -1px; }
.community-modal-readme { font-size: var(--font-text-size); font-family: var(--font-text); line-height: var(--line-height-normal); overflow-wrap: break-word; color: var(--text-normal); user-select: text; }
.installed-plugins-container { padding-top: var(--size-4-4); border-top: 1px solid var(--background-modifier-border); }
.community-modal-grid-button-container { position: absolute; top: var(--size-4-4); right: var(--size-4-12); display: flex; gap: var(--size-4-2); }
.status-bar { position: var(--status-bar-position); width: auto; bottom: 0px; right: 0px; border-radius: var(--status-bar-radius); border-style: solid; border-width: var(--status-bar-border-width); border-color: var(--status-bar-border-color); background-color: var(--status-bar-background); color: var(--status-bar-text-color); display: flex; font-size: var(--status-bar-font-size); justify-content: flex-end; min-height: 18px; padding: var(--size-4-1); gap: var(--size-2-1); user-select: none; z-index: var(--layer-status-bar); font-variant-numeric: tabular-nums; }
.status-bar-item { border-radius: var(--radius-s); display: inline-flex; align-items: center; padding: 3px var(--size-2-2); line-height: 1; }
.status-bar-item.mod-clickable { cursor: var(--cursor); }
@media (hover: hover) {
  .status-bar-item.mod-clickable:hover { background-color: var(--background-modifier-hover); color: var(--text-normal); }
}
.status-bar-item.plugin-editor-status, .status-bar-item.plugin-sync { padding: 0 var(--size-2-2); }
@media (hover: hover) {
  .status-bar-item.plugin-editor-status:hover, .status-bar-item.plugin-sync:hover { background-color: var(--background-modifier-hover); }
}
.status-bar-item-icon { vertical-align: middle; display: flex; align-items: center; }
.status-bar-item-segment { margin-right: var(--size-4-2); }
.status-bar-item-segment:last-child { margin-right: 0px; }
.is-screenshotting .status-bar { display: none; }
.titlebar { app-region: drag; position: fixed; top: 0px; left: 0px; right: 0px; display: flex; background-color: var(--titlebar-background); border-bottom: var(--titlebar-border-width) solid var(--titlebar-border-color); }
.titlebar-inner { color: var(--titlebar-text-color); font-weight: var(--titlebar-text-weight); width: 100%; display: flex; }
.is-focused .titlebar-inner { color: var(--titlebar-text-color-focused); }
.titlebar-text { opacity: 0.85; position: absolute; width: 100%; height: 100%; top: 0px; left: 0px; flex-grow: 1; font-size: var(--font-ui-small); text-align: center; display: flex; justify-content: center; align-items: center; padding: 0px 125px; overflow: hidden; white-space: nowrap; text-overflow: ellipsis; }
.titlebar-button-container { display: flex; position: absolute; top: 0px; }
.mod-macos .titlebar-button-container { top: 8px; }
.titlebar-button-container.mod-left { left: 0px; }
.mod-macos .titlebar-button-container.mod-left { left: calc(80px / var(--zoom-factor)); }
.titlebar-button-container .mod-back, .titlebar-button-container .mod-forward { color: var(--icon-color); }
.titlebar-button-container .mod-back .svg-icon, .titlebar-button-container .mod-forward .svg-icon { width: 14px; height: 14px; stroke-width: 2.25px; }
@media (hover: hover) {
  .titlebar-button-container .mod-back:hover, .titlebar-button-container .mod-forward:hover { color: var(--icon-color-hover); }
}
.titlebar-button-container.mod-right { right: 0px; }
.titlebar-button { app-region: no-drag; padding: var(--size-2-2) var(--size-2-3); cursor: var(--cursor); display: inline-flex; align-items: center; }
@media (hover: hover) {
  .titlebar-button:hover { opacity: 1; background-color: var(--background-modifier-hover); }
  .titlebar-button.mod-close:hover { background-color: var(--background-modifier-error); }
}
.mod-macos .titlebar-button { border-radius: var(--radius-s); }
body.is-frameless.is-hidden-frameless { padding-top: 0px !important; }
.is-hidden-frameless.mod-macos .titlebar { display: none; }
.is-hidden-frameless.mod-windows .titlebar, .is-hidden-frameless.mod-linux .titlebar { background: transparent; border: none; z-index: var(--layer-popover); pointer-events: none; }
.is-hidden-frameless.mod-windows .titlebar-button.mod-back, .is-hidden-frameless.mod-linux .titlebar-button.mod-back, .is-hidden-frameless.mod-windows .titlebar-button.mod-forward, .is-hidden-frameless.mod-linux .titlebar-button.mod-forward, .is-hidden-frameless.mod-windows .titlebar-text, .is-hidden-frameless.mod-linux .titlebar-text { display: none; }
.is-hidden-frameless.mod-windows .titlebar-button-container, .is-hidden-frameless.mod-linux .titlebar-button-container { pointer-events: auto; }
.mod-linux .titlebar-button-container, .mod-windows .titlebar-button-container { height: 100%; }
.mod-linux .titlebar-button, .mod-windows .titlebar-button { padding: 0px 16px; display: flex; align-items: center; }
.mod-linux .titlebar-button.mod-logo, .mod-windows .titlebar-button.mod-logo { padding: 4px 8px; }
@media (hover: hover) {
  .mod-linux .titlebar-button.mod-close:hover, .mod-windows .titlebar-button.mod-close:hover { background-color: var(--background-modifier-error); }
  .mod-linux .titlebar-button.mod-close:hover .svg-icon, .mod-windows .titlebar-button.mod-close:hover .svg-icon { fill: white; stroke: white; }
}
@media screen and (max-width: 300px) {
  .titlebar-text { display: none; }
}
.is-translucent:not(.is-fullscreen) { --nav-collapse-icon-color: rgba(var(--mono-rgb-100), 0.3); --nav-collapse-icon-color-collapsed: rgba(var(--mono-rgb-100), 0.3); --divider-color: rgba(0, 0, 0, 0.15); }
.is-translucent:not(.is-fullscreen) .titlebar, .is-translucent:not(.is-fullscreen) .app-container { background-color: var(--workspace-background-translucent); }
.is-translucent:not(.is-fullscreen) .workspace-ribbon.mod-left, .is-translucent:not(.is-fullscreen) .workspace-tabs, .is-translucent:not(.is-fullscreen) .workspace-split.mod-root, .is-translucent:not(.is-fullscreen) .sidebar-toggle-button, .is-translucent:not(.is-fullscreen) .mod-left-split .workspace-tab-header-container, .is-translucent:not(.is-fullscreen) .mod-right-split .workspace-tab-header-container, .is-translucent:not(.is-fullscreen) .mod-top .workspace-tab-header-container, .is-translucent:not(.is-fullscreen) .workspace-tabs .workspace-leaf, .is-translucent:not(.is-fullscreen) .workspace-ribbon.mod-left::before { background-color: transparent !important; }
.workspace { background-color: var(--background-primary); display: flex; flex: 1 0 0px; transition: padding-left 100ms ease-in 0s; overflow: hidden; height: 100%; }
.is-translucent .workspace { background-color: transparent; }
.workspace-split { display: flex; position: relative; }
.workspace-split.mod-vertical > .workspace-split:last-child { padding-right: 0px; }
.workspace-split:last-child:not(.mod-right-split) > .workspace-leaf-resize-handle { display: none; }
.workspace-split.mod-vertical { flex-direction: row; }
.workspace-split.mod-horizontal { flex-direction: column; }
.workspace-split.mod-root { background-color: var(--background-primary); }
.workspace-leaf { display: flex; flex-direction: column; position: relative; overflow: hidden; isolation: isolate; contain: strict !important; }
.workspace-split.mod-root .workspace-leaf:last-child .workspace-leaf-resize-handle { display: none; }
.workspace-leaf.is-highlighted::before { content: " "; position: absolute; height: 100%; width: 100%; top: 0px; left: 0px; background-color: hsla(var(--interactive-accent-hsl), 0.25); z-index: var(--layer-popover); pointer-events: none; }
.workspace > .workspace-leaf, .workspace > .workspace-split { height: 100%; width: 100%; }
.workspace-split.mod-root > .workspace-leaf-resize-handle { display: none; }
.workspace-leaf-resize-handle { app-region: no-drag; position: absolute; z-index: var(--layer-cover); background-color: transparent; transition: background-color 200ms ease-in-out 0s, border-color 200ms ease-in-out 0s, opacity 200ms ease-in-out 0s; border-right-color: ; border-bottom-color: ; border-left-color: ; border-top-style: initial; border-top-color: initial; border-width: var(--divider-width); margin: 0px; }
@media (hover: hover) {
  .workspace-leaf-resize-handle:hover { background-color: var(--divider-color-hover); border-color: var(--divider-color-hover); }
  .is-translucent .workspace-leaf-resize-handle:hover { background-color: var(--divider-color-hover); border-color: var(--divider-color-hover); }
}
.workspace-split.mod-horizontal > * > .workspace-leaf-resize-handle { bottom: 0px; left: 0px; border-bottom-style: solid; border-bottom-width: var(--divider-width); height: var(--divider-width-hover); width: 100%; cursor: row-resize; }
.workspace-split.mod-vertical > * > .workspace-leaf-resize-handle, .workspace-split.mod-left-split > .workspace-leaf-resize-handle, .workspace-split.mod-right-split > .workspace-leaf-resize-handle { right: 0px; bottom: 0px; width: var(--divider-width-hover); height: var(--divider-vertical-height); cursor: col-resize; }
.workspace-split.mod-right-split > .workspace-leaf-resize-handle { border-left-style: solid; border-left-width: var(--divider-width); }
.workspace-split.mod-vertical > * > .workspace-leaf-resize-handle, .workspace-split.mod-left-split > .workspace-leaf-resize-handle { border-right-style: solid; border-right-width: var(--divider-width); }
.workspace-split.mod-right-split > .workspace-leaf-resize-handle { right: unset; left: 0px; }
.workspace-split.mod-vertical > * { height: 100%; flex: 1 0 0px; width: 0px; }
.workspace-split.mod-horizontal > * { width: 100%; flex: 1 0 0px; height: 0px; }
.workspace-split.mod-left-split, .workspace-split.mod-right-split { flex: 0 0 auto; }
.is-translucent .workspace-split.mod-left-split.is-sidedock-collapsed .workspace-tabs, .is-translucent .workspace-split.mod-right-split.is-sidedock-collapsed .workspace-tabs { visibility: hidden; }
.workspace-split.mod-left-split > .workspace-leaf-resize-handle, .workspace-split.mod-right-split > .workspace-leaf-resize-handle { z-index: var(--layer-status-bar); height: var(--divider-vertical-height); top: unset; bottom: 0px; }
.view-header-nav-buttons { --icon-size: var(--icon-s); align-items: center; display: flex; margin-right: var(--size-4-1); }
body.is-phone .view-header-nav-buttons { display: none; }
.workspace-leaf-content { width: 100%; height: 100%; overflow: hidden; position: relative; display: flex; flex-direction: column; }
.workspace-leaf-content .view-content { padding: var(--size-4-4); overflow: auto; }
.workspace-leaf-content[data-type="markdown"] .view-content { padding: 0px; overflow: hidden; }
.workspace-leaf-content[data-type="backlink"] .view-content, .workspace-leaf-content[data-type="outgoing-link"] .view-content { padding: 0px; overflow: hidden; display: flex; flex-direction: column; }
.workspace-leaf-content .image-container, .workspace-leaf-content .audio-container, .workspace-leaf-content .video-container { text-align: center; }
.workspace-leaf-content img:not([width]), .workspace-leaf-content audio, .workspace-leaf-content video { max-width: 100%; }
.workspace-fake-target-overlay, .workspace-drop-overlay { will-change: transform, width, height; position: fixed; left: 0px; top: 0px; width: 0px; height: 0px; transform: translate(0px, 0px); transition: all 100ms ease-in-out 0s; z-index: var(--layer-cover); pointer-events: none; }
.workspace-drop-overlay::before { content: " "; position: absolute; width: calc(100% - 6px); height: calc(100% - 6px); inset: 0px; margin: auto; background-color: var(--interactive-accent); border-radius: var(--radius-m); opacity: 0.5; }
.workspace-fake-target-container { visibility: hidden; position: absolute; pointer-events: none; top: 0px; left: 0px; }
.workspace-fake-target-overlay { visibility: visible; overflow: hidden; background-color: var(--background-primary); }
.workspace-fake-target-overlay > * { width: 100%; height: 100%; }
.workspace-tabs { overflow: hidden; display: flex; flex-direction: column; position: relative; }
.workspace-tabs > * { flex: 1 0 0px; }
.workspace-tabs .workspace-leaf { height: 100%; }
.workspace-split.mod-right-split .workspace-tabs { padding-right: 0px; }
.workspace-tabs:last-child .workspace-leaf-resize-handle { display: none; }
.workspace-fake-target-overlay:not(.is-in-sidebar) .workspace-tabs .workspace-leaf, .mod-root .workspace-tabs .workspace-leaf { background-color: var(--background-primary); }
.workspace-tabs .workspace-leaf { background-color: var(--background-secondary); }
.workspace-tabs .workspace-leaf .view-content { height: 100%; }
.workspace-tab-header-container { display: flex; background-color: var(--tab-container-background); height: var(--header-height); border-bottom: var(--tab-outline-width) solid var(--tab-outline-color); flex: 0 0 auto; padding-left: 0px; padding-right: var(--size-4-2); position: relative; }
.is-phone .workspace-tab-header-container { display: none; }
.workspace-tab-header-container-inner { display: flex; flex: 0 1 auto; overflow: auto; margin: 6px -5px calc(var(--tab-outline-width) * -1); padding: 1px 15px 0px; }
.mod-root .workspace-tab-header-container-inner { padding: 1px 15px 0px; }
.workspace-tab-header-container-inner::-webkit-scrollbar, .workspace-tab-header-container-inner::-webkit-scrollbar-thumb { display: none; }
.workspace-tab-header-inner-icon { flex: 0 0 auto; display: flex; }
.mod-root .workspace-tab-header[data-type="markdown"] .workspace-tab-header-inner-icon, .mod-root .workspace-tab-header[data-type="empty"] .workspace-tab-header-inner-icon { display: none; }
.is-focused .workspace-tab-header { color: var(--tab-text-color-focused); }
.is-focused .workspace-tab-header.is-active { color: var(--tab-text-color-focused-active); }
.is-focused .mod-active .workspace-tab-header.is-active .workspace-tab-header-inner-icon, .is-focused .mod-active .workspace-tab-header.is-active .workspace-tab-header-inner-title { color: var(--tab-text-color-focused-active-current); }
.is-focused .mod-active .workspace-tab-header.is-active.is-highlighted .workspace-tab-header-inner-icon, .is-focused .mod-active .workspace-tab-header.is-active.is-highlighted .workspace-tab-header-inner-title { color: var(--tab-text-color-focused-highlighted); }
.is-focused .workspace-tab-header.active.is-highlighted .workspace-tab-header-inner-icon, .is-focused .workspace-tab-header.is-highlighted .workspace-tab-header-inner-icon, .is-focused .workspace-tab-header.active.is-highlighted .workspace-tab-header-inner-title, .is-focused .workspace-tab-header.is-highlighted .workspace-tab-header-inner-title { color: var(--tab-text-color-focused-highlighted); }
.workspace-tab-header { app-region: no-drag; color: var(--tab-text-color); display: flex; position: relative; padding: 1px 4px 3.5px; scroll-margin-inline-start: var(--size-2-3); scroll-margin-inline-end: var(--size-4-1); text-align: center; border-radius: var(--tab-radius-active); }
.workspace-tab-header:not(.is-active):hover .workspace-tab-header-inner { background-color: var(--background-modifier-hover); }
.workspace-tab-header::before, .workspace-tab-header::after { position: absolute; bottom: 0px; content: ""; width: calc(var(--tab-curve) * 2); height: calc(var(--tab-curve) * 2); border-radius: 100%; box-shadow: 0 0 0 calc(var(--tab-curve) * 3) transparent; }
.workspace-tab-header::before { left: calc(var(--tab-curve) * -2); clip-path: inset(50% calc(var(--tab-curve) * -1) 0 50%); }
.workspace-tab-header::after { right: calc(var(--tab-curve) * -2); clip-path: inset(50% 50% 0 calc(var(--tab-curve) * -1)); }
.workspace-tab-header.is-active { box-shadow: 0 0 0 var(--tab-outline-width) var(--tab-outline-color); color: var(--tab-text-color-active); background-color: var(--tab-background-active); }
.workspace-split.mod-root .workspace-tab-header.is-active::before, .workspace-split.mod-root .workspace-tab-header.is-active::after { box-shadow: inset 0 0 0 var(--tab-outline-width) var(--tab-outline-color), 0 0 0 calc(var(--tab-curve) * 4) var(--tab-background-active); }
.workspace-tab-header.is-active .workspace-tab-header-inner::after { opacity: 0; }
.workspace-tab-container { display: flex; overflow: hidden; }
.workspace-tab-container > * { flex: 1 0 0px; }
.workspace-tab-header-inner { align-items: center; display: flex; gap: var(--size-2-1); height: 100%; border-radius: var(--tab-radius); overflow: hidden; padding: 0px 8px; width: 100%; }
.workspace-tab-header-inner .workspace-tab-header-inner-icon { color: var(--icon-color); opacity: var(--icon-opacity); }
@media (hover: hover) {
  .workspace-tab-header-inner:hover .workspace-tab-header-inner-icon { color: var(--icon-color-hover); opacity: var(--icon-opacity-hover); }
}
.mod-root .workspace-tab-header-inner { padding: 0px 3px 0px 6px; }
.workspace-tab-header-inner-title { flex: 1 1 auto; font-size: var(--tab-font-size); font-weight: var(--tab-font-weight); overflow: hidden; text-align: left; text-overflow: ellipsis; white-space: nowrap; width: 100%; }
.workspace-tab-header-status-container { display: flex; flex-shrink: 0; gap: var(--size-2-1); justify-content: center; }
.workspace-tab-header-status-container:empty { display: none; }
.workspace-tab-header-status-icon, .workspace-tab-header-inner-close-button { cursor: var(--cursor); padding: var(--size-2-1); border-radius: var(--radius-s); display: flex; align-items: center; --icon-size: var(--icon-xs); --icon-stroke: var(--icon-xs-stroke-width); }
@media (hover: hover) {
  .workspace-tab-header.is-active .workspace-tab-header-status-icon:hover, .workspace-tab-header.is-active .workspace-tab-header-inner-close-button:hover { background-color: var(--background-modifier-hover); }
  .mod-root .workspace-tab-header.is-active .workspace-tab-header-status-icon.mod-linked:hover, .mod-root .workspace-tab-header.is-active .workspace-tab-header-inner-close-button.mod-linked:hover, .mod-root .workspace-tab-header.is-active .workspace-tab-header-status-icon.mod-pinned:hover, .mod-root .workspace-tab-header.is-active .workspace-tab-header-inner-close-button.mod-pinned:hover { background-color: var(--background-modifier-active-hover); }
}
.workspace-tab-header.is-active .workspace-tab-header-status-icon::after, .workspace-tab-header.is-active .workspace-tab-header-inner-close-button::after { background-color: transparent; }
@media (hover: hover) {
  .workspace-tab-header-inner-close-button:hover { color: var(--tab-text-color-focused-active-current); }
}
.workspace-tab-header:hover .workspace-tab-header-inner-close-button { color: var(--tab-text-color-focused); }
@media (hover: hover) {
  .workspace-tab-header:hover .workspace-tab-header-inner-close-button:hover { color: var(--tab-text-color-focused-active-current); }
}
.workspace-tab-header.is-active .workspace-tab-header-inner-close-button { color: var(--tab-text-color-focused); }
@media (hover: hover) {
  .workspace-tab-header.is-active .workspace-tab-header-inner-close-button:hover { color: var(--tab-text-color-focused-active-current); }
}
.workspace-sidedock-empty-state { font-size: var(--font-ui-small); padding: 20px 30px; }
.workspace-tab-header.is-before-active .workspace-tab-header-inner { border-bottom-right-radius: 10px; }
.workspace-tab-header-spacer { display: flex; flex-grow: 1; }
body:not(.is-grabbing):not(.is-fullscreen) .workspace-tabs.mod-top .workspace-tab-header-spacer { app-region: drag; }
body:not(.is-grabbing):not(.is-fullscreen).is-hidden-frameless .mod-top .workspace-tab-header-container { app-region: drag; }
.workspace-tab-header-tab-list, .workspace-tab-header-new-tab { app-region: no-drag; display: none; z-index: 1; align-items: center; }
.titlebar .workspace-tab-header-tab-list, .titlebar .workspace-tab-header-new-tab, .mod-root .workspace-tab-header-tab-list, .mod-root .workspace-tab-header-new-tab { display: flex; }
.workspace-tab-header-tab-list .clickable-icon, .workspace-tab-header-new-tab .clickable-icon { color: var(--icon-color); padding: var(--size-2-2); --icon-size: var(--icon-m); --icon-stroke: var(--icon-m-stroke-width); align-items: center; }
.workspace-tab-header-new-tab { padding: var(--size-4-2) 0 var(--size-2-3); margin-right: var(--size-4-3); margin-left: -4px; }
.workspace-tab-header-tab-list { margin-right: var(--size-4-1); padding: var(--size-4-2) 0 var(--size-2-3); }
.workspace-fake-target-overlay.is-in-sidebar .workspace-tab-header-inner-title, .mod-left-split .workspace-tab-header-inner-title, .mod-right-split .workspace-tab-header-inner-title { display: var(--sidebar-tab-text-display); }
.workspace-fake-target-overlay.is-in-sidebar .workspace-tab-header-inner-close-button, .mod-left-split .workspace-tab-header-inner-close-button, .mod-right-split .workspace-tab-header-inner-close-button { display: none; }
body > .workspace-split { height: 100%; }
.mod-root .workspace-tabs > .workspace-leaf .view-header-title { white-space: normal; }
.mod-root .workspace-tab-header-status-icon { color: var(--text-accent); }
.mod-root .workspace-tab-header-status-icon, .mod-root .workspace-tab-header-inner-icon { --icon-size: var(--icon-xs); --icon-stroke: var(--icon-xs-stroke-width); }
.mod-root .mod-pinned, .mod-root .workspace-tab-header-inner-close-button { --icon-size: var(--icon-s); --icon-stroke: var(--icon-s-stroke-width); }
.mod-right-split .markdown-preview-view, .mod-left-split .markdown-preview-view, .mod-right-split .markdown-source-view.mod-cm6 .cm-scroller, .mod-left-split .markdown-source-view.mod-cm6 .cm-scroller { --file-margins: var(--size-4-5); }
.mod-right-split .markdown-preview-view, .mod-left-split .markdown-preview-view, .mod-right-split .markdown-source-view, .mod-left-split .markdown-source-view { font-size: var(--sidebar-markdown-font-size); }
.mod-left-split .workspace-tab-header-container-inner, .mod-right-split .workspace-tab-header-container-inner { padding: 1px 8px 7px; margin: 6px 0px 0px; gap: 3px; }
.mod-left-split .workspace-tab-header, .mod-right-split .workspace-tab-header { box-shadow: none; background-color: transparent; padding: 0px; margin: 0px; border-radius: var(--radius-s); }
.mod-left-split .workspace-tab-header::before, .mod-right-split .workspace-tab-header::before, .mod-left-split .workspace-tab-header::after, .mod-right-split .workspace-tab-header::after { display: none; }
.mod-left-split .workspace-tab-header:active .workspace-tab-header-inner-icon, .mod-right-split .workspace-tab-header:active .workspace-tab-header-inner-icon { color: var(--icon-color-focused); }
.mod-left-split .workspace-tab-header.has-active-menu, .mod-right-split .workspace-tab-header.has-active-menu, .mod-left-split .workspace-tab-header.is-active, .mod-right-split .workspace-tab-header.is-active { background-color: var(--background-modifier-hover); }
@media (hover: hover) {
  .mod-left-split .workspace-tab-header.has-active-menu:hover, .mod-right-split .workspace-tab-header.has-active-menu:hover, .mod-left-split .workspace-tab-header.is-active:hover, .mod-right-split .workspace-tab-header.is-active:hover { background-color: var(--background-modifier-hover); }
}
.mod-left-split .workspace-tab-header.has-active-menu .workspace-tab-header-inner-icon, .mod-right-split .workspace-tab-header.has-active-menu .workspace-tab-header-inner-icon, .mod-left-split .workspace-tab-header.is-active .workspace-tab-header-inner-icon, .mod-right-split .workspace-tab-header.is-active .workspace-tab-header-inner-icon { opacity: var(--icon-opacity-active); color: var(--icon-color-focused); }
.workspace .mod-root .workspace-tab-header { app-region: no-drag; flex: 1 1 0px; width: var(--tab-width); min-width: 0px; max-width: var(--tab-max-width); padding: 1px 3px 3.5px; }
.workspace .mod-root .workspace-tab-header .workspace-tab-header-status-container { position: sticky; right: 0px; }
.workspace .mod-root .workspace-tab-header .workspace-tab-header-inner-close-button { position: sticky; right: 0px; }
.workspace .mod-root .workspace-tab-header.is-active:hover .workspace-tab-header-inner-close-button, .workspace .mod-root .workspace-tab-header.is-active .workspace-tab-header-inner-close-button { pointer-events: all; opacity: 1; }
.workspace .mod-root .workspace-tab-header.is-active:hover .workspace-tab-header-inner-close-button svg, .workspace .mod-root .workspace-tab-header.is-active .workspace-tab-header-inner-close-button svg { opacity: 1; }
.workspace .mod-root .workspace-tab-header.is-active .workspace-tab-header-inner-close-button::after { background-color: transparent; }
.workspace .mod-root .workspace-tab-header-inner::after { position: absolute; right: -0.5px; width: 1px; background-color: var(--tab-divider-color); content: ""; height: 20px; }
.workspace .mod-root .workspace-tab-header-inner-icon { display: flex; padding-right: 4px; }
.workspace .mod-root .workspace-tab-header[data-type="markdown"] .workspace-tab-header-inner-icon, .workspace .mod-root .workspace-tab-header[data-type="empty"] .workspace-tab-header-inner-icon { display: none; }
.workspace .mod-root .workspace-tab-header-inner-title { text-overflow: ellipsis; width: 100%; }
.workspace .mod-root .workspace-tab-header-status-container.mod-linked { display: none; }
.workspace .mod-root .workspace-tab-header-spacer { flex-shrink: 1; }
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-header-container-inner { padding: 0 0 0 var(--size-4-3); margin: 0px; }
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container { overflow: auto hidden; position: relative; display: flex; flex-direction: row; }
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container > * { flex: 0 0 auto; position: sticky; }
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-tab-header { width: var(--tab-stacked-header-width); writing-mode: var(--tab-stacked-text-writing-mode); text-orientation: sideways; background-color: var(--background-primary); padding: 0px; border-radius: 0px; box-shadow: -1px 0 0 0 var(--tab-outline-color), var(--tab-stacked-shadow); --no-tooltip: true; }
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-tab-header::before, .workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-tab-header::after { display: none; }
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-tab-header:hover .workspace-tab-header-inner { background-color: transparent; }
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-tab-header-inner { padding: var(--size-4-2) var(--size-4-2) var(--size-4-4); border-radius: 0px; }
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-tab-header-inner::after { display: none; }
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-tab-header-inner-title { order: 3; width: auto; -webkit-mask-image: unset; padding: var(--size-4-1) 0; transform: var(--tab-stacked-text-transform); text-align: var(--tab-stacked-text-align); font-weight: var(--tab-stacked-font-weight); font-size: var(--tab-stacked-font-size); text-orientation: mixed; }
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-tab-header-inner-icon { order: 2; cursor: grab; display: flex; padding: var(--size-2-2); border-radius: var(--radius-s); }
@media (hover: hover) {
  .workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-tab-header-inner-icon:hover { background-color: var(--background-modifier-hover); }
}
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-tab-header-inner-icon:active { cursor: grabbing; }
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-tab-header-inner-close-button { color: var(--tab-text-color-focused); }
@media (hover: hover) {
  .workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-tab-header-inner-close-button:hover { background-color: var(--background-modifier-hover); }
}
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-leaf { width: var(--tab-stacked-pane-width); contain: strict; }
.workspace .mod-root .workspace-tabs.mod-stacked .workspace-tab-container .workspace-leaf.is-hidden > * { display: none; }
.sidebar-toggle-button { height: calc(var(--header-height) - 1px); display: flex; justify-content: center; padding: var(--size-4-2) 0 7px 0; app-region: no-drag; --icon-size: var(--icon-l); --icon-stroke: var(--icon-l-stroke-width); }
.mod-macos.is-hidden-frameless:not(.is-popout-window) .sidebar-toggle-button.mod-right { background-color: var(--tab-container-background); position: fixed; top: 0px; right: 0px; padding-right: var(--size-4-2); z-index: var(--layer-popover); }
.mod-macos.is-hidden-frameless:not(.is-popout-window) .workspace .workspace-tabs.mod-top-right-space .workspace-tab-header-container { padding-right: 38px; }
.button-container { margin-top: 20px; }
button { app-region: no-drag; display: inline-flex; align-items: center; justify-content: center; color: var(--text-normal); font-size: var(--font-ui-small); border-radius: var(--button-radius); border: 0px; padding: var(--size-4-1) var(--size-4-3); height: var(--input-height); font-weight: var(--input-font-weight); cursor: var(--cursor); font-family: inherit; outline: none; user-select: none; white-space: nowrap; }
button:not(.clickable-icon) { background-color: var(--interactive-normal); box-shadow: var(--input-shadow); }
@media (hover: hover) {
  button:hover { background-color: var(--interactive-hover); box-shadow: var(--input-shadow-hover); }
}
button[aria-disabled="true"] { background-color: var(--interactive-normal); }
button:focus-visible { box-shadow: 0 0 0 3px var(--background-modifier-border-focus); }
button[disabled="true"] { cursor: not-allowed; }
button.mod-cta { background-color: var(--interactive-accent); color: var(--text-on-accent); }
@media (hover: hover) {
  button.mod-cta:hover { background-color: var(--interactive-accent-hover); }
}
button.mod-cta:focus-visible { box-shadow: 0 0 0 3px var(--background-modifier-border-focus); }
button.mod-muted { background-color: var(--background-secondary); color: var(--text-muted); }
@media (hover: hover) {
  button.mod-muted:hover { background-color: var(--background-secondary); }
}
button.mod-warning { background-color: var(--background-modifier-error); color: var(--text-on-accent); }
@media (hover: hover) {
  button.mod-warning:hover { background-color: var(--background-modifier-error-hover); }
}
.icon-button-group { display: inline-block; }
.icon-button { display: inline-block; color: var(--interactive-normal); }
.rich-button { width: auto; padding-top: 5px; }
.rich-button-icon { position: relative; top: 6px; }
.horizontal-preference-group { display: flex; }
.horizontal-preference-group button { border-radius: 0px; margin: 0px -1px; }
.horizontal-preference-group button:first-child { border-top-left-radius: var(--input-radius); border-bottom-left-radius: var(--input-radius); }
.horizontal-preference-group button:last-child { border-top-right-radius: var(--input-radius); border-bottom-right-radius: var(--input-radius); }
.horizontal-preference-group button.is-selected { background-color: var(--interactive-accent); color: var(--text-on-accent); }
@media (hover: hover) {
  .horizontal-preference-group button.is-selected:hover { background-color: var(--interactive-accent-hover); }
}
.card-container { display: flex; }
.card-container.mod-horizontal { flex-direction: column; }
.card { background-color: var(--background-secondary-alt); border-radius: 4px; border: 1px solid var(--background-modifier-border); margin: 0px 10px; padding: 15px 30px; display: flex; flex-direction: column; flex-grow: 1; }
.card ul { padding: 0px; }
.card .button-container { margin: 10px 0px; }
.card-container.mod-horizontal .card { margin: 10px 0px; }
.card-container.mod-horizontal .card ul { padding-left: 24px; }
.card li { margin: 5px 0px; }
.card.u-clickable { cursor: var(--cursor); }
@media (hover: hover) {
  .card.u-clickable:hover { border: 1px solid var(--interactive-accent); background-color: hsla(var(--interactive-accent-hsl), 0.1); }
}
.card.is-selected { border: 1px solid var(--interactive-accent); background-color: hsla(var(--interactive-accent-hsl), 0.2); }
.card-title { text-align: center; font-size: 20px; line-height: 30px; color: var(--text-muted); margin-bottom: 8px; }
.card-description { color: var(--text-muted); font-size: var(--font-ui-small); line-height: 20px; flex-grow: 1; }
.changelog-item { margin: var(--size-4-2) 0; font-size: var(--font-ui-medium); line-height: var(--line-height); }
.changelog-item::before { content: attr(data-label); width: 50px; border-radius: var(--radius-m); font-size: var(--font-ui-small); display: inline-block; text-align: center; margin-right: 14px; text-transform: uppercase; letter-spacing: 1px; line-height: 22px; }
.changelog-item.mod-success::before { background-color: var(--background-modifier-success); }
.changelog-item.mod-highlighted::before { background-color: var(--interactive-accent); }
.page-container { width: 50vw; max-width: 1000px; margin: 0px auto; padding: 50px 0px; background-color: var(--background-primary); }
.page-title { font-weight: var(--font-extrabold); font-size: 46px; }
[contenteditable] { outline: none; }
.rich-link { color: var(--text-accent); position: relative; padding-left: 30px; }
.rich-link-icon { position: absolute; left: 5px; top: 3px; }
.horizontal-link-group { text-align: center; }
.horizontal-link-group a, .horizontal-link-group span { margin: 0px 10px; }
.footer-link-group { list-style: none; display: inline-block; margin: 0px 30px; padding: 0px; }
.footer-header { font-size: 22px; line-height: 30px; margin-bottom: 10px; }
.footer-link { margin: 4px 0px; }
.components-container .menu { position: relative; display: inline-block; }
.list-item { display: flex; padding: 0px; margin: 8px 0px; gap: var(--size-4-2); align-items: center; }
.list-item-part.mod-extended { flex-grow: 1; overflow-wrap: anywhere; }
.list-item-part.clickable-icon { display: flex; align-items: center; justify-content: center; padding: var(--size-2-2); cursor: var(--cursor); border-radius: var(--radius-s); color: var(--icon-color); }
.list-item-part.clickable-icon:hover, .list-item-part.clickable-icon:active { color: var(--icon-color-hover); background-color: var(--background-modifier-hover); }
.lightbox { display: none; position: fixed; z-index: 999; width: 100%; height: 100%; text-align: center; top: 0px; left: 0px; background: rgba(0, 0, 0, 0.8); }
.lightbox img { max-width: 90vw; max-height: 90vh; margin-top: 5vh; }
.lightbox:target { display: block; }
.u-center-text { text-align: center; }
.u-faded-text { color: var(--text-muted); }
.u-pop { color: var(--text-accent); font-weight: var(--font-semibold); }
.u-muted { color: var(--text-muted); }
.u-small { font-size: 0.8em; }
.u-clickable { cursor: var(--cursor); }
.u-pop-bg { background-color: var(--interactive-accent); color: var(--text-on-accent); display: inline-block; padding: 3px 16px; border-radius: 20px; opacity: 0.6; cursor: default; }
@media (hover: hover) {
  .u-pop-bg:hover { opacity: 1; }
}
.components-container h3 { font-weight: var(--font-semibold); font-size: 30px; margin: 60px 0px 25px; }
.components-container .vertical-tabs-container { height: 300px; }
.components-container .checkbox-demo { margin: 10px 0px; }
.components-container .checkbox-demo label { display: inline-block; width: 300px; }
.components-container .prompt { position: static; }
@keyframes node-inserted { 
  0% { outline-color: rgb(255, 255, 255); }
  100% { outline-color: rgb(0, 0, 0); }
}
.node-insert-event { animation-duration: 0.01s; animation-name: node-inserted; }
.diff-view { height: 100%; overflow: auto; user-select: text; }
.diff-line { padding: 0 var(--size-4-2); }
.diff-line.mod-left { background-color: rgba(var(--background-modifier-error-rgb), 0.2); }
.diff-line.mod-left .diff-changed { background-color: rgba(var(--background-modifier-error-rgb), 0.4); }
.diff-line.mod-right { background-color: rgba(var(--background-modifier-success-rgb), 0.2); }
.diff-line.mod-right .diff-changed { background-color: rgba(var(--background-modifier-success-rgb), 0.4); }
.diff-collapsed { text-align: center; color: var(--text-muted); cursor: pointer; font-size: var(--font-ui-small); margin: var(--size-4-2) 0; }
.diff-collapsed:hover { color: var(--text-accent); }
.markdown-reading-view.is-searching, .markdown-source-view.is-replacing, .markdown-source-view.is-searching { flex-direction: column-reverse; }
.mod-active .document-search-container { background-color: var(--background-primary); }
.document-search-container { display: flex; flex-direction: column; padding: var(--size-4-2) 0; margin: 0 var(--size-4-4); gap: var(--size-4-2); z-index: var(--layer-popover); }
.document-search, .document-replace { width: 100%; max-width: var(--file-line-width); margin: 0px auto; display: flex; padding: 0 var(--size-4-2); gap: var(--size-4-2); }
.document-replace { display: none; }
.document-search-container.mod-replace-mode .document-replace { display: flex; }
input.document-search-input, input.document-replace-input { flex-grow: 1; }
input.document-search-input.mod-no-match, input.document-replace-input.mod-no-match { background-color: rgba(var(--background-modifier-error-rgb), 0.2); }
@media (hover: hover) {
  input.document-search-input.mod-no-match:hover, input.document-replace-input.mod-no-match:hover { background-color: rgba(var(--background-modifier-error-rgb), 0.2); }
}
.document-replace-buttons, .document-search-buttons { display: flex; gap: var(--size-4-2); align-items: center; }
.document-search-button { font-size: var(--font-ui-small); padding: 0 var(--size-4-2); color: var(--text-muted); }
.document-search-close-button { cursor: var(--cursor); position: relative; top: 2px; font-size: 24px; line-height: 20px; height: 24px; width: 24px; padding: 0 var(--size-2-2); border-radius: var(--radius-s); color: var(--text-muted); }
.document-search-close-button::before { font-family: Inter, sans-serif; content: "×"; font-weight: 300; }
@media (hover: hover) {
  .document-search-close-button:hover { background-color: var(--background-modifier-hover); color: var(--text-normal); }
}
.markdown-rendered .search-highlight > div { position: absolute; pointer-events: none; box-shadow: 0 0 0px 2px var(--text-normal); opacity: 0.3; mix-blend-mode: var(--highlight-mix-blend-mode); border-radius: 2px; }
.markdown-rendered .search-highlight > div.is-active { box-shadow: 0 0 0px 3px var(--text-accent); opacity: 1; }
.markdown-source-view.mod-cm5 { position: relative; padding-left: 20px; padding-right: 30px; }
.workspace-leaf-content.is-read-mode .markdown-source-view.mod-cm5 { z-index: 0; }
.markdown-source-view.mod-cm5 .document-search-container { position: absolute; top: 0px; left: 0px; width: 100%; z-index: 5; }
.markdown-source-view.mod-cm6 .document-search-container { flex: 0 0 auto; }
.is-flashing { transition: all 0.25s ease 0s; background-color: var(--text-highlight-bg); color: var(--text-normal); mix-blend-mode: var(--highlight-mix-blend-mode); border-radius: var(--radius-s); }
[dir="rtl"] .dropdown, :root:lang(ar) .dropdown, :root:lang(iw) .dropdown { background-position: left 0.7em top 50%, 0px 0px; padding: 0.6em 0.8em 0.5em 1.4em; }
select, .dropdown { app-region: no-drag; height: var(--input-height); font-size: var(--font-ui-small); font-family: inherit; font-weight: var(--input-font-weight); color: var(--text-normal); line-height: var(--line-height-tight); padding: 0px 1.9em 0px 0.8em; max-width: 100%; box-sizing: border-box; margin: 0px; border: 0px; box-shadow: var(--input-shadow); border-radius: var(--input-radius); appearance: none; background-color: var(--interactive-normal); background-repeat: no-repeat, repeat; background-position: right 0.7em top 50%, 0px 0px; background-size: 0.65em, 100%; }
@media (hover: hover) {
  select:hover, .dropdown:hover { box-shadow: var(--input-shadow-hover); background-color: var(--interactive-hover); }
}
select:focus, .dropdown:focus { box-shadow: 0 0 0px 3px var(--background-modifier-border-focus); outline: none; }
.dropdown { background-image: url("data:image/svg+xml,%3Csvg xmlns=\"http://www.w3.org/2000/svg\" width=\"292.4\" height=\"292.4\"%3E%3Cpath fill=\"%23000\" opacity=\"0.4\" d=\"M287 69.4a17.6 17.6 0 0 0-13-5.4H18.4c-5 0-9.3 1.8-12.9 5.4A17.6 17.6 0 0 0 0 82.2c0 5 1.8 9.3 5.4 12.9l128 127.9c3.6 3.6 7.8 5.4 12.8 5.4s9.2-1.8 12.8-5.4L287 95c3.5-3.5 5.4-7.8 5.4-12.8 0-5-1.9-9.2-5.5-12.8z\"/%3E%3C/svg%3E"); }
.theme-dark .dropdown { background-image: url("data:image/svg+xml,%3Csvg xmlns=\"http://www.w3.org/2000/svg\" width=\"292.4\" height=\"292.4\"%3E%3Cpath fill=\"%23FFF\" opacity=\"0.4\" d=\"M287 69.4a17.6 17.6 0 0 0-13-5.4H18.4c-5 0-9.3 1.8-12.9 5.4A17.6 17.6 0 0 0 0 82.2c0 5 1.8 9.3 5.4 12.9l128 127.9c3.6 3.6 7.8 5.4 12.8 5.4s9.2-1.8 12.8-5.4L287 95c3.5-3.5 5.4-7.8 5.4-12.8 0-5-1.9-9.2-5.5-12.8z\"/%3E%3C/svg%3E"); }
.dropdown option { font-weight: normal; background-color: var(--background-primary); }
.flair { background-color: var(--interactive-normal); border-radius: var(--radius-s); color: var(--text-normal); font-size: 10px; letter-spacing: 0.05em; margin-left: var(--size-4-2); padding: var(--size-2-1) var(--size-2-2); position: relative; text-transform: uppercase; white-space: nowrap; vertical-align: middle; }
.flair.mod-flat { vertical-align: top; }
.flair.mod-pop { background-color: var(--interactive-accent); color: var(--text-on-accent); }
.markdown-preview-view:not(.allow-fold-lists) .list-collapse-indicator, .markdown-preview-view:not(.allow-fold-headings) .heading-collapse-indicator { display: none; }
h1:hover .collapse-indicator, h2:hover .collapse-indicator, h3:hover .collapse-indicator, h4:hover .collapse-indicator, h5:hover .collapse-indicator, h6:hover .collapse-indicator, .collapse-indicator:hover, .is-collapsed .collapse-indicator, .cm-fold-indicator.is-collapsed .collapse-indicator, .cm-gutterElement:hover .collapse-indicator, .cm-gutterElement .is-collapsed .collapse-indicator, .cm-line:hover .cm-fold-indicator .collapse-indicator, .fold-gutter.is-collapsed, .fold-gutter:hover { opacity: 1; }
.view-content .list-collapse-indicator svg.svg-icon, .view-content .collapse-indicator svg.svg-icon { color: var(--collapse-icon-color); }
.view-content .is-collapsed .list-collapse-indicator svg.svg-icon, .view-content .is-collapsed .collapse-indicator svg.svg-icon { color: var(--collapse-icon-color-collapsed); }
.collapse-icon { display: flex; align-items: center; }
.collapse-icon::before { content: "​"; }
.collapse-icon svg.svg-icon { color: var(--nav-collapse-icon-color); stroke-width: 4px; width: 10px; height: 10px; transition: transform 100ms ease-in-out 0s; }
.is-collapsed .collapse-icon svg.svg-icon { transform: rotate(-90deg); color: var(--nav-collapse-icon-color-collapsed); }
.rtl .is-collapsed .collapse-icon svg.svg-icon { transform: rotate(90deg); }
.markdown-preview-view .collapse-indicator { float: left; cursor: var(--cursor); }
.markdown-preview-view .collapse-indicator .svg-icon { vertical-align: middle; }
.markdown-preview-view .list-collapse-indicator { margin-left: -3em; padding: 0px 8px; }
.markdown-preview-view li.is-collapsed > ul, .markdown-preview-view li.is-collapsed > ol { display: none; }
.markdown-preview-view .heading-collapse-indicator { margin-left: -22px; padding: 0px 6px; }
.markdown-source-view.mod-cm6 .cm-fold-indicator .collapse-indicator { opacity: 0; }
.markdown-source-view.mod-cm6 .cm-line:hover .cm-fold-indicator .collapse-indicator, .markdown-source-view.mod-cm6 .cm-fold-indicator.is-collapsed .collapse-indicator { opacity: 1; }
.markdown-source-view.mod-cm6 .cm-foldPlaceholder { color: var(--text-faint); background-color: transparent; border: none; margin-left: 8px; }
.markdown-source-view.mod-cm6 .cm-fold-indicator { display: inline-block; position: relative; z-index: 1; }
.markdown-source-view.mod-cm6 .cm-fold-indicator .collapse-indicator { position: absolute; top: 0px; right: 0px; height: 100%; cursor: var(--cursor); padding-right: 5px; }
svg.svg-icon { height: var(--icon-size); width: var(--icon-size); stroke-width: var(--icon-stroke); }
.nav-buttons-container, .view-actions, .workspace-tab-header-inner, .side-dock-settings, .side-dock-actions { display: flex; justify-content: center; }
.side-dock-settings, .side-dock-actions { gap: var(--size-2-3); }
.view-actions { gap: 0px; align-items: center; --icon-size: var(--icon-s); }
.nav-buttons-container { flex-wrap: wrap; gap: var(--size-2-1); }
.nav-file-icon .svg-icon, .suggestion-flair .svg-icon, .menu-item-icon .svg-icon, .status-bar-item .svg-icon { --icon-size: var(--icon-s); --icon-stroke: var(--icon-s-stroke-width); }
.clickable-icon.side-dock-ribbon-action .svg-icon, .mod-left-split .workspace-tab-header-inner-icon .svg-icon, .mod-right-split .workspace-tab-header-inner-icon .svg-icon { --icon-size: var(--icon-l); --icon-stroke: var(--icon-l-stroke-width); }
.clickable-icon.side-dock-ribbon-action:active, .mod-left-split .workspace-tab-header-inner-icon:active, .mod-right-split .workspace-tab-header-inner-icon:active { color: var(--icon-color-focused); }
.clickable-icon { app-region: no-drag; background-color: transparent; display: flex; align-items: center; justify-content: center; padding: var(--size-2-2) var(--size-2-3); cursor: var(--cursor); border-radius: var(--clickable-icon-radius); color: var(--icon-color); opacity: var(--icon-opacity); transition: opacity 0.15s ease-in-out 0s; height: auto; }
@media (hover: hover) {
  .clickable-icon:hover { box-shadow: none; opacity: var(--icon-opacity-hover); color: var(--icon-color-hover); background-color: var(--background-modifier-hover); }
  .clickable-icon.has-active-menu, .clickable-icon:active { opacity: var(--icon-opacity-hover); color: var(--icon-color-focused); background-color: var(--background-modifier-hover); }
}
.clickable-icon.is-active { opacity: var(--icon-opacity-hover); color: var(--icon-color-active); background-color: var(--background-modifier-active-hover); }
@media (hover: hover) {
  .clickable-icon.is-active:hover { background-color: var(--background-modifier-active-hover); }
}
.clickable-icon[aria-disabled="true"] { background-color: unset; color: var(--text-muted); opacity: 0.4; }
@media (hover: hover) {
  .clickable-icon[aria-disabled="true"]:hover { background-color: unset; }
}
.clickable-icon.mod-warning { color: var(--text-error); }
.setting-item-control .clickable-icon { padding: var(--size-2-2); }
.markdown-rendered.show-indentation-guide li > ul, .markdown-rendered.show-indentation-guide li > ol { position: relative; }
.markdown-rendered.show-indentation-guide li > ul::before, .markdown-rendered.show-indentation-guide li > ol::before { content: "​"; position: absolute; display: block; left: -1em; top: 0px; bottom: 0px; border-right: var(--indentation-guide-width) solid var(--indentation-guide-color); }
.markdown-source-view.mod-cm6 .cm-indent { display: inline-block; }
.markdown-source-view.mod-cm6 .cm-indent::before { content: "​"; display: block; width: 1px; border-right: var(--indentation-guide-width) solid var(--indentation-guide-color); color: transparent; position: absolute; top: 0px; bottom: 0px; transform: translateX(0.15em); }
.markdown-source-view.mod-cm6 .cm-active-indent::before { border-color: var(--indentation-guide-color-active); }
.input-label { display: inline-block; width: 150px; text-align: right; margin-right: var(--size-4-2); }
.input-button { padding: 6px 14px; margin-left: 14px; color: var(--text-muted); font-size: var(--font-ui-medium); position: relative; top: -1px; }
@media (hover: hover) {
  .input-button:hover { color: var(--text-normal); }
}
textarea, input[type="text"], input[type="search"], input[type="email"], input[type="password"], input[type="number"] { app-region: no-drag; background: var(--background-modifier-form-field); border: var(--input-border-width) solid var(--background-modifier-border); color: var(--text-normal); font-family: inherit; padding: var(--size-4-1) var(--size-4-2); font-size: var(--font-ui-small); border-radius: var(--input-radius); outline: none; }
@media (hover: hover) {
  textarea:hover, input[type="text"]:hover, input[type="search"]:hover, input[type="email"]:hover, input[type="password"]:hover, input[type="number"]:hover { border-color: var(--background-modifier-border-hover); transition: box-shadow 0.15s ease-in-out 0s, border 0.15s ease-in-out 0s; }
}
textarea:active, input[type="text"]:active, input[type="search"]:active, input[type="email"]:active, input[type="password"]:active, input[type="number"]:active, textarea:focus, input[type="text"]:focus, input[type="search"]:focus, input[type="email"]:focus, input[type="password"]:focus, input[type="number"]:focus { border-color: var(--background-modifier-border-focus); transition: box-shadow 0.15s ease-in-out 0s, border 0.15s ease-in-out 0s; }
textarea:active, input[type="text"]:active, input[type="search"]:active, input[type="email"]:active, input[type="password"]:active, input[type="number"]:active, textarea:focus, input[type="text"]:focus, input[type="search"]:focus, input[type="email"]:focus, input[type="password"]:focus, input[type="number"]:focus, textarea:focus-visible, input[type="text"]:focus-visible, input[type="search"]:focus-visible, input[type="email"]:focus-visible, input[type="password"]:focus-visible, input[type="number"]:focus-visible { box-shadow: 0 0 0 2px var(--background-modifier-border-focus); }
textarea::placeholder, input[type="text"]::placeholder, input[type="search"]::placeholder, input[type="email"]::placeholder, input[type="password"]::placeholder, input[type="number"]::placeholder { color: var(--text-faint); }
input[type="text"], input[type="search"], input[type="email"], input[type="password"], input[type="number"] { height: var(--input-height); }
textarea { line-height: var(--line-height-tight); }
input[type="search"]::-webkit-search-decoration, input[type="search"]::-webkit-search-cancel-button { display: none; pointer-events: none; }
input[type="number"]::-webkit-inner-spin-button { appearance: none; }
input[type="range"] { width: 100px; appearance: none; background-color: var(--slider-track-background); border-radius: var(--slider-track-height); height: var(--slider-track-height); padding: 0px; }
body:not(.is-mobile) input[type="range"]:focus { box-shadow: none; }
input[type="range"]::-webkit-slider-runnable-track { height: 6px; appearance: none; }
input[type="range"]::-webkit-slider-thumb { appearance: none; height: var(--slider-thumb-height); width: var(--slider-thumb-width); border-radius: var(--slider-thumb-radius); cursor: default; background: rgb(255, 255, 255); border: var(--slider-thumb-border-width) solid var(--slider-thumb-border-color); position: relative; top: var(--slider-thumb-y); transition: all 0.1s linear 0s; box-shadow: rgba(0, 0, 0, 0.05) 0px 1px 1px 0px, rgba(0, 0, 0, 0.1) 0px 2px 2px 0px; }
input[type="range"]::-webkit-slider-thumb:hover, input[type="range"]::-webkit-slider-thumb:active { background: white; border-color: var(--background-modifier-border-focus); box-shadow: rgba(0, 0, 0, 0.1) 0px 1px 2px 0px, rgba(0, 0, 0, 0.2) 0px 2px 3px 0px; transition: all 0.1s linear 0s; }
input[type="range"] { outline: none; }
body:not(.is-mobile) input[type="range"]:focus::-webkit-slider-thumb { box-shadow: rgba(0, 0, 0, 0.05) 0px 1px 2px 0px, rgba(0, 0, 0, 0.2) 0px 2px 3px 0px; }
body:not(.is-mobile) input[type="range"]:focus-visible::-webkit-slider-thumb { border-color: var(--background-modifier-border-focus); box-shadow: 0 1px 2px 0px rgba(0, 0, 0, 0.05), 0 2px 3px 0px rgba(0, 0, 0, 0.2), 0 0 0px 2px var(--background-modifier-border-focus); }
input[type="color"] { appearance: none; width: calc(var(--swatch-width) + 4px); background-color: transparent; border: none; cursor: var(--cursor); padding: 0px; }
input[type="color"]::-webkit-color-swatch-wrapper { padding: 2px; }
input[type="color"]::-webkit-color-swatch { border: 0px; box-shadow: var(--swatch-shadow); border-radius: var(--swatch-radius); height: var(--swatch-height); width: var(--swatch-width); align-self: center; }
@media (hover: hover) {
  input[type="color"]::-webkit-color-swatch:hover { box-shadow: inset 0 0 0 1px rgba(var(--mono-rgb-100), 0.25), 0 0 0 3px var(--background-modifier-border-hover); }
}
input[type="color"]:focus-visible::-webkit-color-swatch, input[type="color"]:focus::-webkit-color-swatch { box-shadow: var(--swatch-shadow), 0 0 0 3px var(--background-modifier-border-focus); }
select.mod-hidden { display: none; }
.notice-container { z-index: var(--layer-notice); position: fixed; top: 22px; right: 0px; padding: 10px; overflow: hidden; }
.notice { background-color: var(--background-modifier-message); border-radius: var(--radius-m); box-shadow: 0 2px 8px var(--background-modifier-box-shadow); color: rgb(250, 250, 250); font-size: var(--font-ui-small); line-height: var(--line-height-tight); padding: 0.75em 1em; max-width: 300px; margin-bottom: 14px; white-space: pre-wrap; overflow-wrap: anywhere; word-break: break-word; cursor: var(--cursor); }
.menu { padding: var(--size-2-3); border: 1px solid var(--background-modifier-border-hover); background-color: var(--background-secondary); border-radius: var(--radius-m); box-shadow: var(--shadow-s); position: fixed; z-index: var(--layer-menu); user-select: none; max-height: calc(100% - var(--header-height)); overflow: hidden; }
.menu.mod-no-icon .menu-item-icon:first-child { display: none; }
.menu-separator { height: 0px; margin: var(--size-2-3) calc(var(--size-2-3) * -1); border-bottom: 1px solid var(--background-modifier-border); }
.menu-separator:last-child, .menu-separator:first-child { display: none; }
.menu-separator + .menu-separator { display: none; }
.menu-item { display: flex; align-items: center; gap: var(--size-4-2); padding: var(--size-4-1) var(--size-4-2); cursor: var(--cursor); font-size: var(--font-ui-small); border-radius: var(--radius-s); white-space: nowrap; }
.menu-item.is-disabled { cursor: default; color: var(--text-faint); }
.menu-item.is-warning.selected { color: var(--text-error); }
.menu-item.is-label { cursor: default; pointer-events: none; font-size: var(--font-ui-medium); color: var(--text-muted); white-space: pre-wrap; overflow-wrap: anywhere; word-break: break-word; }
@media (hover: hover) {
  .menu-item.is-warning:hover { color: var(--text-error); }
  .menu-item:hover:not(.is-disabled):not(.is-label) { background-color: var(--background-modifier-hover); }
}
.menu-item.selected:not(.is-disabled):not(.is-label) { background-color: var(--background-modifier-hover); }
.menu-item-icon { flex: 0 1 auto; display: flex; color: var(--text-muted); }
.menu-item.is-warning.selected .menu-item-icon, .menu-item.is-warning:hover .menu-item-icon { color: var(--text-error); }
.menu-item-icon .mod-submenu { color: var(--text-faint); }
.menu-item-title { flex: 1 0 0px; }
.menu.mod-tab-list .menu-item-title { max-width: 300px; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; vertical-align: bottom; }
.debug-textarea { width: 100%; height: 50vh; max-height: 80vh; font-family: var(--font-monospace); tab-size: 4; resize: none; }
.modal-container { display: flex; align-items: center; justify-content: center; position: absolute; top: 0px; left: 0px; width: 100%; height: 100%; z-index: var(--layer-modal); }
.modal-container.mod-dim .modal { box-shadow: var(--shadow-l); }
.modal-bg { position: absolute; top: 0px; left: 0px; width: 100%; height: 100%; background-color: var(--background-modifier-cover); }
.modal { --checkbox-size: var(--font-ui-medium); background-color: var(--modal-background); border-radius: var(--modal-radius); border: var(--modal-border-width) solid var(--modal-border-color); padding: var(--size-4-4); position: relative; min-height: 100px; width: var(--dialog-width); max-width: var(--dialog-max-width); max-height: var(--dialog-max-height); display: flex; flex-direction: column; overflow: auto; }
.modal.mod-sidebar-layout { padding: 0px; width: var(--modal-width); height: var(--modal-height); max-width: var(--modal-max-width); max-height: var(--modal-max-height); overflow: hidden; display: flex; flex-direction: column; }
.modal.mod-sidebar-layout .modal-content { display: flex; }
.modal-sidebar { background-color: var(--background-secondary); flex: 1 1 var(--modal-community-sidebar-width); min-width: var(--modal-community-sidebar-width); padding: var(--size-4-3) 0 0 0; display: flex; flex-direction: column; }
body:not(.native-scrollbars) .modal-close-button { right: 12px; }
.modal-close-button { cursor: var(--cursor); position: absolute; top: var(--size-2-3); right: var(--size-2-3); font-size: 24px; line-height: 20px; height: 24px; width: 24px; padding: 0 var(--size-2-2); border-radius: var(--radius-s); color: var(--text-muted); }
@media (hover: hover) {
  .modal-close-button:hover { background-color: var(--background-modifier-hover); color: var(--text-normal); }
}
.modal-close-button::before { font-family: Inter, sans-serif; content: "×"; font-weight: 300; }
.modal-title { font-size: 1.2em; margin-bottom: 0.75em; font-weight: var(--font-semibold); text-align: left; line-height: var(--line-height-tight); }
.mod-sidebar-layout .modal-title { display: none; }
.modal-title:empty { display: none; }
.modal-content { flex: 1 1 auto; font-size: var(--font-ui-medium); }
.modal-button-container { margin-top: 1.5em; display: flex; justify-content: flex-end; gap: var(--size-4-2); flex-wrap: wrap; font-size: var(--font-ui-medium); }
.modal-button-container .mod-checkbox { flex-grow: 1; display: flex; align-items: center; gap: var(--size-4-1); }
.modal-checkbox-label { cursor: var(--cursor); margin-left: 10px; user-select: none; }
.message-container { margin: var(--size-4-4) 0; }
.message { display: inline-block; padding: 6px 12px; border-radius: var(--radius-s); }
.message.mod-success { background-color: var(--background-modifier-success); color: var(--text-on-accent); }
.message.mod-success a { color: var(--text-normal); }
.message.mod-info { background-color: var(--background-modifier-info); }
.message.mod-error { background-color: var(--background-modifier-error); color: var(--text-on-accent); }
.message.mod-error a { color: var(--text-normal); }
.mod-warning { color: var(--text-error); }
.mod-success { color: var(--text-success); }
.mod-file-rename .rename-textarea { overflow: hidden; padding: var(--size-2-3) var(--size-4-2); resize: none; width: 100%; }
.modal-setting-back-button { position: absolute; top: var(--safe-area-inset-top); left: 0px; padding: var(--size-4-3) var(--size-4-3); height: var(--modal-header-height); color: var(--text-normal); font-weight: var(--font-semibold); }
.modal-setting-back-button-icon { display: flex; align-items: center; margin-right: 6px; }
.modal-setting-nav-bar { display: flex; flex: 0 1 auto; padding: var(--size-4-3); border-bottom: 1px solid var(--background-modifier-border); }
.popover { background-color: var(--background-primary); border: 1px solid var(--background-modifier-border); box-shadow: var(--shadow-s); border-radius: var(--radius-m); padding: var(--size-4-5); position: relative; max-height: 95vh; }
.popover-title { font-weight: var(--font-extrabold); }
.popover-content { margin: var(--size-4-2) 0; }
.components-container .popover { width: 300px; margin-top: var(--size-4-5); }
.components-container .popover .popover-content { font-size: var(--font-ui-medium); }
.popover.hover-popover { position: absolute; z-index: var(--layer-popover); max-width: 80vw; min-height: 100px; width: var(--popover-width); padding: 0px; overflow: hidden; }
.popover.hover-popover .markdown-preview-view { font-size: var(--popover-font-size); }
.popover.hover-popover > .mod-empty { display: flex; justify-content: center; align-items: center; padding: 20px; font-size: var(--popover-font-size); color: var(--text-muted); }
.popover.hover-popover > .media-embed { min-height: 0px; line-height: 0; border: none; }
.popover.hover-popover > .image-embed img { max-height: 100%; max-width: 100%; height: auto; }
.popover.hover-popover > .pdf-embed { width: var(--popover-pdf-width); height: var(--popover-pdf-height); max-height: var(--popover-max-height); }
.popover.hover-popover > .markdown-embed { height: var(--popover-height); max-height: var(--popover-max-height); border: 0px; padding: 0px; margin: 0px; }
.popover.hover-popover > .markdown-embed > .markdown-embed-content { height: 100%; overflow: auto; }
.popover.hover-popover > .markdown-embed > .markdown-embed-content > .markdown-preview-view { padding: var(--file-margins); }
.popover.hover-popover > .markdown-embed .mod-header + div > :first-child { margin-top: 0px; }
.follow-link-popover { box-shadow: 0 2px 8px var(--background-modifier-box-shadow); background-color: rgba(0, 0, 0, 0.9); border-radius: var(--radius-m); color: rgb(204, 204, 204); font-size: var(--font-ui-small); line-height: 20px; max-width: 300px; padding: 5px 12px; text-align: center; z-index: var(--layer-tooltip); white-space: pre-wrap; top: calc(100%); }
.follow-link-popover.mod-bottom { top: 0px; }
@media (hover: hover) {
  .follow-link-popover:hover { background-color: rgb(0, 0, 0); }
}
.follow-link-popover .popover-arrow { position: absolute; top: calc(100%); left: 50%; width: 0px; margin-left: -5px; border-width: 5px; border-style: solid; border-color: rgba(0, 0, 0, 0.9) transparent transparent; content: " "; font-size: 0px; line-height: 0; }
.follow-link-popover.mod-bottom .popover-arrow { border-bottom: 5px solid rgba(0, 0, 0, 0.9); border-top: none; top: -5px; }
.markdown-preview-view progress, .markdown-rendered progress, .markdown-source-view.is-live-preview progress { -webkit-writing-mode: horizontal-tb; writing-mode: horizontal-tb; appearance: none; box-sizing: border-box; display: inline-block; height: 6px; margin-bottom: 4px; max-width: 100%; overflow: hidden; border-radius: 0px; border: 0px; vertical-align: -0.2rem; }
.markdown-preview-view progress[value]::-webkit-progress-bar, .markdown-rendered progress[value]::-webkit-progress-bar, .markdown-source-view.is-live-preview progress[value]::-webkit-progress-bar { background-color: var(--background-secondary); box-shadow: inset 0px 0px 0px 1px var(--background-modifier-border); border-radius: 6px; overflow: hidden; }
.markdown-preview-view progress[value]::-webkit-progress-value, .markdown-rendered progress[value]::-webkit-progress-value, .markdown-source-view.is-live-preview progress[value]::-webkit-progress-value { background-color: var(--interactive-accent); overflow: hidden; }
.progress-bar { position: absolute; height: 100vh; width: 100vw; top: 0px; left: 0px; background-color: var(--background-primary); z-index: 10000; display: flex; flex-direction: column; justify-content: center; align-items: center; }
.progress-bar-message { margin-bottom: var(--size-4-8); opacity: 1; color: var(--text-muted); }
.progress-bar-indicator { position: relative; height: 8px; margin: 0px 10vw; width: 90vw; overflow-x: hidden; border-radius: 3px; }
.progress-bar-line { position: absolute; opacity: 0.4; background-color: var(--interactive-accent); width: 150%; height: 8px; }
.progress-bar-subline { position: absolute; background-color: var(--interactive-accent); height: 8px; }
.progress-bar-subline.mod-increase { animation: 2s ease 0s infinite normal none running increase; }
.progress-bar-subline.mod-decrease { animation: 2s ease 0.5s infinite normal none running decrease; }
.progress-bar .progress-bar-subline { transition: width 150ms ease-in-out 0s; }
@keyframes increase { 
  0% { left: -5%; width: 5%; }
  100% { left: 130%; width: 100%; }
}
@keyframes decrease { 
  0% { left: -80%; width: 80%; }
  100% { left: 110%; width: 10%; }
}
.prompt { display: flex; flex-direction: column; border-radius: var(--radius-l); background-color: var(--background-primary); box-shadow: var(--shadow-l); border: var(--prompt-border-width) solid var(--prompt-border-color); z-index: 1; position: absolute; top: 80px; width: var(--prompt-width); max-width: var(--prompt-max-width); max-height: var(--prompt-max-height); overflow: hidden; }
.prompt-input-container { display: flex; }
input.prompt-input { width: 100%; padding: var(--size-4-6); background-color: var(--background-primary); font-size: var(--font-ui-medium); border-top: none; border-right: none; border-left: none; border-image: initial; height: 40px; border-radius: 0px; border-bottom: 1px solid var(--background-secondary); }
input.prompt-input:hover, input.prompt-input:focus, input.prompt-input:focus-visible { border-bottom: 1px solid var(--background-secondary); box-shadow: none; }
.prompt-results { list-style: none; margin: 0px; padding: var(--size-4-3); overflow-y: auto; }
.prompt-instructions { border-top: 1px solid var(--background-secondary); user-select: none; font-size: var(--font-ui-smaller); color: var(--text-muted); padding: var(--size-4-2); text-align: center; display: flex; flex-wrap: wrap; justify-content: center; gap: var(--size-4-3); }
.prompt-instruction { display: inline-block; }
.prompt-instruction-command { font-weight: var(--bold-weight); margin-right: var(--size-2-2); }
body:not(.native-scrollbars) ::-webkit-scrollbar { width: 12px; height: 12px; border-radius: var(--radius-l); background-color: transparent; }
body:not(.native-scrollbars) ::-webkit-scrollbar-track { background-color: transparent; }
body:not(.native-scrollbars) ::-webkit-scrollbar-thumb { background-color: var(--scrollbar-thumb-bg); border-radius: var(--radius-l); background-clip: padding-box; border-style: solid; border-color: transparent; border-image: initial; border-width: 3px 3px 3px 2px; min-height: 45px; }
body:not(.native-scrollbars) ::-webkit-scrollbar-thumb:active { border-radius: var(--radius-l); }
body:not(.native-scrollbars) ::-webkit-scrollbar-thumb:hover, body:not(.native-scrollbars) ::-webkit-scrollbar-thumb:active { background-color: var(--scrollbar-active-thumb-bg); }
body:not(.native-scrollbars) ::-webkit-scrollbar-corner { background: transparent; }
body:not(.native-scrollbars) * { }
.suggestion-container { position: absolute; background-color: var(--background-primary); max-width: 500px; border-radius: var(--radius-m); border: 1px solid var(--background-modifier-border); box-shadow: var(--shadow-s); z-index: var(--layer-notice); }
.suggestion { max-height: 300px; overflow-y: auto; padding: var(--size-2-3); }
.suggestion-item, .suggestion-empty { font-size: var(--font-ui-medium); margin-bottom: 1px; }
.suggestion-empty { color: var(--text-muted); padding-right: ; padding-bottom: ; padding-left: ; padding-top: var(--size-4-3); text-align: center; }
.suggestion-item { cursor: var(--cursor); padding-top: ; padding-right: ; padding-bottom: ; padding-left: 12px; white-space: pre-wrap; border-radius: var(--radius-s); }
.suggestion-item.is-selected { background-color: var(--background-modifier-hover); }
.suggestion-item.mod-downranked { color: var(--text-muted); }
.suggestion-item.mod-complex { align-items: baseline; display: flex; justify-content: space-between; }
.suggestion-item.mod-complex .suggestion-title { overflow-wrap: break-word; }
.suggestion-item.mod-complex .suggestion-content { display: flex; flex-direction: column; overflow: hidden; text-overflow: ellipsis; margin-right: auto; }
.suggestion-item.mod-complex .suggestion-prefix::after { content: ": "; }
.suggestion-item.mod-complex .suggestion-highlight { font-weight: bold; }
.suggestion-item.mod-complex .suggestion-note { font-size: 0.8em; color: var(--text-muted); width: 100%; flex-basis: 100%; overflow-wrap: break-word; }
.suggestion-item.mod-complex .suggestion-aux { display: flex; align-items: center; align-self: center; flex-shrink: 0; }
.suggestion-item.mod-complex .suggestion-hotkey { font-size: var(--font-ui-smaller); font-family: var(--font-interface); padding: 2px 6px; }
.suggestion-item.mod-complex .suggestion-hotkey:not(:last-child) { margin-left: 10px; }
.suggestion-item.mod-complex .suggestion-flair { color: var(--text-muted); opacity: var(--icon-opacity); margin: 0px 4px 0px 12px; display: flex; align-items: center; }
.suggestion-item.mod-complex .suggestion-flair:not(:last-child) { margin-left: 6px; }
.suggestion-highlight { font-weight: bold; }
.suggestion-bg { position: fixed; top: 0px; left: 0px; width: 100%; height: 100%; background-color: var(--background-modifier-cover); z-index: var(--layer-popover); }
.horizontal-tab-header { display: flex; }
.horizontal-tab-nav-item, .vertical-tab-nav-item { padding: var(--size-4-1) var(--size-4-2); user-select: none; cursor: var(--cursor); font-size: calc(var(--font-ui-small) + 1px); border-radius: var(--radius-s); }
.horizontal-tab-nav-item.is-active, .vertical-tab-nav-item.is-active { background-color: var(--interactive-accent); color: var(--text-on-accent); }
@media (hover: hover) {
  .horizontal-tab-nav-item.is-active:hover, .vertical-tab-nav-item.is-active:hover { background-color: var(--interactive-accent); }
}
@media (hover: hover) {
  .horizontal-tab-nav-item:hover, .vertical-tab-nav-item:hover { background-color: var(--background-modifier-hover); }
}
.vertical-tab-nav-item { margin-bottom: var(--size-2-1); }
.vertical-tab-nav-item-chevron { display: none; }
.horizontal-tab-content, .vertical-tab-content { background-color: var(--background-primary); padding-left: var(--size-4-12); padding-right: var(--size-4-12); }
.vertical-tabs-container { display: flex; }
.vertical-tab-header { padding: var(--size-4-3); background-color: var(--background-secondary); }
.vertical-tab-header-group-items { display: flex; flex-direction: column; }
.vertical-tab-header-group-title { font-size: var(--font-ui-smaller); color: var(--text-faint); font-weight: var(--font-semibold); padding: var(--size-4-2); user-select: none; }
.vertical-tab-header-group { padding: var(--size-4-3) 0; }
.vertical-tab-content-container { overflow: hidden; flex-grow: 1; }
.vertical-tab-content { overflow-y: auto; height: 100%; padding-top: var(--size-4-8); padding-bottom: var(--size-4-16); }
.vertical-tab-content h2 { font-size: var(--font-ui-medium); font-weight: var(--font-semibold); }
.checkbox-container { app-region: no-drag; cursor: var(--cursor); background-color: var(--background-modifier-border-hover); border-radius: var(--toggle-radius); display: inline-block; flex-shrink: 0; height: calc(var(--toggle-thumb-height) + var(--toggle-border-width) * 2); position: relative; user-select: none; width: var(--toggle-width); box-shadow: rgba(0, 0, 0, 0.07) 0px 4px 10px inset, rgba(0, 0, 0, 0.21) 0px 0px 1px inset; transition: box-shadow 0.15s ease-in-out 0s, outline 0.15s ease-in-out 0s, border 0.15s ease-in-out 0s, opacity 0.15s ease-in-out 0s; outline: 0 solid var(--background-modifier-border-focus); }
.checkbox-container input[type="checkbox"] { position: absolute; opacity: 0; left: 0px; }
.checkbox-container:focus-within { outline: var(--toggle-border-width) solid var(--background-modifier-border-focus); }
@media (hover: hover) {
  .checkbox-container:hover { box-shadow: rgba(0, 0, 0, 0.14) 0px 6px 20px inset, rgba(0, 0, 0, 0.28) 0px 0px 1px inset; }
}
.checkbox-container.is-enabled { background-color: var(--interactive-accent); }
.checkbox-container.is-enabled::after { transform: translate3d(calc(var(--toggle-width) - var(--toggle-thumb-width) - var(--toggle-border-width)), 0, 0); }
.checkbox-container.is-enabled:active::after { left: -4px; }
.checkbox-container::before { content: ""; display: block; position: absolute; inset: 0px; opacity: 0; }
.checkbox-container::after { pointer-events: none; content: ""; display: block; position: absolute; background-color: var(--toggle-thumb-color); width: var(--toggle-thumb-width); height: var(--toggle-thumb-height); margin: var(--toggle-border-width) 0 0 0; border-radius: var(--toggle-thumb-radius); transition: transform 0.15s ease-in-out 0s, width 0.1s ease-in-out 0s, left 0.1s ease-in-out 0s; left: 0px; transform: translate3d(var(--toggle-border-width), 0, 0); box-shadow: rgba(0, 0, 0, 0.15) 0px 1px 2px; }
.checkbox-container:active::after { width: calc(var(--toggle-thumb-width) + var(--toggle-border-width)); }
.checkbox-container.mod-small { width: var(--toggle-s-width); height: calc(var(--toggle-s-thumb-height) + var(--toggle-s-border-width) * 2); }
.checkbox-container.mod-small:focus-within { outline: var(--toggle-s-border-width) solid var(--background-modifier-border-focus); }
.checkbox-container.mod-small::after { width: var(--toggle-s-thumb-width); height: var(--toggle-s-thumb-height); margin: var(--toggle-s-border-width) 0 0 0; transform: translate3d(var(--toggle-s-border-width), 0, 0); }
.checkbox-container.mod-small.is-enabled::after { transform: translate3d(calc(var(--toggle-s-width) - var(--toggle-s-thumb-width) - var(--toggle-s-border-width)), 0, 0); }
.checkbox-container.mod-small:active::after { width: calc(var(--toggle-s-thumb-width) + var(--toggle-s-border-width)); }
.tooltip { animation: 200ms ease-in-out 0s 1 normal forwards running pop-down; box-shadow: 0 2px 8px var(--background-modifier-box-shadow); background-color: var(--background-modifier-message); border-radius: var(--radius-s); color: rgb(250, 250, 250); font-size: var(--font-ui-smaller); font-weight: var(--font-medium); left: 50%; line-height: var(--line-height-tight); max-width: 300px; padding: 4px 8px; position: fixed; text-align: center; transform: translateX(-50%); z-index: var(--layer-tooltip); pointer-events: none; white-space: pre-wrap; word-break: normal; overflow-wrap: anywhere; }
.tooltip.mod-right { animation: 200ms ease-in-out 0s 1 normal forwards running pop-right; transform: translateY(-50%); }
.tooltip.mod-left { animation: 200ms ease-in-out 0s 1 normal forwards running pop-right; transform: translateY(-50%); }
.tooltip.mod-error { width: 200px; background-color: var(--background-modifier-error); color: var(--text-on-accent); }
.tooltip.mod-wide { max-width: 450px; width: 400px; }
.tooltip .tooltip-arrow { position: absolute; top: -5px; left: 50%; width: 0px; margin-left: -5px; border-bottom: 5px solid var(--background-modifier-message); border-right: 5px solid transparent; border-left: 5px solid transparent; content: " "; font-size: 0px; line-height: 0; }
.tooltip.mod-right .tooltip-arrow { top: calc(50% - 5px); left: -5px; border-right: 5px solid var(--background-modifier-message); border-top: 5px solid transparent; border-bottom: 5px solid transparent; }
.tooltip.mod-left .tooltip-arrow { top: calc(50% - 5px); left: calc(100% + 5px); border-left: 5px solid var(--background-modifier-message); border-top: 5px solid transparent; border-bottom: 5px solid transparent; }
.tooltip.mod-top .tooltip-arrow { top: calc(100%); border-top: 5px solid var(--background-modifier-message); border-bottom: 5px solid transparent; }
.tooltip.mod-error .tooltip-arrow { border-bottom-color: var(--background-modifier-error); }
.tooltip.mod-error.mod-right .tooltip-arrow { border-right-color: var(--background-modifier-error); border-bottom: 5px solid transparent; }
.tooltip.mod-error.mod-left .tooltip-arrow { border-left-color: var(--background-modifier-error); border-bottom: 5px solid transparent; }
[aria-label] .svg-icon { pointer-events: none; }
@keyframes pop-down { 
  0% { opacity: 0; transform: translateX(-50%) scale(1); }
  20% { opacity: 0.7; transform: translateX(-50%) scale(1.02); }
  40% { opacity: 1; transform: translateX(-50%) scale(1.05); }
  100% { opacity: 1; transform: translateX(-50%) scale(1); }
}
@keyframes pop-right { 
  0% { opacity: 0; transform: translateY(-50%) scale(1); }
  20% { opacity: 0.7; transform: translateY(-50%) scale(1.02); }
  40% { opacity: 1; transform: translateY(-50%) scale(1.05); }
  100% { opacity: 1; transform: translateY(-50%) scale(1); }
}
.tree-item-self { padding: var(--nav-item-padding); margin-bottom: 1px; display: flex; align-items: baseline; border-radius: var(--radius-s); font-size: var(--nav-item-size); font-weight: var(--nav-item-weight); color: var(--nav-item-color); }
.tree-item-self.mod-collapsible { padding: var(--nav-item-parent-padding); }
.tree-item-self.is-clickable { cursor: var(--cursor); }
@media (hover: hover) {
  .tree-item-self.is-clickable:hover { background-color: var(--nav-item-background-hover); color: var(--nav-item-color-hover); font-weight: var(--nav-item-weight-hover); }
}
.tree-item-self .tree-item-icon { display: flex; align-items: center; padding-inline-end: var(--size-2-3); opacity: var(--icon-opacity); color: var(--icon-color); flex: 0 0 auto; }
.tree-item-self .tree-item-icon .svg-icon:not(.right-triangle) { --icon-size: var(--icon-s); --icon-stroke: var(--icon-s-stroke-width); }
.tree-item-flair-outer { flex: 0 0 auto; margin-left: var(--size-4-1); display: flex; align-items: center; }
.tree-item-flair { font-size: var(--font-ui-smaller); color: var(--text-faint); line-height: 1; border-radius: var(--radius-s); }
.tree-item-self:hover .tree-item-flair { color: var(--text-muted); }
.tree-item-inner { flex: 1 1 auto; line-height: var(--line-height-tight); }
.tree-item-inner-subtext { color: var(--text-faint); font-size: 85%; }
.tree-item-children { padding-left: var(--nav-item-children-padding-left); margin-left: var(--nav-item-children-margin-left); margin-bottom: 1px; border-left: var(--nav-indentation-guide-width) solid var(--nav-indentation-guide-color); }
audio { outline: none; }
.markdown-rendered audio { max-width: 100%; outline: none; }
audio { width: 100%; height: 42px; }
audio::-webkit-media-controls-enclosure { border-radius: calc(var(--radius-m) - 1px); border: 1px solid var(--background-modifier-border); background-color: var(--background-primary-alt); }
audio::-webkit-media-controls-current-time-display, audio::-webkit-media-controls-time-remaining-display { font-family: var(--font-interface); }
iframe { border: 0px; }
kbd { color: var(--code-normal); font-family: var(--font-monospace); background-color: var(--code-background); border-radius: var(--radius-s); font-size: var(--code-size); padding: 0.1em 0.25em; }
.workspace-leaf-content[data-type="pdf"] .view-content { padding: 0px; overflow: hidden; }
.pdf-container { height: 100%; padding: 0px 10px; position: relative; }
.pdf-scroll-container { overflow-y: auto; height: 100%; }
.pdf-canvas { width: 100%; margin: 6px 0px; }
.pdf-controls { position: absolute; top: 30px; left: calc(50% - 50px); height: 30px; background-color: var(--background-secondary); opacity: 0; border-radius: 6px; box-shadow: inset 8px 0 8px -10px var(--background-modifier-box-shadow); transition: opacity 200ms ease-in-out 0s; text-align: center; font-size: var(--font-ui-medium); line-height: 30px; padding: 0px 30px; }
.pdf-controls.mod-visible { opacity: 0.75; }
@media (hover: hover) {
  .pdf-container:hover .pdf-controls { opacity: 0.75; }
  .pdf-container:hover .pdf-controls:hover { opacity: 0.9; }
}
.pdf-controls-pager { position: absolute; top: 3px; cursor: var(--cursor); }
.pdf-controls-pager.mod-previous { left: 8px; }
.pdf-controls-pager.mod-next { right: 8px; }
.markdown-rendered video { max-width: 100%; outline: none; }
.markdown-rendered blockquote { color: var(--blockquote-color); font-style: var(--blockquote-font-style); background-color: var(--blockquote-background-color); border-left: var(--blockquote-border-thickness) solid var(--blockquote-border-color); padding: 0 0 0 var(--size-4-6); margin-inline: 0px; }
.markdown-rendered blockquote > :first-child { margin-top: 0px; }
.markdown-rendered blockquote > :last-child { margin-bottom: 0px; }
.markdown-source-view.mod-cm6.is-live-preview .HyperMD-quote::before, .markdown-source-view.mod-cm6 .cm-blockquote-border::before { content: "​"; display: block; width: 1px; border-left: var(--blockquote-border-thickness) solid var(--blockquote-border-color); color: transparent; position: absolute; top: 0px; bottom: 0px; }
.markdown-source-view.mod-cm6.is-live-preview .HyperMD-quote { font-style: var(--blockquote-style); background-color: var(--blockquote-background-color); }
.markdown-source-view.mod-cm6.is-live-preview .HyperMD-quote::before { left: 0px; }
.markdown-source-view.mod-cm6 .cm-blockquote-border { display: inline-block; }
.callout { --callout-color: var(--callout-default); --callout-icon: lucide-pencil; }
.callout[data-callout="abstract"], .callout[data-callout="summary"], .callout[data-callout="tldr"] { --callout-color: var(--callout-summary); --callout-icon: lucide-clipboard-list; }
.callout[data-callout="info"] { --callout-color: var(--callout-info); --callout-icon: lucide-info; }
.callout[data-callout="todo"] { --callout-color: var(--callout-todo); --callout-icon: lucide-check-circle-2; }
.callout[data-callout="important"] { --callout-color: var(--callout-important); --callout-icon: lucide-flame; }
.callout[data-callout="tip"], .callout[data-callout="hint"] { --callout-color: var(--callout-tip); --callout-icon: lucide-flame; }
.callout[data-callout="success"], .callout[data-callout="check"], .callout[data-callout="done"] { --callout-color: var(--callout-success); --callout-icon: lucide-check; }
.callout[data-callout="question"], .callout[data-callout="help"], .callout[data-callout="faq"] { --callout-color: var(--callout-question); --callout-icon: help-circle; }
.callout[data-callout="warning"], .callout[data-callout="caution"], .callout[data-callout="attention"] { --callout-color: var(--callout-warning); --callout-icon: lucide-alert-triangle; }
.callout[data-callout="failure"], .callout[data-callout="fail"], .callout[data-callout="missing"] { --callout-color: var(--callout-fail); --callout-icon: lucide-x; }
.callout[data-callout="danger"], .callout[data-callout="error"] { --callout-color: var(--callout-error); --callout-icon: lucide-zap; }
.callout[data-callout="bug"] { --callout-color: var(--callout-bug); --callout-icon: lucide-bug; }
.callout[data-callout="example"] { --callout-color: var(--callout-example); --callout-icon: lucide-list; }
.callout[data-callout="quote"], .callout[data-callout="cite"] { --callout-color: var(--callout-quote); --callout-icon: quote-glyph; }
.callout { overflow: hidden; border-style: solid; border-color: rgba(var(--callout-color), var(--callout-border-opacity)); border-width: var(--callout-border-width); border-radius: var(--callout-radius); margin: 1em 0px; mix-blend-mode: var(--callout-blend-mode); background-color: rgba(var(--callout-color), 0.1); padding: var(--callout-padding); }
.callout.is-collapsible .callout-title { cursor: var(--cursor); }
.callout-title { padding: var(--callout-title-padding); display: flex; gap: var(--size-4-1); font-size: var(--callout-title-size); color: rgb(var(--callout-color)); line-height: var(--line-height-tight); }
.callout-content { overflow-x: auto; padding: var(--callout-content-padding); background-color: var(--callout-content-background); }
.callout-icon { flex: 0 0 auto; display: flex; margin-top: 0.15em; align-self: flex-start; }
.callout-icon .svg-icon { color: rgb(var(--callout-color)); }
.callout-title-inner { font-weight: var(--bold-weight); color: var(--callout-title-color); }
.callout-fold { display: flex; margin-top: 0.15em; align-self: flex-start; padding-right: var(--size-4-2); }
.callout-fold .svg-icon { transition: transform 100ms ease-in-out 0s; }
.callout.is-collapsed .callout-fold .svg-icon { transform: rotate(-90deg); }
.markdown-source-view.mod-cm6 .callout { margin: 0px; }
.markdown-rendered code { color: var(--code-normal); font-family: var(--font-monospace); background-color: var(--code-background); border-radius: var(--radius-s); font-size: var(--code-size); padding: 0.1em 0.25em; }
.markdown-rendered pre { position: relative; padding: var(--size-4-2) var(--size-4-4); min-height: 38px; background-color: var(--code-background); border-radius: var(--radius-s); white-space: var(--code-white-space); overflow-x: auto; }
.markdown-rendered pre code { border: none; padding: 0px; background-color: transparent; }
.markdown-rendered pre:not(:hover) > button.copy-code-button { display: none; }
.markdown-rendered button.copy-code-button { margin: 6px; padding: 6px 8px; height: auto; background-color: transparent; box-shadow: none; color: var(--text-muted); font-size: var(--font-ui-smaller); font-family: var(--font-interface); position: absolute; top: 0px; right: 0px; }
@media (hover: hover) {
  .markdown-rendered button.copy-code-button:hover { background-color: var(--background-modifier-hover); }
}
.markdown-source-view.mod-cm6 .cm-preview-code-block pre { margin: 0px; }
.markdown-source-view.mod-cm6 .code-block-flair { position: absolute; right: 6px; top: 6px; z-index: 1; display: inline-block; padding: var(--size-4-1) var(--size-4-2); border-radius: var(--radius-s); font-family: var(--font-interface); font-size: var(--font-ui-smaller); color: var(--text-muted); cursor: var(--cursor); }
@media (hover: hover) {
  .markdown-source-view.mod-cm6 .code-block-flair:hover { background-color: var(--background-modifier-hover); }
}
.markdown-source-view.mod-cm6 .cm-line.HyperMD-codeblock { padding-left: var(--size-4-4); color: var(--code-normal); }
code[class*="language-"], pre[class*="language-"] { color: var(--code-normal); background: none; overflow-wrap: break-word; white-space: pre-wrap; word-break: normal; font-family: var(--font-monospace); text-align: left; word-spacing: normal; line-height: var(--line-height-normal); hyphens: none; }
@media print {
  code[class*="language-"], pre[class*="language-"] { text-shadow: none; }
}
:not(pre) > code[class*="language-"], pre[class*="language-"] { background: var(--code-background); }
pre[class*="language-"] { overflow: hidden; }
code[class*="language-"] { display: block; padding: 1em; overflow: auto; }
:not(pre) > code[class*="language-"] { padding: 0.1em; border-radius: 0.3em; white-space: normal; }
.token.important, .token.bold { font-weight: bold; }
.token.italic { font-style: italic; }
.token.entity { cursor: help; }
.token.comment, .token.prolog, .token.doctype, .token.cdata { color: var(--code-comment); }
.token.namespace { opacity: 0.7; }
.token.tag, .token.constant, .token.symbol, .token.deleted { color: var(--code-tag); }
.token.punctuation { color: var(--code-punctuation); }
.token.boolean, .token.number { color: var(--code-value); }
.token.selector, .token.attr-name, .token.string, .token.char, .token.inserted { color: var(--code-string); }
.token.operator { color: var(--code-operator); }
.token.entity, .token.parameter, .token.property, .token.url, .language-css .token.string, .style .token.string, .token.variable { color: var(--code-property); }
.token.atrule, .token.attr-value, .token.builtin, .token.function, .token.class-name, .token.property-access { color: var(--code-function); }
.token.keyword { color: var(--code-keyword); }
.token.regex, .token.important { color: var(--code-important); }
.markdown-preview-view .markdown-embed .markdown-preview-view { --file-folding-offset: 0px; height: 100%; padding: 0px; }
.markdown-preview-view .markdown-embed .markdown-preview-view .markdown-preview-pusher h1, .markdown-preview-view .markdown-embed .markdown-preview-view .markdown-preview-pusher h2, .markdown-preview-view .markdown-embed .markdown-preview-view .markdown-preview-pusher h3, .markdown-preview-view .markdown-embed .markdown-preview-view .markdown-preview-pusher h4, .markdown-preview-view .markdown-embed .markdown-preview-view .markdown-preview-pusher h5, .markdown-preview-view .markdown-embed .markdown-preview-view .markdown-preview-pusher h6 { margin-top: 0px; }
.pdf-embed, .markdown-source-view .pdf-embed { width: 100%; height: 800px; }
.markdown-embed, .file-embed { position: relative; }
.markdown-embed-link, .file-embed-link { position: absolute; top: 4px; right: 4px; color: var(--icon-color); opacity: var(--icon-opacity); cursor: var(--cursor-link); padding: var(--size-2-2); border-radius: var(--radius-s); display: flex; align-items: center; --icon-size: var(--icon-s); --icon-stroke: var(--icon-s-stroke-width); }
@media (hover: hover) {
  .markdown-embed-link:hover, .file-embed-link:hover { color: var(--icon-color-hover); opacity: var(--icon-opacity-hover); background: var(--background-modifier-hover); }
}
.file-embed-title { display: flex; align-items: center; justify-content: center; gap: var(--size-4-2); }
.file-embed-icon { color: var(--text-muted); display: flex; }
.file-embed { display: flex; justify-content: center; border-radius: var(--radius-m); background-color: var(--background-primary-alt); }
.file-embed.mod-generic, .file-embed.mod-empty { cursor: var(--cursor-link); padding: var(--size-4-2); color: var(--text-muted); text-align: center; font-size: var(--font-smaller); }
@media (hover: hover) {
  .file-embed.mod-generic:hover, .file-embed.mod-empty:hover { color: var(--text-normal); background-color: var(--background-secondary); }
}
.markdown-embed-content { height: 100%; }
.embed-title { align-items: center; display: flex; gap: var(--size-4-1); font-size: var(--font-text-size); font-weight: var(--bold-weight); text-align: left; text-overflow: ellipsis; white-space: nowrap; padding: 0 0 var(--size-4-2) 0; }
.markdown-embed { font-style: var(--embed-font-style); background-color: var(--embed-background); border-top: var(--embed-border-top); border-right: var(--embed-border-right); border-bottom: var(--embed-border-bottom); border-left: var(--embed-border-left); margin: 0px; padding: var(--embed-padding); }
.markdown-embed .markdown-preview-view { padding: 0px; }
.internal-embed:not(.image-embed) { display: block; }
.internal-embed img:not([width]), .internal-embed audio, .internal-embed video { max-width: 100%; }
.inline-embed .markdown-embed-content { height: fit-content; max-height: var(--embed-max-height); overflow: auto; }
.inline-embed .markdown-embed-content p:first-child { margin-top: 0px; }
.inline-embed .markdown-source-view.mod-cm6 .cm-editor { min-height: unset; }
.embed-iframe { width: 100%; height: 100%; }
.markdown-source-view.mod-cm6 .internal-embed { white-space: normal; }
.markdown-source-view.mod-cm6 .cm-embed-block { position: relative; white-space: normal; overflow-wrap: normal; word-break: normal; }
@media (hover: hover) {
  .markdown-source-view.mod-cm6 .cm-embed-block:hover { box-shadow: var(--embed-block-shadow-hover); border-radius: var(--radius-s); overflow: hidden; cursor: text; }
  .markdown-source-view.mod-cm6 .cm-embed-block:hover .edit-block-button { opacity: 1; }
  .markdown-source-view.mod-cm6 .cm-embed-block:hover .edit-block-button:hover { background-color: var(--background-modifier-hover); }
}
.markdown-source-view.mod-cm6 .cm-embed-block pre { margin: 0px; }
.markdown-source-view.mod-inside-iframe > .cm-editor > .cm-scroller { flex-direction: column; padding: 0 var(--size-4-4); }
.markdown-source-view.mod-inside-iframe > .cm-editor > .cm-scroller::before, .markdown-source-view.mod-inside-iframe > .cm-editor > .cm-scroller::after { content: " "; display: block; min-height: min(calc(10vh - 3px), var(--size-4-4)); max-height: var(--size-4-4); flex: 1 1 0px; }
.markdown-source-view.mod-inside-iframe > .cm-editor > .cm-scroller > .cm-sizer { min-height: unset; flex: 1 0 0px; }
.footnote-link { text-decoration: none; }
.footnotes { font-size: var(--footnote-size); }
.footnote-ref { vertical-align: top; }
.footnote-backref { color: var(--text-faint); text-decoration: none; }
@media (hover: hover) {
  .footnote-backref:hover { color: var(--text-accent); text-decoration: none; }
}
@media (hover: hover) {
  .cm-s-obsidian .cm-line.HyperMD-footnote span.cm-hmd-footnote:hover { color: var(--text-accent); }
}
.markdown-preview-view:not(.show-frontmatter) .frontmatter-container { display: none; }
.markdown-rendered .frontmatter.mod-failed { position: relative; }
.markdown-rendered .frontmatter.mod-failed .mod-error { color: var(--text-error); font-size: var(--font-smaller); }
.markdown-rendered .frontmatter.mod-failed::after { content: ""; position: absolute; top: 0px; right: 0px; width: 100%; height: 100%; background-color: var(--background-modifier-error); opacity: 0.3; mix-blend-mode: var(--highlight-mix-blend-mode); }
.frontmatter-container { padding: var(--size-4-2) 0 var(--size-4-4); color: var(--text-muted); position: relative; }
.markdown-embed-content .frontmatter-container { display: none; }
.frontmatter-container.is-collapsed .frontmatter-section { display: none; }
.frontmatter-container .frontmatter-collapse-indicator { margin-right: 6px; align-self: center; display: none; }
.frontmatter-container .frontmatter-container-header { color: var(--text-normal); font-size: var(--font-smaller); user-select: none; cursor: var(--cursor); font-weight: var(--font-medium); display: flex; content: "Metadata"; border-bottom: 1px solid var(--background-modifier-border); padding-bottom: var(--size-4-2); margin-bottom: var(--size-4-2); }
.frontmatter-container.is-collapsed .frontmatter-container-header { color: var(--text-faint); }
@media (hover: hover) {
  .frontmatter-container.is-collapsed .frontmatter-container-header:hover { color: var(--text-muted); }
}
.frontmatter-container .frontmatter-section-label { padding-right: 0.5em; flex-basis: 4em; flex-shrink: 0; font-size: var(--font-smaller); text-transform: capitalize; }
.frontmatter-container .frontmatter-alias { font-size: var(--font-smaller); color: var(--text-normal); cursor: default; display: inline-flex; align-items: center; line-height: 1; white-space: nowrap; padding-right: 4px; }
.frontmatter-container .frontmatter-alias-icon { margin-right: var(--size-2-1); color: var(--text-accent); display: flex; align-items: center; }
.frontmatter-container .frontmatter-alias-icon .svg-icon { width: 12px; height: 12px; stroke-width: 2.5px; }
.frontmatter-container .frontmatter-section { display: flex; align-items: center; margin-bottom: var(--size-2-3); }
.frontmatter-container .frontmatter-section:last-child { margin-bottom: 0px; }
.frontmatter-container .frontmatter-section-data { display: inline-flex; flex-wrap: wrap; align-items: center; gap: var(--size-2-2); }
.markdown-rendered h1, .markdown-rendered h2, .markdown-rendered h3, .markdown-rendered h4, .markdown-rendered h5, .markdown-rendered h6 { margin: 15px 0px; }
.markdown-rendered li h1, .markdown-rendered li h2, .markdown-rendered li h3, .markdown-rendered li h4, .markdown-rendered li h5 { margin-top: 0px; margin-bottom: 0px; }
h1, .markdown-rendered h1 { font-variant: var(--h1-variant); letter-spacing: -0.015em; line-height: var(--h1-line-height); font-size: var(--h1-size); color: var(--h1-color); font-weight: var(--h1-weight); font-style: var(--h1-style); font-family: var(--h1-font); }
h1 a, .markdown-rendered h1 a { font-weight: inherit; }
h2, .markdown-rendered h2 { font-variant: var(--h2-variant); letter-spacing: -0.015em; line-height: var(--h2-line-height); font-size: var(--h2-size); color: var(--h2-color); font-weight: var(--h2-weight); font-style: var(--h2-style); font-family: var(--h2-font); }
h2 a, .markdown-rendered h2 a { font-weight: inherit; }
h3, .markdown-rendered h3 { font-variant: var(--h3-variant); letter-spacing: -0.015em; line-height: var(--h3-line-height); font-size: var(--h3-size); color: var(--h3-color); font-weight: var(--h3-weight); font-style: var(--h3-style); font-family: var(--h3-font); }
h3 a, .markdown-rendered h3 a { font-weight: inherit; }
h4, .markdown-rendered h4 { font-variant: var(--h4-variant); letter-spacing: 0.01em; line-height: var(--h4-line-height); font-size: var(--h4-size); color: var(--h4-color); font-weight: var(--h4-weight); font-style: var(--h4-style); font-family: var(--h4-font); }
h4 a, .markdown-rendered h4 a { font-weight: inherit; }
h5, .markdown-rendered h5 { font-variant: var(--h5-variant); letter-spacing: 0.015em; font-size: var(--h5-size); line-height: var(--h5-line-height); color: var(--h5-color); font-weight: var(--h5-weight); font-style: var(--h5-style); font-family: var(--h5-font); }
h5 a, .markdown-rendered h5 a { font-weight: inherit; }
h6, .markdown-rendered h6 { font-variant: var(--h6-variant); letter-spacing: 0.015em; font-size: var(--h6-size); line-height: var(--h6-line-height); color: var(--h6-color); font-weight: var(--h6-weight); font-style: var(--h6-style); font-family: var(--h6-font); }
h6 a, .markdown-rendered h6 a { font-weight: inherit; }
.HyperMD-header-1, .inline-title[data-level="1"], .HyperMD-list-line .cm-header-1 { font-variant: var(--h1-variant); letter-spacing: -0.015em; line-height: var(--h1-line-height); font-size: var(--h1-size); color: var(--h1-color); font-weight: var(--h1-weight); font-style: var(--h1-style); font-family: var(--h1-font); }
.HyperMD-header-1 a, .inline-title[data-level="1"] a, .HyperMD-list-line .cm-header-1 a { font-weight: inherit; }
.HyperMD-header-2, .inline-title[data-level="2"], .HyperMD-list-line .cm-header-2 { font-variant: var(--h2-variant); letter-spacing: -0.015em; line-height: var(--h2-line-height); font-size: var(--h2-size); color: var(--h2-color); font-weight: var(--h2-weight); font-style: var(--h2-style); font-family: var(--h2-font); }
.HyperMD-header-2 a, .inline-title[data-level="2"] a, .HyperMD-list-line .cm-header-2 a { font-weight: inherit; }
.HyperMD-header-3, .inline-title[data-level="3"], .HyperMD-list-line .cm-header-3 { font-variant: var(--h3-variant); letter-spacing: -0.015em; line-height: var(--h3-line-height); font-size: var(--h3-size); color: var(--h3-color); font-weight: var(--h3-weight); font-style: var(--h3-style); font-family: var(--h3-font); }
.HyperMD-header-3 a, .inline-title[data-level="3"] a, .HyperMD-list-line .cm-header-3 a { font-weight: inherit; }
.HyperMD-header-4, .inline-title[data-level="4"], .HyperMD-list-line .cm-header-4 { font-variant: var(--h4-variant); letter-spacing: 0.015em; line-height: var(--h4-line-height); font-size: var(--h4-size); color: var(--h4-color); font-weight: var(--h4-weight); font-style: var(--h4-style); font-family: var(--h4-font); }
.HyperMD-header-4 a, .inline-title[data-level="4"] a, .HyperMD-list-line .cm-header-4 a { font-weight: inherit; }
.HyperMD-header-5, .inline-title[data-level="5"], .HyperMD-list-line .cm-header-5 { font-variant: var(--h5-variant); letter-spacing: 0.015em; font-size: var(--h5-size); line-height: var(--h5-line-height); color: var(--h5-color); font-weight: var(--h5-weight); font-style: var(--h5-style); font-family: var(--h5-font); }
.HyperMD-header-5 a, .inline-title[data-level="5"] a, .HyperMD-list-line .cm-header-5 a { font-weight: inherit; }
.HyperMD-header-6, .inline-title[data-level="6"], .HyperMD-list-line .cm-header-6 { font-variant: var(--h6-variant); letter-spacing: 0.015em; font-size: var(--h6-size); line-height: var(--h6-line-height); color: var(--h6-color); font-weight: var(--h6-weight); font-style: var(--h6-style); font-family: var(--h6-font); }
.HyperMD-header-6 a, .inline-title[data-level="6"] a, .HyperMD-list-line .cm-header-6 a { font-weight: inherit; }
.HyperMD-header .cm-header-1, .HyperMD-header .cm-header-2, .HyperMD-header .cm-header-3, .HyperMD-header .cm-header-4, .HyperMD-header .cm-header-5, .HyperMD-header .cm-header-6 { font-size: inherit !important; }
hr { border-right-width: initial; border-bottom-width: initial; border-left-width: initial; border-right-style: none; border-bottom-style: none; border-left-style: none; border-image: initial; border-top-width: ; border-top-style: ; border-color: var(--hr-color); margin: 1.5em 0px; }
.markdown-rendered hr { border-right-width: initial; border-bottom-width: initial; border-left-width: initial; border-right-style: none; border-bottom-style: none; border-left-style: none; border-image: initial; border-top-width: ; border-top-style: ; border-color: var(--hr-color); }
.markdown-source-view.mod-cm6 .hr { display: flex; align-items: center; }
.markdown-source-view.mod-cm6 hr { margin: 0px; flex: 1 0 0px; }
@media (hover: hover) {
  .cm-s-obsidian .hmd-fold-html:hover { border: 1px dashed rgb(153, 153, 153); }
}
.markdown-preview-view img, .markdown-rendered img { image-rendering: -webkit-optimize-contrast; }
.markdown-preview-view img:not([width]), .markdown-rendered img:not([width]) { max-width: 100%; outline: none; }
.markdown-source-view.mod-cm6 .cm-line .internal-embed.image-embed { display: inline; }
.internal-query { margin: 0px; border-top: 1px solid var(--background-modifier-border); }
.internal-query .search-result-container { padding: var(--size-4-2); max-height: 800px; overflow: auto; border: 1px solid var(--background-modifier-border); background-color: var(--background-secondary); border-radius: var(--radius-m); }
.internal-query .internal-query-header { text-align: center; padding: var(--size-4-3) 0 var(--size-4-3) var(--size-4-1); color: var(--text-normal); display: flex; justify-content: flex-start; align-items: center; }
.internal-query .internal-query-header-icon { color: var(--text-faint); margin-right: var(--size-4-1); display: flex; }
.internal-query .internal-query-header-title { font-weight: var(--font-medium); }
.internal-query .internal-query-header-title::before, .internal-query .internal-query-header-title::after { content: "\""; }
ul ul, ol ul, ol ol ul, ol ul ul, ul ol ul, ul ul ul { list-style-type: disc; }
ol { list-style-type: var(--list-numbered-style); }
ol > li::marker, ul > li::marker { color: var(--list-marker-color); }
ol > li.is-collapsed::marker, ul > li.is-collapsed::marker { color: var(--list-marker-color-collapsed); }
.markdown-rendered ul, .markdown-rendered ol { padding-inline-start: var(--list-indent); }
.markdown-rendered ol > li, .markdown-rendered ul > li { padding-top: var(--list-spacing); padding-bottom: var(--list-spacing); }
.markdown-source-view.mod-cm6 .cm-content > .cm-line.HyperMD-list-line { margin-left: 0.5em; }
.markdown-source-view ol > li, .markdown-source-view ul > li, .markdown-preview-view ol > li, .markdown-preview-view ul > li, .mod-cm6 .HyperMD-list-line.cm-line { padding-top: var(--list-spacing); padding-bottom: var(--list-spacing); }
.markdown-rendered .list-collapse-indicator { margin-left: -3em; padding-right: 2em; }
.markdown-rendered .list-bullet { float: left; margin-left: -1em; }
.markdown-rendered .task-list-item > .list-bullet { display: none; }
.markdown-rendered ul.has-list-bullet { list-style-type: "​"; }
.markdown-rendered ul.has-list-bullet > li::marker { color: transparent; }
.markdown-rendered ul.has-list-bullet li p:first-of-type { margin-block-start: 0px; }
.markdown-rendered ul.has-list-bullet li p:last-of-type { margin-block-end: 0px; }
.list-bullet { color: transparent; position: relative; display: inline-flex; justify-content: center; align-items: center; }
.list-bullet::before { content: "​"; }
.list-bullet::after { position: absolute; content: "​"; pointer-events: none; color: var(--list-marker-color); border-radius: var(--list-bullet-radius); width: var(--list-bullet-size); height: var(--list-bullet-size); border: var(--list-bullet-border); transform: var(--list-bullet-transform); background-color: var(--list-marker-color); transition: transform 0.15s ease 0s, box-shadow 0.15s ease 0s; }
@media (hover: hover) {
  .list-collapse-indicator:hover ~ .list-bullet::after, .cm-fold-indicator:hover ~ .list-bullet::after, .list-collapse-indicator:hover ~ .cm-formatting-list .list-bullet::after, .cm-fold-indicator:hover ~ .cm-formatting-list .list-bullet::after { background-color: var(--list-marker-color-hover); box-shadow: 0 0 0 4px var(--background-modifier-hover); }
  li.is-collapsed .list-collapse-indicator:hover ~ .list-bullet::after, li.is-collapsed .cm-fold-indicator:hover ~ .list-bullet::after, .list-collapse-indicator:hover.is-collapsed ~ .list-bullet::after, .cm-fold-indicator:hover.is-collapsed ~ .list-bullet::after, li.is-collapsed .list-collapse-indicator:hover ~ .cm-formatting-list .list-bullet::after, li.is-collapsed .cm-fold-indicator:hover ~ .cm-formatting-list .list-bullet::after, .list-collapse-indicator:hover.is-collapsed ~ .cm-formatting-list .list-bullet::after, .cm-fold-indicator:hover.is-collapsed ~ .cm-formatting-list .list-bullet::after { background-color: var(--list-marker-color-collapsed); box-shadow: 0 0 0 4px var(--background-modifier-active-hover); }
}
li.is-collapsed .list-bullet::after, .is-collapsed ~ .cm-formatting-list .list-bullet::after { background-color: var(--list-marker-color-collapsed); box-shadow: 0 0 0 4px var(--background-modifier-active-hover); }
.markdown-source-view.mod-cm6 { }
.markdown-source-view.mod-cm6 .cm-fold-indicator .collapse-indicator { padding-right: 0.5rem; }
.markdown-source-view.mod-cm6 .cm-line:not(.cm-active):not(.HyperMD-header):not(.HyperMD-task-line) .cm-fold-indicator .collapse-indicator { padding-right: 1em; right: -0.5em; }
@media (hover: hover) {
  .list-collapse-indicator:hover ~ .list-bullet::after, .cm-fold-indicator:hover ~ .list-bullet::after, .list-collapse-indicator:hover ~ .cm-formatting-list .list-bullet::after, .cm-fold-indicator:hover ~ .cm-formatting-list .list-bullet::after { background-color: var(--list-marker-color-hover); box-shadow: 0 0 0 4px var(--background-modifier-hover); }
  li.is-collapsed .list-collapse-indicator:hover ~ .list-bullet::after, li.is-collapsed .cm-fold-indicator:hover ~ .list-bullet::after, .list-collapse-indicator:hover.is-collapsed ~ .list-bullet::after, .cm-fold-indicator:hover.is-collapsed ~ .list-bullet::after, li.is-collapsed .list-collapse-indicator:hover ~ .cm-formatting-list .list-bullet::after, li.is-collapsed .cm-fold-indicator:hover ~ .cm-formatting-list .list-bullet::after, .list-collapse-indicator:hover.is-collapsed ~ .cm-formatting-list .list-bullet::after, .cm-fold-indicator:hover.is-collapsed ~ .cm-formatting-list .list-bullet::after { background-color: var(--list-marker-color-collapsed); box-shadow: 0 0 0 4px var(--background-modifier-active-hover); }
}
.markdown-source-view.mod-cm6 .cm-hmd-list-indent { display: inline-block; }
.markdown-source-view.mod-cm6 .cm-formatting-list-ul, .markdown-source-view.mod-cm6 .cm-formatting-list-ol { white-space: pre; }
a { color: var(--link-color); outline: none; text-decoration-line: var(--link-decoration); text-decoration-thickness: var(--link-decoration-thickness); cursor: var(--cursor-link); }
@media (hover: hover) {
  a:hover { color: var(--link-color-hover); text-decoration-line: var(--link-decoration-hover); }
}
.external-link { color: var(--link-external-color); text-decoration-line: var(--link-external-decoration); background-position: right 4px; background-repeat: no-repeat; background-image: linear-gradient(transparent, transparent), url("https://publish.obsidian.md/public/images/874d8b8e340f75575caa.svg"); background-size: 13px; padding-right: 16px; cursor: var(--cursor-link); filter: var(--link-external-filter); }
@media (hover: hover) {
  .external-link:hover { color: var(--link-external-color-hover); text-decoration-line: var(--link-external-decoration-hover); }
}
.markdown-rendered .internal-link { cursor: var(--cursor-link); text-decoration-line: var(--link-decoration); }
@media (hover: hover) {
  .markdown-rendered .internal-link:hover { text-decoration-line: var(--link-decoration-hover); }
}
.markdown-rendered .internal-link.is-unresolved { color: var(--link-unresolved-color); opacity: var(--link-unresolved-opacity); filter: var(--link-unresolved-filter); text-decoration-style: var(--link-unresolved-decoration-style); text-decoration-color: var(--link-unresolved-decoration-color); }
@media (hover: hover) {
  .markdown-rendered .internal-link.is-unresolved:hover { opacity: 1; color: var(--link-color-hover); text-decoration-color: var(--link-color-hover); text-decoration-line: var(--link-decoration-hover); }
}
@media (hover: hover) {
  .cm-s-obsidian span.cm-link:hover { color: var(--link-external-color-hover); text-decoration-line: var(--link-external-decoration-hover); }
}
@media (hover: hover) {
  .cm-s-obsidian span.cm-formatting-link.cm-url:hover, .cm-s-obsidian span.cm-url:hover { color: var(--link-external-color-hover); text-decoration-line: var(--link-external-decoration-hover); }
}
@media (hover: hover) {
  .cm-s-obsidian span.hmd-link-icon:hover { opacity: 1; }
}
.markdown-source-view.mod-cm6 .is-unresolved { color: var(--link-unresolved-color); opacity: var(--link-unresolved-opacity); filter: var(--link-unresolved-filter); }
@media (hover: hover) {
  .markdown-source-view.mod-cm6 .is-unresolved:hover { opacity: 1; color: var(--link-color-hover); text-decoration-color: var(--link-color-hover); }
}
.markdown-source-view.mod-cm6 .is-unresolved .cm-underline { text-decoration-line: var(--link-decoration); text-decoration-style: var(--link-unresolved-decoration-style); text-decoration-color: var(--link-unresolved-decoration-color); }
.markdown-source-view.mod-cm6 .cm-underline { text-decoration-line: var(--link-decoration); text-decoration-thickness: var(--link-decoration-thickness); }
body.is-mobile .markdown-source-view.mod-cm6 .cm-underline { user-select: text; }
.markdown-source-view.mod-cm6.is-live-preview .cm-hashtag.cm-meta, .markdown-source-view.mod-cm6 .cm-hmd-internal-link .cm-underline, .markdown-source-view.mod-cm6 .cm-link .cm-underline, .markdown-source-view.mod-cm6 .cm-url .cm-underline { cursor: var(--cursor-link); }
@media (hover: hover) {
  .markdown-source-view.mod-cm6 .cm-hmd-internal-link .cm-underline:hover { text-decoration-line: var(--link-decoration-hover); }
}
.markdown-source-view.mod-cm6 .cm-link .cm-underline, .markdown-source-view.mod-cm6 .cm-url .cm-underline { text-decoration-line: var(--link-external-decoration); }
@media (hover: hover) {
  .markdown-source-view.mod-cm6 .cm-link .cm-underline:hover, .markdown-source-view.mod-cm6 .cm-url .cm-underline:hover { color: var(--link-external-color-hover); text-decoration-line: var(--link-external-decoration-hover); }
}
.inline-block { display: inline-block; vertical-align: middle; }
.hidden-token { display: inline; letter-spacing: -1ch; font-family: monospace; color: transparent; font-size: 1px !important; }
.mod-cm5 .cm-s-obsidian .HyperMD-table-row > :last-child { padding-right: 52px !important; }
@keyframes hmd-file-uploading-ani { 
  0%, 100% { opacity: 0.4; }
  50% { opacity: 0.7; }
}
@media (hover: hover) {
  .cm-s-obsidian div.HyperMD-goback-button:hover { color: transparent; text-align: left; }
  .cm-s-obsidian div.HyperMD-goback-button:hover::before { position: absolute; padding-left: 5px; content: "Back"; color: rgb(247, 247, 247); }
}
mjx-container { outline: none; }
.markdown-source-view.mod-cm6 .math-block > mjx-container { margin: 0px; padding: 1em 0px; overflow-x: auto; }
.markdown-rendered table { border-collapse: collapse; margin-block: 1em; }
.markdown-rendered td, .markdown-rendered th { padding: var(--size-2-2) var(--size-4-2); border: var(--table-border-width) solid var(--table-border-color); max-width: var(--table-column-max-width); }
.markdown-rendered td { font-size: var(--table-text-size); color: var(--table-text-color); }
.markdown-rendered th { font-size: var(--table-header-size); font-weight: var(--table-header-weight); color: var(--table-header-color); font-family: var(--table-header-font); text-align: left; line-height: var(--line-height-tight); }
.markdown-rendered th[align="center"] { text-align: center; }
.markdown-rendered th[align="right"] { text-align: right; }
.markdown-rendered thead > tr > th, .markdown-rendered tbody > tr > td { white-space: var(--table-white-space); text-overflow: ellipsis; overflow: hidden; }
.markdown-rendered tbody tr { background-color: var(--table-background); }
@media (hover: hover) {
  .markdown-rendered tbody tr:hover { background-color: var(--table-row-background-hover); }
}
.markdown-rendered tbody tr:nth-child(2n+1) { background-color: var(--table-row-alt-background); }
@media (hover: hover) {
  .markdown-rendered tbody tr:nth-child(2n+1):hover { background-color: var(--table-row-background-hover); }
}
.markdown-rendered tbody tr > td:nth-child(2n+2) { background-color: var(--table-column-alt-background); }
.markdown-rendered tbody tr:last-child > td { border-bottom-width: var(--table-row-last-border-width); }
.markdown-rendered tbody tr > td:first-child { border-left-width: var(--table-column-first-border-width); }
.markdown-rendered tbody tr > td:last-child { border-right-width: var(--table-column-last-border-width); }
.markdown-rendered thead tr { background-color: var(--table-header-background); }
@media (hover: hover) {
  .markdown-rendered thead tr:hover { background-color: var(--table-header-background-hover); }
}
.markdown-rendered thead tr > th { border-width: var(--table-header-border-width); border-color: var(--table-header-border-color); }
.markdown-rendered thead tr > th:nth-child(2n+2) { background-color: var(--table-column-alt-background); }
.markdown-rendered thead tr > th:first-child { border-left-width: var(--table-column-first-border-width); }
.markdown-rendered thead tr > th:last-child { border-right-width: var(--table-column-last-border-width); }
.markdown-source-view.mod-cm6 .cm-line.HyperMD-table-row { min-width: max-content; }
.markdown-source-view.mod-cm6 .cm-table-widget table { margin-bottom: 0px; }
a.tag { background-color: var(--tag-background); border: var(--tag-border-width) solid var(--tag-border-color); border-radius: var(--tag-radius); color: var(--tag-color); font-size: var(--tag-size); text-decoration: var(--tag-decoration); padding: var(--tag-padding-y) var(--tag-padding-x); line-height: 1; }
@media (hover: hover) {
  a.tag:hover { background-color: var(--tag-background-hover); border: var(--tag-border-width) solid var(--tag-border-color-hover); color: var(--tag-color-hover); text-decoration: var(--tag-decoration-hover); }
}
a.tag { background-color: var(--tag-background); border: var(--tag-border-width) solid var(--tag-border-color); border-radius: var(--tag-radius); color: var(--tag-color); font-size: var(--tag-size); text-decoration: var(--tag-decoration); padding: var(--tag-padding-y) var(--tag-padding-x); line-height: 1; }
@media (hover: hover) {
  a.tag:hover { background-color: var(--tag-background-hover); border: var(--tag-border-width) solid var(--tag-border-color-hover); color: var(--tag-color-hover); text-decoration: var(--tag-decoration-hover); }
}
input[type="checkbox"] { appearance: none; border-radius: var(--checkbox-radius); border: 1px solid var(--checkbox-border-color); flex-shrink: 0; padding: 0px; margin: 0px 6px 0px 0px; width: var(--checkbox-size); height: var(--checkbox-size); position: relative; transition: box-shadow 0.15s ease-in-out 0s; }
input[type="checkbox"]:hover, input[type="checkbox"]:active, input[type="checkbox"]:focus { outline: 0px; border-color: var(--checkbox-border-color-hover); }
input[type="checkbox"]:focus-visible { box-shadow: 0 0 0 2px var(--background-modifier-border-focus); }
input[type="checkbox"]:checked::after { content: ""; top: -1px; left: -1px; position: absolute; width: var(--checkbox-size); height: var(--checkbox-size); display: block; background-color: var(--checkbox-marker-color); -webkit-mask-position: 52% 52%; -webkit-mask-size: 65%; -webkit-mask-repeat: no-repeat; -webkit-mask-image: url("data:image/svg+xml; utf8, <svg width=\"12px\" height=\"10px\" viewBox=\"0 0 12 8\" version=\"1.1\" xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\"><g stroke=\"none\" stroke-width=\"1\" fill=\"none\" fill-rule=\"evenodd\"><g transform=\"translate(-4.000000, -6.000000)\" fill=\"%23000000\"><path d=\"M8.1043257,14.0367999 L4.52468714,10.5420499 C4.32525014,10.3497722 4.32525014,10.0368095 4.52468714,9.8424863 L5.24777413,9.1439454 C5.44721114,8.95166768 5.77142411,8.95166768 5.97086112,9.1439454 L8.46638057,11.5903727 L14.0291389,6.1442083 C14.2285759,5.95193057 14.5527889,5.95193057 14.7522259,6.1442083 L15.4753129,6.84377194 C15.6747499,7.03604967 15.6747499,7.35003511 15.4753129,7.54129009 L8.82741268,14.0367999 C8.62797568,14.2290777 8.3037627,14.2290777 8.1043257,14.0367999\"></path></g></g></svg>"); }
input[type="checkbox"]:checked { background-color: var(--checkbox-color); border-color: var(--checkbox-color); }
@media (hover: hover) {
  input[type="checkbox"]:checked:hover { background-color: var(--checkbox-color-hover); border-color: var(--checkbox-color-hover); }
}
.task-list-item-checkbox { width: var(--checkbox-size); height: var(--checkbox-size); }
.markdown-preview-view .task-list-item-checkbox { position: relative; top: 0.2em; margin-right: 0.6em; }
ul > li.task-list-item { list-style: none; }
ul > li.task-list-item .task-list-item-checkbox { margin-inline-start: calc(var(--checkbox-size) * -1.5); }
ul > li.task-list-item[data-task="x"], ul > li.task-list-item[data-task="X"] { text-decoration: var(--checklist-done-decoration); color: var(--checklist-done-color); }
.markdown-source-view.mod-cm6 .task-list-label { padding: 0px; margin-left: -0.25em; }
.markdown-source-view.mod-cm6 .task-list-item-checkbox { top: -0.1em; vertical-align: middle; margin-left: 2px; }
.markdown-source-view.mod-cm6 .HyperMD-task-line[data-task="x"], .markdown-source-view.mod-cm6 .HyperMD-task-line[data-task="X"] { text-decoration: var(--checklist-done-decoration); color: var(--checklist-done-color); }
b, strong { font-weight: var(--bold-weight); color: var(--bold-color); }
i, em { font-style: italic; color: var(--italic-color); }
.markdown-rendered mark { background-color: var(--text-highlight-bg); color: var(--text-normal); }
.markdown-rendered mark .internal-link { color: var(--text-normal); }
.embedded-backlinks { border-top: 1px solid var(--background-modifier-border); }
.markdown-preview-view .embedded-backlinks { margin-top: 3em; }
.embedded-backlinks .backlink-pane { padding: var(--size-4-3) 0 0 0; }
.embedded-backlinks .backlink-pane .search-empty-state, .embedded-backlinks .backlink-pane .tree-item-self { font-size: max(var(--font-ui-small),var(--font-smaller)); align-items: center; }
.embedded-backlinks .backlink-pane > .tree-item-self { font-size: max(var(--font-ui-small),1em); gap: var(--size-2-3); width: fit-content; }
.embedded-backlinks .backlink-pane .tree-item-flair { font-size: max(var(--font-ui-small),var(--font-smallest)); }
.embedded-backlinks .nav-header { padding: 0px; position: relative; }
.embedded-backlinks .nav-header ~ .search-input-container { width: calc(100% - 150px); margin: var(--size-4-3) 0 0 0; }
.embedded-backlinks .nav-buttons-container { position: absolute; right: 0px; top: 14px; z-index: 1; }
.nav-header { padding: var(--size-4-2); }
.nav-buttons-container.has-separator { border-bottom: 1px solid var(--background-modifier-border); padding-bottom: var(--size-2-3); margin-bottom: var(--size-4-2); }
.nav-files-container { flex-grow: 1; overflow: hidden auto; padding: 0 var(--size-4-3) var(--size-4-6) var(--size-4-3); scroll-padding-block: var(--size-4-2); }
.nav-folder.mod-root > .nav-folder-title { font-size: var(--vault-name-font-size); color: var(--vault-name-color); font-weight: var(--vault-name-font-weight); cursor: default; }
@media (hover: hover) {
  .nav-folder.mod-root > .nav-folder-title:hover { background-color: inherit; font-weight: var(--vault-name-font-weight); }
}
.nav-folder.mod-root > .nav-folder-title.is-being-dragged-over { background-color: hsla(var(--interactive-accent-hsl), 0.2); }
.nav-folder.mod-root > .nav-folder-title .nav-folder-collapse-indicator { display: none; }
.nav-folder.mod-root .nav-folder > .nav-folder-children { padding-left: var(--nav-item-children-padding-left); margin: 0 0 0 var(--nav-item-children-margin-left); border-left: var(--nav-indentation-guide-width) solid var(--nav-indentation-guide-color); }
.nav-file { border-radius: var(--radius-s); }
.nav-folder-title { padding: var(--nav-item-parent-padding); }
.nav-file-title { padding: var(--nav-item-padding); }
.nav-file-title, .nav-folder-title { margin-bottom: var(--size-2-1); display: flex; border-radius: var(--radius-s); cursor: var(--cursor); color: var(--nav-item-color); font-size: var(--nav-item-size); font-weight: var(--nav-item-weight); line-height: var(--line-height-tight); }
@media (hover: hover) {
  body:not(.is-grabbing) .nav-file-title:hover, body:not(.is-grabbing) .nav-folder-title:hover { background-color: var(--nav-item-background-hover); color: var(--nav-item-color-hover); font-weight: var(--nav-item-weight-hover); }
}
body:not(.is-grabbing) .nav-file-title.is-active:hover, body:not(.is-grabbing) .nav-folder-title.is-active:hover, .nav-file-title.is-active, .nav-folder-title.is-active { color: var(--nav-item-color-active); background-color: var(--nav-item-background-active); font-weight: var(--nav-item-weight-active); }
body:not(.is-grabbing) .nav-file-title.is-selected:hover, body:not(.is-grabbing) .nav-folder-title.is-selected:hover, .nav-file-title.is-selected, .nav-folder-title.is-selected { color: var(--nav-item-color-selected); background-color: var(--nav-item-background-selected); }
body:not(.is-grabbing) .nav-file-title.is-being-dragged, body:not(.is-grabbing) .nav-folder-title.is-being-dragged, .nav-file-title.is-being-dragged, .nav-folder-title.is-being-dragged { background-color: var(--interactive-accent); color: var(--text-on-accent); }
body:not(.is-grabbing) .nav-file-title.is-being-dragged .nav-folder-collapse-indicator, body:not(.is-grabbing) .nav-folder-title.is-being-dragged .nav-folder-collapse-indicator, .nav-file-title.is-being-dragged .nav-folder-collapse-indicator, .nav-folder-title.is-being-dragged .nav-folder-collapse-indicator { color: var(--text-on-accent); }
body:not(.is-grabbing) .nav-file-title.is-being-dragged .nav-file-tag, body:not(.is-grabbing) .nav-folder-title.is-being-dragged .nav-file-tag, .nav-file-title.is-being-dragged .nav-file-tag, .nav-folder-title.is-being-dragged .nav-file-tag { color: var(--text-normal); }
.workspace-leaf.mod-active .nav-folder.has-focus > .nav-folder-title, .workspace-leaf.mod-active .nav-file.has-focus > .nav-file-title { border-radius: var(--radius-s); box-shadow: 0 0 0 2px var(--background-modifier-border-focus); }
.workspace-leaf.mod-active .nav-folder.has-focus > .nav-folder-title:focus-within, .workspace-leaf.mod-active .nav-file.has-focus > .nav-file-title:focus-within { box-shadow: 0 0 0 2px var(--interactive-accent); }
.nav-folder-collapse-indicator { width: 16px; flex-shrink: 0; }
.nav-file-tag { background-color: var(--background-modifier-hover); border-radius: var(--radius-s); font-size: 9px; font-weight: var(--font-semibold); letter-spacing: 0.05em; line-height: var(--line-height-normal); margin-left: var(--size-2-3); padding: 0 var(--size-4-1); text-transform: uppercase; align-self: center; }
.nav-file-icon { display: inline-flex; align-items: center; margin-right: var(--size-2-3); position: relative; color: var(--icon-color); opacity: var(--icon-opacity); }
.nav-files-container:not(.show-unsupported) .is-unsupported { display: none; }
.nav-file-title-content, .nav-folder-title-content { display: inline-block; overflow-wrap: anywhere; overflow: hidden; white-space: var(--nav-item-white-space); text-overflow: ellipsis; }
.nav-file-title-content.is-being-renamed, .nav-folder-title-content.is-being-renamed { flex-grow: 1; white-space: normal; cursor: text; }
.nav-folder-title.is-being-dragged-over { border-radius: var(--radius-s); color: var(--nav-item-color-highlighted); background: hsla(var(--interactive-accent-hsl), 0.1); }
.nav-folder-title.is-being-dragged-over .collapse-icon { color: var(--nav-item-color-highlighted); }
.item-list { flex-grow: 1; padding: 0 var(--size-4-3) var(--size-4-6) var(--size-4-3); overflow-y: auto; }
.drop-indicator { position: absolute; left: 0px; width: 100%; height: 0px; border: 2px solid var(--interactive-accent); pointer-events: none; }
.drop-indicator:not(.is-active) { display: none; }
.file-tree-item-checkbox, .file-tree-item-icon { flex-shrink: 0; }
.file-tree-item-title { flex-grow: 1; word-break: break-word; }
.file-tree-item-icon { --icon-size: var(--icon-s); --icon-stroke: var(--icon-s-stroke-width); margin-right: var(--size-4-1); color: var(--icon-color); position: relative; top: var(--size-2-1); }
.file-tree .tree-item-inner { display: flex; align-items: center; position: relative; }
.file-tree .tree-item-flair { line-height: 1; padding: var(--size-2-1) var(--size-2-3); color: var(--text-on-accent); }
.file-tree .is-selected { color: var(--text-normal); }
.file-tree .mod-changed.is-selected { background-color: hsla(var(--interactive-accent-hsl), 0.2); }
.file-tree .mod-changed .tree-item-flair { color: var(--text-accent-hover); }
.file-tree .mod-new.is-selected { background-color: rgba(var(--background-modifier-success-rgb), 0.2); }
.file-tree .mod-new .tree-item-flair { color: var(--text-success); }
.file-tree .mod-deleted.is-selected, .file-tree .mod-to-delete.is-selected { background-color: rgba(var(--background-modifier-error-rgb), 0.2); }
.file-tree .mod-deleted .tree-item-flair, .file-tree .mod-to-delete .tree-item-flair { color: var(--text-error); }
.file-tree .mod-to-delete .tree-item-flair { display: none; }
.file-tree .mod-to-delete.is-selected .tree-item-flair { display: block; }
.file-tree .clickable-icon { display: flex; --icon-size: var(--icon-s); --icon-stroke: var(--icon-s-stroke-width); }
.graph-view.color-fill { color: var(--graph-node); }
.graph-view.color-fill-focused { color: var(--graph-node-focused); }
.graph-view.color-fill-tag { color: var(--graph-node-tag); }
.graph-view.color-fill-attachment { color: var(--graph-node-attachment); }
.graph-view.color-fill-unresolved { color: var(--graph-node-unresolved); opacity: 0.5; }
.graph-view.color-fill-1 { color: var(--text-muted); }
.graph-view.color-fill-2 { color: var(--text-muted); }
.graph-view.color-fill-3 { color: var(--text-muted); }
.graph-view.color-fill-4 { color: var(--text-muted); }
.graph-view.color-fill-5 { color: var(--text-muted); }
.graph-view.color-fill-6 { color: var(--text-muted); }
.graph-view.color-arrow { color: var(--text-normal); opacity: 0.5; }
.graph-view.color-circle { color: var(--graph-node-focused); }
.graph-view.color-line { color: var(--graph-line); }
.graph-view.color-text { color: var(--graph-text); }
.graph-view.color-fill-highlight { color: var(--interactive-accent); }
.graph-view.color-line-highlight { color: var(--interactive-accent); }
.graph-controls { border-radius: var(--radius-m); position: absolute; right: var(--size-4-3); top: var(--size-4-3); padding: 0px; background-color: var(--background-primary); width: var(--graph-controls-width); overflow: auto; }
.graph-controls:not(.is-close) { max-height: calc(100% - var(--size-4-4)); border: 1px solid var(--background-modifier-border); box-shadow: var(--shadow-s); }
.graph-controls.is-close { min-width: inherit; width: auto; background-color: var(--background-primary); border: 1px solid transparent; padding: var(--size-2-3); }
.graph-controls.is-close > .graph-control-section { display: none; }
.workspace-split:not(.mod-root) .graph-controls.is-close { background-color: var(--background-secondary); }
.graph-controls input[type="text"], .graph-controls input[type="range"] { width: 100%; font-size: var(--font-ui-small); }
.graph-controls .mod-cta { margin-top: var(--size-2-3); width: 100%; }
.graph-controls .setting-item { padding: var(--size-2-3) 0; border: none; }
.graph-controls .setting-item .setting-item-info { display: flex; align-items: center; }
.graph-controls .setting-item:first-of-type { border-top: none; }
.graph-controls .setting-item.mod-slider { flex-direction: column; }
.graph-controls .setting-item.mod-slider > * { width: 100%; }
.graph-controls .setting-item.mod-slider .setting-item-info { margin-right: 0px; }
.graph-controls .setting-item.mod-slider .setting-item-control { padding-top: var(--size-4-3); }
.graph-controls .setting-item.mod-toggle .setting-item-control { padding-top: 0px; }
.graph-controls .setting-item.mod-search-setting .setting-item-info { margin-right: 0px; }
.graph-controls .setting-item-name { font-size: var(--font-ui-small); }
.graph-controls::-webkit-scrollbar, .graph-controls::-webkit-scrollbar-thumb { display: none; }
.graph-color-group { --swatch-height: 18px; --swatch-width: 18px; position: relative; display: flex; align-items: center; padding: 0px 0px 6px; transition: top 200ms ease-in-out 0s; }
.graph-color-group input[type="color"] { margin: 0px 2px 0px 6px; }
.graph-color-group .clickable-icon { padding: var(--size-2-2); }
.graph-color-button-container { text-align: center; margin-bottom: 10px; }
.graph-color-button-container button { margin: 0px; width: 100%; }
.graph-color-group.drag-ghost { position: fixed; display: flex; max-width: unset; border: none; box-shadow: none; background-color: var(--background-primary-alt); padding: 0px; transition: none 0s ease 0s; pointer-events: none; }
.graph-color-group.drag-ghost input[type="text"] { width: 100%; }
.graph-color-group.drag-ghost input[type="color"] { margin-left: 6px; }
.graph-control-section.mod-color-groups .tree-item-children.is-grabbing .graph-color-groups-container { padding-bottom: 40px; }
.graph-controls-button { display: none; z-index: 1; }
.graph-controls-button.mod-close, .graph-controls-button.mod-reset { position: absolute; top: var(--size-4-2); right: var(--size-4-2); padding: var(--size-2-2); }
.graph-controls:not(.is-close) .graph-controls-button.mod-close, .graph-controls:not(.is-close) .graph-controls-button.mod-reset { display: flex; }
.graph-controls-button.mod-reset { right: 36px; }
.graph-controls.is-close .graph-controls-button.mod-open { display: flex; }
.graph-controls-button.mod-animate { margin-top: var(--size-4-2); }
.graph-controls.is-close .graph-controls-button.mod-animate { display: flex; }
.setting-item.mod-search-setting .setting-item-info { display: none; }
.setting-item.mod-search-setting .setting-item-control .search-input-container { position: relative; flex-grow: 1; margin: 0px; }
.setting-item.mod-search-setting.is-loading .setting-item-control::before { background-color: var(--interactive-accent); animation: 1000ms ease-in-out 300ms infinite normal none running progress-bar; }
.graph-control-section-header { font-weight: var(--font-semibold); font-size: var(--font-ui-small); color: var(--text-normal); }
.graph-control-section { padding: var(--size-2-3) var(--size-4-3); border-bottom: 1px solid var(--background-modifier-border); }
.graph-control-section:last-child { border-bottom: none; }
.graph-control-section:last-child .tree-item-children { padding-bottom: var(--size-4-4); }
.graph-control-section > .tree-item-self { padding-left: var(--size-4-1); }
.graph-control-section .tree-item-children { margin: 0px; padding: var(--size-4-1) 0; border-left: none; }
.graph-control-section.mod-display .setting-item:not(.mod-slider):last-child .setting-item-info { display: none; }
.workspace-leaf-content[data-type="outline"] .view-content { padding: 0px; }
.outline { padding: var(--size-4-3) var(--size-4-3) var(--size-4-8); }
.modal.mod-publish { height: var(--modal-height); width: var(--modal-width); max-width: var(--modal-max-width-narrow); padding: var(--size-4-4) 0 0 0; position: relative; overflow: hidden; }
.modal.mod-publish .modal-title { padding: 0 var(--size-4-4); }
.modal.mod-publish .modal-content { overflow: auto; padding: 0 var(--size-4-4) var(--size-4-4); margin-bottom: calc(var(--input-height) + var(--size-4-8)); border-top: var(--border-width) solid var(--background-modifier-border); }
.modal.mod-publish .modal-button-container { margin: 0 0 0 calc(var(--size-4-4) * -1); padding: var(--size-4-4); gap: var(--size-4-2); position: absolute; bottom: 0px; background-color: var(--background-primary); border-top: var(--border-width) solid var(--background-modifier-border); width: 100%; }
.publish-section { margin-bottom: var(--size-4-1); }
.publish-change-list { padding: var(--size-4-2) 0 var(--size-4-2) 0; }
.site-list-site-id-setting { margin-top: var(--size-4-4); }
.publish-section-header-text, .publish-section-header-toggle-collapsed-button, .publish-section-header-action { cursor: var(--cursor); }
@media (hover: hover) {
  .publish-section-header-text:hover, .publish-section-header-toggle-collapsed-button:hover, .publish-section-header-action:hover { color: var(--text-accent-hover); }
}
.publish-section-header { border-bottom: 1px solid var(--background-modifier-border); font-size: var(--font-ui-small); line-height: 1.1; color: var(--text-muted); display: flex; padding: var(--size-4-2) 0; align-items: center; }
.publish-section-header-text { flex-grow: 1; font-size: var(--font-ui-medium); color: var(--text-normal); line-height: var(--line-height-tight); font-weight: var(--font-medium); }
.publish-changes-switch-site { margin-left: var(--size-4-2); display: flex; flex-direction: row; flex-grow: 1; font-size: var(--font-ui-small); position: relative; gap: var(--size-2-1); top: 2px; }
.publish-changes-switch-site .clickable-icon { --icon-size: var(--icon-s); --icon-stroke: var(--icon-s-stroke-width); padding: var(--size-2-2); }
.upload-progress-container { max-height: 60vh; overflow: auto; }
.upload-progress-container.is-finished { max-height: calc(60vh - 200px); }
.publish-changes-current-site-name { margin-left: var(--size-2-3); text-decoration: underline; }
.publish-changes-info { display: flex; align-items: center; margin-bottom: 20px; }
.publish-changes-info button { margin-right: 0px; margin-left: var(--size-4-2); }
.publish-changes-info .search-input-container { margin: 0px; width: 0px; flex: 1 0 auto; }
.publish-section-header-toggle-collapsed-button { margin-right: var(--size-4-1); color: var(--text-faint); width: 9px; height: 9px; }
.publish-section-header-action { color: var(--text-faint); margin-left: var(--size-4-3); }
.publish-upload-item-title { word-break: break-word; font-size: var(--nav-item-size); line-height: var(--line-height-tight); }
.publish-changes-buttons { text-align: right; padding-bottom: var(--size-4-4); }
.publish-upload-item { position: relative; padding: var(--size-4-1) var(--size-4-2); }
.publish-upload-item .flair { background-color: transparent; text-transform: unset; letter-spacing: normal; font-size: var(--font-ui-smaller); }
.publish-upload-item .list-item-part { --icon-size: var(--icon-s); --icon-stroke: var(--icon-s-stroke-width); display: flex; align-items: center; }
.publish-upload-item::before { content: " "; position: absolute; top: 0px; left: 0px; width: 0px; height: 100%; transition: width 150ms ease-in-out 0s; background-color: rgba(var(--background-modifier-success-rgb), 0.2); z-index: 0; border-radius: var(--radius-s); }
.publish-upload-item.mod-failed { color: var(--text-error); }
.publish-upload-item.mod-failed::before { background-color: rgba(var(--background-modifier-error-rgb), 0.2); }
.publish-upload-item.mod-completed { color: var(--text-success); }
.publish-upload-item.mod-completed > * { position: relative; }
.publish-upload-item.mod-completed::before { width: 100%; }
.site-list-container { border-top: 1px solid var(--background-modifier-border); margin-bottom: var(--size-4-4); }
.site-list-container .list-item:last-child { padding-top: var(--size-4-4); }
.site-list-item-name { flex-grow: 1; }
.slug-input { text-transform: lowercase; }
.passwords-container { margin-bottom: var(--size-4-4); }
.password-item { border-radius: var(--radius-s); padding: var(--size-4-2) var(--size-4-4); margin: var(--size-4-1) 0; }
@media (hover: hover) {
  .password-item:hover { background-color: var(--background-primary); }
}
.nav-header ~ .search-input-container { padding: 0px; width: calc(100% - var(--size-4-8)); margin: 4px auto; }
.search-input-container { margin: 0px; position: relative; }
.search-input-container::before { top: calc((var(--input-height) - var(--search-icon-size))/2); left: 8px; position: absolute; content: ""; height: var(--search-icon-size); width: var(--search-icon-size); display: block; background-color: var(--search-icon-color); -webkit-mask-image: url("data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='currentColor' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'><circle cx='11' cy='11' r='8'></circle><line x1='21' y1='21' x2='16.65' y2='16.65'></line></svg>"); -webkit-mask-repeat: no-repeat; }
.search-input-container input { display: block; width: 100%; padding-right: 28px; padding-left: 36px; }
.search-input-clear-button { position: absolute; background: transparent; border-radius: 50%; color: var(--search-clear-button-color); cursor: var(--cursor); top: 0px; right: 2px; bottom: 0px; line-height: 0; height: var(--input-height); width: 28px; margin: auto; padding: 0px; text-align: center; display: flex; justify-content: center; align-items: center; transition: color 0.15s ease-in-out 0s; }
.search-input-clear-button::after { content: ""; height: var(--search-clear-button-size); width: var(--search-clear-button-size); display: block; background-color: currentcolor; -webkit-mask-image: url("data:image/svg+xml,<svg viewBox='0 0 12 12' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath fill-rule='evenodd' clip-rule='evenodd' d='M6 12C9.31371 12 12 9.31371 12 6C12 2.68629 9.31371 0 6 0C2.68629 0 0 2.68629 0 6C0 9.31371 2.68629 12 6 12ZM3.8705 3.09766L6.00003 5.22718L8.12955 3.09766L8.9024 3.8705L6.77287 6.00003L8.9024 8.12955L8.12955 8.9024L6.00003 6.77287L3.8705 8.9024L3.09766 8.12955L5.22718 6.00003L3.09766 3.8705L3.8705 3.09766Z' fill='currentColor'/></svg>"); -webkit-mask-repeat: no-repeat; }
.search-input-clear-button:hover, .search-input-clear-button:active { color: var(--text-normal); transition: color 0.15s ease-in-out 0s; }
.search-input-suggest-button { position: absolute; left: 0px; top: 0px; color: var(--text-faint); cursor: var(--cursor); padding: var(--size-4-1) var(--size-4-2); opacity: 0; z-index: 10; }
@media (hover: hover) {
  .search-input-suggest-button:hover { color: var(--text-muted); }
}
.backlink-pane, .outgoing-link-pane { overflow-y: auto; padding: var(--size-4-3) var(--size-4-3) var(--size-4-8); flex: 1 0 0px; }
.backlink-pane .search-result-container, .outgoing-link-pane .search-result-container { padding: var(--size-4-1) 1px var(--size-4-4); }
.backlink-pane > .tree-item-self, .outgoing-link-pane > .tree-item-self { color: var(--text-normal); }
.backlink-pane > .tree-item-self .tree-item-inner, .outgoing-link-pane > .tree-item-self .tree-item-inner { font-weight: var(--font-medium); }
.backlink-pane > .tree-item-self.is-collapsed, .outgoing-link-pane > .tree-item-self.is-collapsed { color: var(--text-faint); }
@media (hover: hover) {
  .backlink-pane > .tree-item-self.is-collapsed:hover, .outgoing-link-pane > .tree-item-self.is-collapsed:hover { color: var(--text-muted); }
}
.backlink-pane > .tree-item-self .collapse-icon, .outgoing-link-pane > .tree-item-self .collapse-icon { display: none; }
.search-result-container { padding: var(--size-4-3) var(--size-4-3) var(--size-4-4); position: relative; flex: 1 0 0px; }
.search-result-container.mod-global-search { overflow-y: auto; }
.search-result-container::before { content: " "; position: absolute; top: 0px; width: 0px; height: 3px; }
.search-result-container.is-loading::before { background-color: var(--interactive-accent); animation: 1000ms ease-in-out 300ms infinite normal none running progress-bar; }
.search-suggest-info-text { color: var(--text-muted); margin-left: 4px; }
.search-suggest-icon { padding: 4px; border-radius: var(--radius-s); }
@media (hover: hover) {
  .search-suggest-icon:hover { background-color: var(--background-modifier-hover); }
}
.suggestion-container.mod-search-suggestion { max-width: unset; background-color: var(--background-secondary); border-color: var(--prompt-border-color); }
.suggestion-container.mod-search-suggestion .suggestion { max-height: 600px; padding: var(--size-2-3); background-color: var(--background-secondary); border-radius: var(--radius-m); }
.search-suggest-icon { align-items: center; display: flex; }
.search-suggest-item { padding: var(--size-4-1) var(--size-4-2); border-radius: var(--radius-s); }
.search-suggest-item.suggestion-item { font-size: var(--font-ui-small); }
.search-suggest-item.mod-group { align-items: center; margin: 0px; color: var(--text-muted); padding: 0 0 0 var(--size-4-2); cursor: default; font-weight: var(--font-semibold); font-size: var(--font-ui-smaller); border-radius: 0px; }
.search-suggest-item.mod-group:not(:first-child) { border-top: 1px solid var(--background-modifier-border); margin-top: 6px; padding: 6px 6px 0px 14px; margin-left: -6px; margin-right: -6px; }
.search-suggest-item.mod-group:hover, .search-suggest-item.mod-group.is-selected { background-color: initial; }
@keyframes progress-bar { 
  0% { width: 0px; left: 0px; }
  5% { width: 0px; left: 0px; }
  50% { width: 100%; right: 0px; }
  95% { width: 0px; right: 0px; }
  100% { width: 0px; right: 0px; }
}
.search-empty-state { color: var(--text-faint); font-size: var(--font-ui-small); margin: 0 0 var(--size-4-3); padding-left: var(--size-4-2); }
.search-result { word-break: break-word; }
.search-result:not(.is-collapsed) .search-result-file-title { color: var(--nav-item-color-active); }
.search-result-file-matches { font-size: var(--font-ui-smaller); line-height: var(--line-height-tight); background-color: var(--search-result-background); border-radius: var(--radius-s); overflow: hidden; margin: var(--size-4-1) 0 var(--size-4-2); color: var(--text-muted); box-shadow: 0 0 0 1px var(--background-modifier-border); }
.search-info-more-matches { color: var(--text-faint); }
.search-result-file-match { cursor: var(--cursor); position: relative; padding: var(--size-4-2) var(--size-4-5) var(--size-4-2) var(--size-4-3); white-space: pre-wrap; width: 100%; border-bottom: 1px solid var(--background-modifier-border); }
.search-result-file-match:last-child { border-bottom: none; }
@media (hover: hover) {
  .search-result-file-match:hover { color: var(--text-normal); background-color: var(--text-selection); }
}
.search-result-file-match:hover .search-result-file-match-replace-button { display: block; }
.search-result-file-match-replace-button { display: none; position: absolute; height: auto; bottom: 5px; right: 24px; padding: var(--size-4-1) var(--size-4-2); color: var(--text-muted); font-size: var(--font-ui-smaller); }
@media (hover: hover) {
  .search-result-file-match-replace-button:hover { color: var(--text-normal); }
}
.search-result-hover-button { position: absolute; display: flex; right: 2px; border-radius: var(--radius-s); color: var(--text-faint); padding: 1px 3px; }
@media (hover: hover) {
  .search-result-hover-button:hover { opacity: 1; background-color: var(--background-modifier-hover); }
}
.search-result-hover-button.mod-top { top: 2px; }
.search-result-hover-button.mod-bottom { bottom: 2px; }
.search-result-file-matched-text { color: var(--text-normal); background-color: var(--text-highlight-bg); }
.search-info-container { color: var(--text-muted); padding: var(--size-4-1) var(--size-4-4) var(--size-4-1); font-size: var(--font-ui-smaller); }
.search-info-children { padding-left: 20px; border-left: 1px solid var(--background-modifier-border); margin: 1px 0px; }
.copy-search-result-container { display: flex; flex-direction: column; }
.copy-search-result-textarea { height: 300px; max-height: 20vh; resize: none; }
.copy-search-result-textarea + .setting-item { border-top: none; }
.search-result-file-match-destination-file-container { margin-top: var(--size-2-3); }
.search-result-file-match-destination-file { display: inline-flex; background-color: var(--interactive-normal); border-radius: var(--radius-s); box-shadow: var(--input-shadow); color: var(--text-muted); padding: var(--size-2-2) var(--size-2-3); margin-bottom: var(--size-2-1); }
@media (hover: hover) {
  .search-result-file-match:hover .search-result-file-match-destination-file { background-color: var(--background-secondary); }
  .search-result-file-match:hover .search-result-file-match-destination-file:hover { background-color: var(--interactive-hover); box-shadow: var(--input-shadow-hover); color: var(--text-normal); }
}
.search-result-file-match-destination-file-icon { --icon-size: var(--icon-xs); --icon-stroke: var(--icon-xs-stroke-width); margin-right: var(--size-4-1); display: flex; color: var(--text-faint); }
.search-result-file-match-destination-file-icon .svg-icon { align-self: center; }
.search-result-file-match-destination-file-name { white-space: pre-wrap; word-break: break-all; }
.workspace-leaf.mod-active .search-result.has-focus .tree-item-self, .workspace-leaf.mod-active .search-result-file-match.has-focus { border-radius: var(--radius-s); box-shadow: inset 0 0 0 2px var(--background-modifier-border-focus); }
.slides-container { position: fixed; top: 0px; left: 0px; height: 100vh; width: 100vw; transition: -webkit-transform 0.8s ease 0s; background-color: rgb(25, 25, 25); z-index: var(--layer-slides); border: none; }
.slides-container li .collapse-indicator { display: none; }
.slides-close-btn { display: inline-block; position: absolute; top: var(--size-4-2); right: var(--size-4-2); color: var(--text-faint); cursor: var(--cursor); z-index: 1; }
@media (hover: hover) {
  .slides-close-btn:hover { color: var(--text-muted); }
}
.reveal input[type="checkbox"] { width: 24px; height: 24px; }
.reveal .task-list-item, .reveal .footnote-item { list-style: none; }
.reveal .task-list-item { margin-left: -1.5em; }
.vault-list-item { margin: 6px 0px; display: flex; }
.vault-list-item.is-connected .vault-list-item-title { color: var(--text-normal); }
.vault-list-item-icon { color: var(--text-muted); position: relative; top: 1px; }
.vault-list-item-title { color: var(--text-muted); user-select: none; }
.vault-list-item-creation-time { color: var(--text-faint); font-size: var(--font-ui-small); }
.sync-status-icon { display: flex; align-items: center; cursor: var(--cursor); }
.sync-status-icon.mod-success { color: var(--text-success); }
.sync-status-icon.mod-working { color: var(--interactive-accent); }
.sync-status-icon.mod-error { color: var(--text-error); }
.sync-history-list-container { display: flex; flex-direction: column; flex-basis: 250px; flex-shrink: 0; border-right: 1px solid var(--background-modifier-border); }
.sync-history-list { overflow: auto; padding: var(--size-4-3); flex-grow: 1; display: flex; flex-direction: column; }
.sync-history-list .search-input-container { width: 100%; }
.sync-history-list-item-container { overflow: auto; flex: 1 1 0px; }
.sync-history-list-item { padding: var(--size-4-2) var(--size-4-3); margin-bottom: var(--size-4-2); cursor: var(--cursor); font-size: var(--font-ui-small); border-radius: var(--radius-s); transition: background-color 200ms ease-in-out 0s, color 200ms ease-in-out 0s; }
.sync-history-list-item:last-child { margin-bottom: 0px; }
.sync-history-list-item.is-active, .sync-history-list-item.is-active:hover { background-color: var(--interactive-accent); color: var(--text-on-accent); }
.sync-history-list-item.is-active .u-muted, .sync-history-list-item.is-active:hover .u-muted { color: var(--text-on-accent); opacity: 0.8; }
@media (hover: hover) {
  .sync-history-list-item:hover { background-color: var(--background-modifier-hover); }
}
.sync-history-content-container { background-color: var(--background-primary); padding: 0px; height: auto; display: flex; flex-direction: column; width: 0px; flex: 1 1 auto; }
.sync-history-content-container .modal-button-container { border-top: 1px solid var(--background-modifier-border); margin: 0px; padding: 12px; justify-content: center; }
.sync-history-content-container textarea { resize: none; border: none; box-shadow: none; }
.sync-history-content-container textarea:hover, .sync-history-content-container textarea:active, .sync-history-content-container textarea:focus { border: none; box-shadow: none; }
.sync-history-content-empty { display: none; }
.sync-history-content-container.mod-empty .sync-history-content-empty { display: block; text-align: center; padding: 24px; }
.sync-history-content { display: flex; flex-direction: column; flex-grow: 1; overflow: hidden; padding: 0px; }
.sync-history-content .setting-item:first-child { padding: var(--size-4-4) var(--size-4-6) var(--size-4-4); border-bottom: 1px solid var(--background-modifier-border); }
.sync-history-content .setting-item-info { flex-grow: 0; font-weight: var(--bold-weight); }
.sync-history-content .setting-item-control { justify-content: flex-start; }
.sync-history-text, .sync-history-diff { flex: 1 0 auto; padding: var(--size-4-6); }
.sync-history-content-other { flex-grow: 1; padding: var(--size-4-6); text-align: center; }
.sync-history-content-other img { max-width: 100%; }
.sync-history-content-container.mod-empty .sync-history-content, .sync-history-content-container.mod-empty .sync-history-content-buttons { display: none; }
.sync-history-content-buttons { border-top: 1px solid var(--background-modifier-border); margin: 0px; padding: var(--size-4-3); }
.mod-selectable { cursor: var(--cursor); padding: var(--size-4-2) var(--size-4-4); border-radius: var(--radius-m); }
@media (hover: hover) {
  .mod-selectable:hover { background-color: var(--background-modifier-hover); }
}
.sync-history-load-more-button { height: 38px; text-align: center; line-height: 38px; cursor: var(--cursor); color: var(--text-muted); }
@media (hover: hover) {
  .sync-history-load-more-button:hover { color: var(--text-normal); }
}
.modal.mod-sync-log { height: var(--modal-height); width: var(--modal-width); max-width: var(--modal-max-width-narrow); padding: var(--size-4-4) 0 0 0; }
.modal.mod-sync-log .modal-title { padding: 0 var(--size-4-4); }
.modal.mod-sync-log .modal-content { display: flex; flex-direction: column; overflow: hidden; }
.modal.mod-sync-log .modal-button-container { margin: 0px; padding: var(--size-4-4); }
.modal.mod-sync-log .setting-item.mod-toggle { padding: 0 var(--size-4-4) var(--size-4-4); }
.modal.mod-sync-log .sync-log-container { overflow: auto; flex-grow: 1; font-family: var(--font-monospace); font-size: var(--font-ui-smaller); color: var(--text-muted); border-top: 1px solid var(--background-modifier-border); border-bottom: 1px solid var(--background-modifier-border); padding: var(--size-4-4); background-color: var(--background-secondary); }
.modal.mod-sync-log .sync-log-container .list-item { line-height: var(--line-height-normal); margin: 0px; }
.modal.mod-sync-log .sync-log-container .list-item.mod-error { color: var(--text-error); }
.sync-file-tree-container { max-height: calc(90vh - 250px); overflow: auto; }
.sync-exclude-folder { display: flex; margin: var(--size-4-3) 0; }
.sync-exclude-folder > * { align-self: center; display: flex; }
.sync-exclude-folder-name { flex-grow: 1; }
.sync-exclude-folder-remove { visibility: hidden; margin-right: 6px; }
.sync-exclude-folder:hover .sync-exclude-folder-remove { visibility: visible; }
.tag-pane-tag.is-active { background-color: var(--interactive-accent); color: var(--text-on-accent); }
.tag-pane-tag.is-active .tag-pane-tag-count { background-color: var(--background-modifier-hover); color: var(--text-normal); }
@media (hover: hover) {
  .tag-pane-tag.is-active:hover { background-color: var(--interactive-accent); color: var(--text-on-accent); }
}
.tag-pane-tag-text, .tag-pane-tag-count { display: inline-block; }
.tag-pane-tag-text { word-break: break-word; flex-grow: 1; }
.tag-container { font-size: var(--font-ui-small); padding: var(--size-4-3) var(--size-4-3) var(--size-4-8); overflow: auto; }
.tree-item-children .tag-pane-tag .tag-pane-tag-parent { display: none; }
.workspace-leaf.mod-active .tree-item.has-focus > .tag-pane-tag { border-radius: var(--radius-s); box-shadow: 0 0 0 2px var(--background-modifier-border-focus); }
.mod-canvas-color-1 { --canvas-color: var(--canvas-color-1); }
.mod-canvas-color-2 { --canvas-color: var(--canvas-color-2); }
.mod-canvas-color-3 { --canvas-color: var(--canvas-color-3); }
.mod-canvas-color-4 { --canvas-color: var(--canvas-color-4); }
.mod-canvas-color-5 { --canvas-color: var(--canvas-color-5); }
.mod-canvas-color-6 { --canvas-color: var(--canvas-color-6); }
.workspace-leaf-content[data-type="canvas"] .view-content { padding: 0px; position: relative; }
body { --canvas-color: 192, 192, 192; }
body.theme-dark { --canvas-color: 126, 126, 126; }
.canvas-wrapper { position: absolute; width: 100%; height: 100%; left: 0px; top: 0px; --resizer-size: 20px; --shadow-stationary: 0px 0.5px 1px 0.5px rgba(0, 0, 0, 0.1); --shadow-drag: 0px 2px 10px rgba(0, 0, 0, 0.1); --shadow-border-accent: 0 0 0 2px var(--color-accent); --zoom-multiplier: 1; background-color: var(--canvas-background); overflow: hidden; contain: strict; touch-action: none; user-select: none; }
.canvas-wrapper.is-dragging { cursor: grabbing; }
.canvas-wrapper.is-dragging iframe:not(.is-controlled), .canvas-wrapper.is-dragging webview { pointer-events: none; }
.canvas-wrapper.is-screenshotting { z-index: 999999; }
.canvas-wrapper.is-screenshotting .canvas-card-menu, .canvas-wrapper.is-screenshotting .canvas-controls { display: none !important; }
.canvas-wrapper.is-screenshotting * { pointer-events: none !important; }
.canvas-mover { position: absolute; width: 100%; height: 100%; left: 0px; top: 0px; cursor: grab; }
.canvas-mover:active { cursor: grabbing; }
.canvas-background { position: absolute; width: 100%; height: 100%; left: 0px; top: 0px; pointer-events: none; }
.canvas-background circle { fill: var(--canvas-dot-pattern); }
.canvas { position: absolute; width: 100%; height: 100%; left: 0px; top: 0px; transform-origin: 0px 0px; pointer-events: none; }
.canvas > * { pointer-events: initial; }
.canvas-selection { pointer-events: none; position: absolute; background-color: hsla(var(--color-accent-hsl), 0.1); border: 2px solid var(--color-accent); z-index: -1; }
.canvas-selection.mod-group-selection { border-width: 3px; border-radius: 3px; background-color: hsla(var(--color-accent-hsl), 0.03); border-color: hsla(var(--color-accent-hsl), 0.3); pointer-events: initial; }
.canvas-wrapper:not(.mod-readonly) .canvas-selection.mod-group-selection { cursor: grab; }
.canvas-wrapper:not(.mod-readonly) .canvas-selection.mod-group-selection:active { cursor: grabbing; }
.canvas-selection.mod-node-highlight { border-radius: var(--radius-m); }
.canvas-controls, .canvas-card-menu { display: flex; position: absolute; z-index: var(--layer-cover); font-size: var(--font-ui-medium); }
.canvas-card-menu { background-color: var(--background-primary); border-radius: var(--radius-s); box-shadow: var(--input-shadow); bottom: var(--size-4-4); left: 50%; transform: translateX(-50%); align-items: stretch; }
.is-phone .canvas-card-menu, .mod-toolbar-open .canvas-card-menu { display: none; }
.theme-dark .canvas-card-menu { background-color: var(--background-secondary); }
.canvas-card-menu .canvas-card-menu-divider { width: 1px; background-color: var(--background-modifier-border); }
.canvas-card-menu .canvas-card-menu-button { color: var(--text-muted); height: auto; display: flex; line-height: 1; align-items: center; justify-content: center; padding: var(--size-4-2); --icon-size: var(--icon-xl); --icon-stroke: var(--icon-xl-stroke-width); }
@media (hover: hover) {
  .canvas-card-menu .canvas-card-menu-button:hover { color: var(--color-accent); }
}
.canvas-card-menu .canvas-card-menu-button svg { fill: var(--background-primary); }
.theme-dark .canvas-card-menu .canvas-card-menu-button svg { fill: var(--background-secondary); }
.canvas-card-menu .canvas-card-menu-button.mod-draggable { cursor: grab; }
.canvas-card-menu .canvas-card-menu-button.mod-draggable:active { cursor: grabbing; }
.canvas-card-menu .canvas-card-menu-button.mod-draggable svg { transition: transform 90ms ease-out 0s; }
@media (hover: hover) {
  .canvas-card-menu .canvas-card-menu-button.mod-draggable:hover svg { transform: translateY(-6px); filter: drop-shadow(rgba(0, 0, 0, 0.1) 0px 6px 2px); }
}
.canvas-controls { right: var(--size-4-2); top: var(--size-4-2); gap: var(--size-4-2); display: flex; flex-direction: column; }
.canvas-control-group { border-radius: var(--radius-s); background-color: var(--background-primary); border: 1px solid var(--background-modifier-border); box-shadow: var(--input-shadow); display: flex; flex-direction: column; overflow: hidden; }
.canvas-control-item { border-radius: 0px; box-shadow: none; height: auto; display: flex; line-height: 1; font-size: inherit; align-items: center; justify-content: center; cursor: var(--cursor); padding: var(--size-4-2); border-bottom: 1px solid var(--background-modifier-border); color: var(--text-muted); background-color: var(--interactive-normal); --icon-size: var(--icon-s); --icon-stroke: var(--icon-s-stroke-width); }
.canvas-control-item:last-child { border-bottom: none; }
@media (hover: hover) {
  .canvas-control-item:hover { color: var(--text-normal); background-color: var(--interactive-hover); }
}
.canvas-control-item.is-active { color: var(--color-accent); }
.canvas-control-item.is-disabled svg { color: var(--text-faint); }
.canvas-control-item svg { pointer-events: none; }
.canvas-node-container { background-color: var(--background-primary); border-radius: var(--radius-m); border: 2px solid rgb(var(--canvas-color)); contain: strict; display: flex; flex-direction: column; overflow: hidden; position: absolute; left: 0px; top: 0px; width: 100%; height: 100%; box-shadow: var(--shadow-stationary); }
.canvas-wrapper:not(.mod-readonly) .canvas-node:not(.is-editing) .canvas-node-container { cursor: grab; }
.canvas-wrapper:not(.mod-readonly) .canvas-node:not(.is-editing) .canvas-node-container:active { cursor: grabbing; }
.canvas-node-label { position: absolute; left: 0px; top: calc(-1 * var(--size-4-1) * var(--zoom-multiplier)); transform: translate(0, -100%) scale(var(--zoom-multiplier)); transform-origin: left bottom; max-width: calc(100% / var(--zoom-multiplier)); overflow: hidden; text-overflow: ellipsis; white-space: nowrap; color: var(--canvas-card-label-color); --icon-size: 1em; }
body:not(.is-ios) .canvas-wrapper.mod-animating .canvas-node-label { transition: transform 500ms cubic-bezier(0.16, 1, 0.3, 1) 0s; }
.canvas-node-label svg { position: relative; top: 2px; margin-right: var(--size-4-1); }
.canvas-node-label.mod-hover-label { opacity: 0; }
@media (hover: hover) {
  .canvas-node-label:hover { color: var(--text-muted); }
  .canvas-node:hover .canvas-node-label.mod-hover-label { opacity: 1; }
}
@media (hover: none) {
  .canvas-node.is-focused .canvas-node-label.mod-hover-label { opacity: 1; }
}
.canvas-wrapper.mod-zoomed-out .canvas-node-label { display: none; }
.canvas-node-placeholder { display: flex; align-items: center; justify-content: center; text-align: center; width: 100%; height: 100%; overflow: hidden; overflow-wrap: anywhere; padding: var(--size-4-6); font-size: 32px; font-weight: var(--font-semibold); }
.canvas-node-placeholder::after { border-radius: var(--radius-s); content: " "; display: block; position: absolute; top: var(--size-4-4); right: var(--size-4-4); bottom: var(--size-4-4); left: var(--size-4-4); background-color: rgba(var(--canvas-color), 0.1); }
.canvas-icon-placeholder { display: flex; width: 40%; height: 40%; }
.canvas-icon-placeholder svg { opacity: 0.3; color: rgb(var(--canvas-color)); width: 100%; height: 100%; }
.canvas-node-interaction-layer { position: absolute; width: 0px; height: 0px; pointer-events: none; }
.canvas-node-interaction-layer > * { pointer-events: initial; }
.canvas-node { --shadow-border-themed-inset: inset 0 0 0 1px rgb(var(--canvas-color)); --shadow-border-themed: 0 0 0 2px rgb(var(--canvas-color)); position: absolute; width: 0px; height: 0px; }
.canvas-node.is-dragging { pointer-events: none; }
.canvas-node.is-dragging .canvas-node-container { box-shadow: var(--shadow-drag); }
.canvas-node.is-selected, .canvas-node.is-focused { touch-action: initial; }
.canvas-node.is-selected .canvas-node-label, .canvas-node.is-focused .canvas-node-label { color: var(--text-muted); }
.canvas-node.is-selected .canvas-node-container, .canvas-node.is-focused .canvas-node-container { border-color: var(--color-accent); box-shadow: var(--shadow-stationary), var(--shadow-border-accent); }
.canvas-node.is-selected.is-dragging .canvas-node-container, .canvas-node.is-focused.is-dragging .canvas-node-container { box-shadow: var(--shadow-drag), var(--shadow-border-accent); }
.canvas-node.is-themed .canvas-node-container { border-color: rgba(var(--canvas-color), 0.7); box-shadow: inset 0 0 0 1px rgba(var(--canvas-color), 0.7), var(--shadow-stationary); }
.canvas-node.is-selected.is-themed .canvas-node-container, .canvas-node.is-focused.is-themed .canvas-node-container { border-color: rgb(var(--canvas-color)); box-shadow: var(--shadow-border-themed-inset), var(--shadow-border-themed); }
.canvas-node.is-selected.is-themed.is-dragging .canvas-node-container, .canvas-node.is-focused.is-themed.is-dragging .canvas-node-container { box-shadow: var(--shadow-border-themed-inset), var(--shadow-border-themed); }
.canvas-node.is-dummy { cursor: grabbing; }
.canvas-node.is-dummy .canvas-node-container { border: 4px solid var(--color-accent); box-shadow: rgba(0, 0, 0, 0.15) 0px 2px 10px; background-color: hsla(var(--color-accent-hsl), 0.2); }
.canvas-node.is-focused:not(.is-dragging) .canvas-node-content-blocker { display: none; }
.canvas-node-content-blocker { position: absolute; width: 100%; height: 100%; left: 0px; top: 0px; }
.canvas-node-group:not(.is-focused):not(.is-selected) { pointer-events: none; }
.canvas-node-group .canvas-node-resizer { pointer-events: initial; }
.canvas-node-group .canvas-node-container { background-color: transparent; }
.canvas-node-group .canvas-node-content { background-color: rgba(var(--canvas-color), 0.07); }
.canvas-group-label { position: absolute; left: 0px; top: calc(-1 * var(--size-4-1) * var(--zoom-multiplier)); transform: translate(0, -100%) scale(var(--zoom-multiplier)); transform-origin: left bottom; max-width: calc(100% / var(--zoom-multiplier)); overflow: hidden; text-overflow: ellipsis; white-space: nowrap; pointer-events: initial; font-size: 1.5em; padding: var(--size-4-1) var(--size-4-2); border-radius: var(--radius-s); color: var(--text-muted); background-color: rgba(var(--canvas-color), 0.1); line-height: 1; }
body:not(.is-ios) .canvas-wrapper.mod-animating .canvas-group-label { transition: transform 500ms cubic-bezier(0.16, 1, 0.3, 1) 0s; }
.canvas-wrapper:not(.mod-readonly) .canvas-group-label { cursor: grab; }
.canvas-wrapper:not(.mod-readonly) .canvas-group-label:active { cursor: grabbing; }
.canvas-group-label[contenteditable="true"] { cursor: text; background-color: var(--background-primary); box-shadow: 0 0 0 2px rgb(var(--canvas-color)); color: var(--text-normal); text-overflow: initial; }
.canvas-node-group.is-themed .canvas-group-label:not([contenteditable="true"]) { background-color: rgb(var(--canvas-color)); }
.canvas-node-group.is-themed .canvas-group-label:not([contenteditable="true"]).mod-foreground-light { color: var(--text-on-accent); }
.canvas-node-group.is-themed .canvas-group-label:not([contenteditable="true"]).mod-foreground-dark { color: var(--text-on-accent-inverted); }
.canvas-node-content { backface-visibility: hidden; width: 100%; height: 100%; overflow: hidden; position: relative; }
.canvas-node-content.markdown-embed { border: none; padding: 0px; }
.canvas-node-content.markdown-embed .inline-title { cursor: text; }
.canvas-node-content.markdown-embed > .markdown-embed-content > .markdown-preview-view { padding: 0 var(--size-4-6); display: flex; flex-direction: column; }
.canvas-wrapper:not(.mod-readonly) .canvas-node-content.markdown-embed > .markdown-embed-content > .markdown-preview-view { user-select: none; }
.canvas-node-content.markdown-embed > .markdown-embed-content > .markdown-preview-view::before, .canvas-node-content.markdown-embed > .markdown-embed-content > .markdown-preview-view::after { content: " "; display: block; min-height: min(calc(var(--canvas-node-height) * 0.1 - 3px), var(--size-4-6)); max-height: var(--size-4-4); flex: 1 1 0px; }
.canvas-node-content.markdown-embed > .markdown-embed-content > .markdown-preview-view > .markdown-preview-sizer { flex: 1 0 0px; }
.canvas-node-content.markdown-embed > .markdown-embed-content > .markdown-preview-view .callout { mix-blend-mode: normal; }
.canvas-node-content.markdown-embed > .markdown-embed-content > .markdown-preview-view .markdown-preview-pusher + div > :first-child { margin-top: 0px; }
.canvas-node-content.markdown-embed > .markdown-embed-content > .markdown-preview-view .mod-header + div > :first-child { margin-top: 0px; }
.canvas-node-content.markdown-embed > .markdown-embed-content > .markdown-preview-view .markdown-preview-sizer > div:last-child > :last-child { margin-bottom: 0px; }
.is-focused .canvas-node-content.markdown-embed > .markdown-embed-content > .markdown-preview-view { transform: translateZ(0px); }
.canvas-node.is-themed .canvas-node-content { background-color: rgba(var(--canvas-color), 0.07); }
.canvas-node-content.media-embed { justify-content: center; align-items: center; display: flex; }
.canvas-node-content.media-embed img, .canvas-node-content.media-embed video, .canvas-node-content.media-embed audio { flex-shrink: 0; flex-grow: 1; }
.canvas-node-content.media-embed img:not([width]), .canvas-node-content.media-embed video, .canvas-node-content.media-embed audio { max-width: 100%; }
.canvas-node-resizer { position: absolute; height: calc(var(--resizer-size) * var(--zoom-multiplier)); width: calc(var(--resizer-size) * var(--zoom-multiplier)); }
.is-selected .canvas-node-resizer { pointer-events: none; }
body.is-mobile .canvas-node-resizer { --zoom-multiplier: 1; }
.canvas-wrapper.mod-readonly .canvas-node-resizer { display: none; }
.canvas-node-resizer[data-resize="top"] { left: 0px; right: 0px; width: auto; top: calc(var(--resizer-size) * var(--zoom-multiplier) * -0.5); cursor: ns-resize; }
.canvas-node-resizer[data-resize="bottom"] { left: 0px; right: 0px; width: auto; bottom: calc(var(--resizer-size) * var(--zoom-multiplier) * -0.5); cursor: ns-resize; }
.canvas-node-resizer[data-resize="left"] { top: 0px; bottom: 0px; height: auto; left: calc(var(--resizer-size) * var(--zoom-multiplier) * -0.5); cursor: ew-resize; }
.canvas-node-resizer[data-resize="right"] { top: 0px; bottom: 0px; height: auto; right: calc(var(--resizer-size) * var(--zoom-multiplier) * -0.5); cursor: ew-resize; }
.canvas-node-resizer[data-resize="topright"] { right: calc(var(--resizer-size) * var(--zoom-multiplier) * -0.5); top: calc(var(--resizer-size) * var(--zoom-multiplier) * -0.5); cursor: nesw-resize; }
.canvas-node-resizer[data-resize="bottomright"] { right: calc(var(--resizer-size) * var(--zoom-multiplier) * -0.5); bottom: calc(var(--resizer-size) * var(--zoom-multiplier) * -0.5); cursor: nwse-resize; }
.canvas-node-resizer[data-resize="topleft"] { left: calc(var(--resizer-size) * var(--zoom-multiplier) * -0.5); top: calc(var(--resizer-size) * var(--zoom-multiplier) * -0.5); cursor: nwse-resize; }
.canvas-node-resizer[data-resize="bottomleft"] { left: calc(var(--resizer-size) * var(--zoom-multiplier) * -0.5); bottom: calc(var(--resizer-size) * var(--zoom-multiplier) * -0.5); cursor: nesw-resize; }
.is-mobile .canvas-node-resizer { pointer-events: none; }
.is-mobile .canvas-wrapper:not(.mod-readonly) .canvas-node-interaction-layer .canvas-node-resizer[data-resize="topright"], .is-mobile .canvas-wrapper:not(.mod-readonly) .canvas-node-interaction-layer .canvas-node-resizer[data-resize="bottomright"], .is-mobile .canvas-wrapper:not(.mod-readonly) .canvas-node-interaction-layer .canvas-node-resizer[data-resize="topleft"], .is-mobile .canvas-wrapper:not(.mod-readonly) .canvas-node-interaction-layer .canvas-node-resizer[data-resize="bottomleft"] { pointer-events: all; width: 20px; height: 20px; display: block; background-color: var(--background-primary); border: 2px solid var(--color-accent); border-radius: 3px; }
.canvas-node-connection-point { width: calc(var(--resizer-size) * var(--zoom-multiplier)); height: calc(var(--resizer-size) * var(--zoom-multiplier)); position: absolute; pointer-events: all; cursor: pointer; }
.canvas-node-connection-point[data-side="top"] { top: 1px; left: calc(50% - var(--resizer-size) * var(--zoom-multiplier) / 2); }
.canvas-node-connection-point[data-side="right"] { right: 1px; top: calc(50% - var(--resizer-size) * var(--zoom-multiplier) / 2); }
.canvas-node-connection-point[data-side="bottom"] { bottom: 1px; left: calc(50% - var(--resizer-size) * var(--zoom-multiplier) / 2); }
.canvas-node-connection-point[data-side="left"] { left: 1px; top: calc(50% - var(--resizer-size) * var(--zoom-multiplier) / 2); }
.canvas-node-connection-point::after { content: " "; background-color: var(--color-accent); border-radius: 50%; border: 3px solid var(--background-modifier-border); box-sizing: border-box; display: block; height: calc(var(--resizer-size) * var(--zoom-multiplier)); opacity: 0; position: relative; width: calc(var(--resizer-size) * var(--zoom-multiplier)); left: 0px; top: 0px; }
.is-mobile .canvas-node-interaction-layer .canvas-node-connection-point::after, .canvas-node-resizer:hover .canvas-node-connection-point::after { opacity: 1; }
.canvas-snaps { position: absolute; width: 100%; height: 100%; left: 0px; top: 0px; overflow: visible; pointer-events: none; opacity: 0.6; }
.canvas-snaps line { stroke-width: 1px; stroke: var(--color-accent); }
.canvas-snaps circle { fill: var(--color-accent); }
.canvas-edges { position: absolute; width: 100%; height: 100%; left: 0px; top: 0px; overflow: visible; pointer-events: none; }
.canvas-edges > * { pointer-events: initial; }
.canvas-edges path.canvas-display-path { pointer-events: none; stroke-width: calc(3px * var(--zoom-multiplier)); stroke: rgb(var(--canvas-color)); fill: none; transition: stroke-width 100ms ease-out 0s; }
.canvas-edges path.canvas-interaction-path { pointer-events: stroke; stroke-width: calc(24px * var(--zoom-multiplier)); stroke-linecap: round; stroke: transparent; fill: none; transition: stroke 100ms ease-out 0s; }
.canvas-wrapper:not(.mod-readonly) .canvas-edges path.canvas-interaction-path { cursor: grab; }
.canvas-wrapper:not(.mod-readonly) .canvas-edges path.canvas-interaction-path:active { cursor: grabbing; }
.canvas-edges polygon.canvas-path-end { pointer-events: none; stroke: rgb(var(--canvas-color)); fill: rgb(var(--canvas-color)); stroke-linecap: round; stroke-linejoin: round; stroke-width: 1px; transform-box: fill-box; transform: scale(var(--zoom-multiplier)); transform-origin: center top; }
.canvas-edges g.is-focused path.canvas-display-path, .canvas:not(.is-connecting) .canvas-edges g:hover path.canvas-display-path { stroke-width: calc(5.5px * var(--zoom-multiplier)); }
.canvas-edges g.is-focused path.canvas-interaction-path, .canvas:not(.is-connecting) .canvas-edges g:hover path.canvas-interaction-path { stroke: rgba(var(--canvas-color), 0.1); }
.canvas-path-label-wrapper { position: absolute; width: fit-content; height: fit-content; }
.canvas-path-label { font-size: calc(var(--font-ui-large) * var(--zoom-multiplier)); background-color: var(--background-primary); border-radius: var(--radius-s); padding: calc(var(--size-2-3) * var(--zoom-multiplier)); line-height: var(--line-height-tight); white-space: pre-wrap; transform: translate(-50%, -50%); text-align: center; max-width: calc(17em * var(--zoom-multiplier)); }
.canvas-path-label.is-editing { border-color: rgb(var(--canvas-color)); box-shadow: var(--shadow-stationary), 0 0 0 calc(3px * var(--zoom-multiplier)) rgb(var(--canvas-color)); }
.canvas-menu-container { position: absolute; width: 0px; height: 0px; top: 0px; left: 0px; }
.canvas-menu { position: relative; width: fit-content; height: fit-content; line-height: 1; background-color: var(--background-primary); border: 1px solid var(--background-modifier-border); border-radius: var(--radius-s); box-shadow: rgba(0, 0, 0, 0.07) 0px 2px 10px; display: flex; padding: var(--size-2-1); gap: 1px; }
.canvas-menu .clickable-icon { padding: var(--size-2-3) var(--size-4-2); }
.canvas-submenu { display: flex; position: absolute; top: calc(100% + 5px); left: 50%; transform: translateX(-50%); padding: var(--size-4-2); border: 1px solid var(--background-modifier-border); background-color: var(--background-primary); border-radius: var(--radius-s); box-shadow: rgba(0, 0, 0, 0.07) 0px 2px 10px; overflow: hidden; gap: 1px; }
.canvas-submenu .clickable-icon { padding: var(--size-2-2) var(--size-2-3); }
.canvas-color-picker-item { cursor: var(--cursor); width: 24px; height: 24px; margin: 2px; border-radius: 12px; border: 2px solid var(--background-primary); background-color: rgb(var(--canvas-color)); }
.canvas-color-picker-item.is-active { box-shadow: 0 0 0 2px rgb(var(--canvas-color)); }
@media (hover: hover) {
  .canvas-color-picker-item:hover { box-shadow: 0 0 0 2px rgb(var(--canvas-color)); }
}
.canvas-color-picker-item input[type="color"] { margin: -4px 0px 0px -2px; --swatch-width: 20px; --swatch-height: 20px; opacity: 0; }
.canvas-color-picker-item.canvas-color-picker-custom:not(.is-active) { background: conic-gradient(var(--color-red), var(--color-yellow), var(--color-green), var(--color-blue), var(--color-purple), var(--color-red)); }
@media (hover: hover) {
  .canvas-color-picker-item.canvas-color-picker-custom:not(.is-active):hover { box-shadow: 0 0 0 2px var(--background-modifier-border-hover); }
}
.canvas-empty-embed-container { align-items: center; display: flex; flex-direction: column; gap: var(--size-4-6); justify-content: center; height: 100%; padding: var(--size-4-3); text-align: center; }
.canvas-empty-embed-action-list { display: flex; flex-direction: column; gap: var(--size-4-3); }
.canvas-empty-embed-action-list button { font-size: var(--font-text-size); padding: var(--size-4-5) var(--size-4-9); }
.canvas-help { display: flex; flex-direction: column; gap: var(--size-4-3); }
.canvas-instruction { display: flex; justify-content: space-between; }
.canvas-instruction-desc { display: flex; gap: var(--size-4-1); }
.canvas-instruction-desc .setting-hotkey { display: inline; align-self: unset; padding: var(--size-4-1); margin: 0px; line-height: 1; }
.canvas-placeholder-message { max-width: 70vw; background: hsla(var(--color-accent-hsl), 0.1); border-radius: var(--radius-m); color: var(--color-accent); font-size: var(--font-ui-large); line-height: var(--line-height-normal); padding: var(--size-4-4) var(--size-4-6); pointer-events: none; position: absolute; text-align: center; transform: translate(-50%, -50%); }
.canvas-minimap { width: 100%; height: 100%; padding: var(--size-4-1); }
.inline-embed > .canvas-minimap { max-height: var(--embed-canvas-max-height); }
.canvas-minimap rect { stroke-width: 5px; stroke: var(--background-modifier-border); fill: var(--background-modifier-border); fill-opacity: 0.65; }
.canvas-minimap rect.is-themed { stroke: rgb(var(--canvas-color)); fill: rgb(var(--canvas-color)); fill-opacity: 0.5; }
.canvas-minimap path { stroke: rgb(192, 192, 192); fill: none; }
.canvas-minimap path.is-themed { stroke: rgb(var(--canvas-color)); }
.canvas-cursor { position: absolute; width: 1px; height: 1px; border: 5px solid var(--color-accent); border-radius: 5px; pointer-events: none; }
.canvas-watermark * { font-family: var(--font-default)  !important; }
.mod-macos.starter { app-region: drag; }
.starter { user-select: none; padding-top: 0px !important; }
.starter .titlebar { background-color: transparent; border: none; }
.starter .titlebar-inner .titlebar-text { display: none; }
.starter-screen { display: flex; flex-direction: column; background-color: var(--background-primary); width: 100%; height: 100%; }
.starter-screen-inner { flex-grow: 1; display: flex; height: calc(100% - 24px); }
.splash { align-items: center; background-color: var(--background-primary); display: flex; flex-direction: column; justify-content: center; flex: 1 1 auto; text-align: center; padding: 36px 0px 0px; }
.splash-brand { flex: 0 0 content; padding: 20px; }
.splash-brand-name { margin-top: 20px; flex-grow: 1; font-size: 30px; text-transform: uppercase; font-family: "Avenir Next", sans-serif; letter-spacing: 2px; line-height: 26px; }
.splash-brand-version { color: var(--text-muted); margin-top: 6px; font-size: var(--font-ui-small); }
.help-options-container { flex: 1 0 0px; overflow: auto; width: 100%; max-width: 82%; text-align: left; padding: var(--size-4-6) 0; }
.help-options-container::-webkit-scrollbar { display: none; }
.help-options-container .setting-item-description { max-width: 30em; padding-right: 12px; }
.help-options-container .setting-icon .svg-icon { stroke-width: 1px; --icon-size: 48px; color: var(--text-faint); }
.open-vault-options-container { flex: 1 0 0px; overflow: auto; width: 100%; position: relative; }
.open-vault-options-container::-webkit-scrollbar { display: none; }
.open-vault-options { position: absolute; top: 0px; left: 0px; width: 100%; height: 100%; padding: 12px 36px; text-align: left; overflow-y: auto; display: flex; flex-direction: column; }
.open-vault-options input[type="text"] { width: 150px; }
.open-vault-options .setting-item-control button { width: 100px; }
.open-vault-options .back-button { display: flex; align-items: center; app-region: no-drag; color: var(--text-muted); user-select: none; cursor: var(--cursor); }
@media (hover: hover) {
  .open-vault-options .back-button:hover { color: var(--text-normal); }
}
.open-vault-options .setting-item-description { display: -webkit-box; -webkit-line-clamp: 3; -webkit-box-orient: vertical; overflow: hidden; }
.open-vault-options.mod-login { justify-content: flex-start; }
.open-vault-options.mod-login input[type="text"] { width: 250px; }
.quick-start-container { margin-bottom: 10px; }
.quick-start-container button { font-size: var(--font-ui-medium); padding: 8px 60px; }
.quick-start-container + .setting-item { border-top: none; }
.open-folder-input[type="text"] { font-size: var(--font-ui-small); width: 200px; height: 28px; }
.browse-folder-button { margin-left: 10px; }
.open-folder-button { margin-top: 14px; padding: 6px 36px; }
.starter .notice { top: 38px; }
.setting-item.mod-change-language { app-region: no-drag; }
.setting-item.mod-change-language .setting-item-info { flex-grow: 0; }
.setting-item.mod-change-language .setting-item-control { flex-grow: 1; justify-content: flex-start; }
.setting-item.mod-change-language select { width: 100%; max-width: 100%; }
.setting-item.mod-change-language .setting-item-name { color: var(--text-faint); position: relative; top: 3px; cursor: var(--cursor); }
@media (hover: hover) {
  .setting-item.mod-change-language .setting-item-name:hover { color: var(--text-muted); }
}
.setting-icon { display: flex; color: var(--text-muted); margin-right: 24px; }
.choose-vault-clickable-area { text-align: center; padding: 40px 60px; border: 5px dashed var(--interactive-accent); border-radius: 10px; cursor: var(--cursor); }
@media (hover: hover) {
  .choose-vault-clickable-area:hover { background-color: hsla(var(--interactive-accent-hsl), 0.4); border: 5px solid hsla(var(--interactive-accent-hsl), 0.4); }
}
.choose-vault-label-welcome { line-height: 46px; color: var(--text-muted); }
.choose-vault-label-choose { font-weight: var(--font-extrabold); font-size: 32px; }
.recent-vaults { background-color: var(--background-secondary); border-right: 1px solid var(--background-modifier-border); padding: var(--size-4-8) var(--size-4-3) var(--size-4-2) var(--size-4-3); flex-shrink: 0; width: 280px; overflow-y: hidden; height: 100%; }
.recent-vaults-header { height: 30px; line-height: 30px; font-size: 18px; color: var(--text-muted); }
.recent-vaults-list { overflow-y: auto; height: 100%; }
.recent-vaults-list-item { app-region: no-drag; border-radius: var(--radius-s); margin-bottom: var(--size-4-1); padding: var(--size-4-2) var(--size-4-6) var(--size-4-2) var(--size-4-3); cursor: var(--cursor); position: relative; }
@media (hover: hover) {
  .recent-vaults-list-item:hover { background-color: var(--background-modifier-hover); color: var(--text-on-accent); }
}
.recent-vaults-list-item-name, .recent-vaults-list-item-path { word-break: break-all; }
.recent-vaults-list-item-name { border-radius: 2px; border: 1px solid transparent; }
.recent-vaults-list-item-name[contenteditable] { cursor: text; border-color: var(--interactive-accent); background-color: var(--background-modifier-hover); font-size: 0.9em; padding: 0 var(--size-4-1); }
.recent-vaults-list-item-path { font-size: var(--font-ui-smaller); color: var(--text-muted); line-height: 16px; }
.recent-vaults-list-item-option-button { position: absolute; top: var(--size-4-3); right: var(--size-4-1); color: var(--text-faint); width: 30px; height: 30px; line-height: 36px; text-align: center; transition: background-color 200ms ease-in-out 0s; }
.recent-vaults-list-item-option-button:hover { color: var(--text-normal); }
:root { --safe-area-inset-top: env(safe-area-inset-top); --safe-area-inset-bottom: env(safe-area-inset-bottom); --safe-area-inset-left: env(safe-area-inset-left); --safe-area-inset-right: env(safe-area-inset-right); }
.is-mobile { --ribbon-width: 58px; --view-header-height: 50px; --mobile-toolbar-height: 40px; --caret-color: var(--text-accent); --font-ui-smaller: calc(var(--font-text-size) * 0.8); --font-ui-small: calc(var(--font-text-size) * 0.937); --font-ui-medium: var(--font-text-size); --font-ui-large: calc(var(--font-text-size) * 1.2); --icon-s: 18px; --icon-m: 20px; --icon-l: 24px; --icon-l-stroke-width: 1.8px; --icon-opacity: 1; --input-height: 40px; --input-shadow: none; --input-shadow-hover: none; --input-font-weight: var(--font-medium); --input-border-width: 0px; --interactive-normal: var(--background-secondary); --mobile-sidebar-width: 340px; --mobile-sidebar-max-width: 500px; --nav-item-padding: var(--size-2-3) var(--size-4-2); --nav-item-color: var(--text-normal); --search-clear-button-size: 16px; --search-icon-size: 20px; --settings-home-background: var(--background-secondary); --slider-thumb-border-width: 0px; --slider-thumb-height: 24px; --slider-thumb-width: 24px; --slider-thumb-y: -9px; --slider-track-height: 6px; --swatch-shadow: none; --swatch-height: 40px; --swatch-width: 40px; --swatch-radius: 40px; --toggle-width: 48px; --toggle-radius: 26px; --toggle-thumb-radius: 26px; --toggle-thumb-height: 26px; --toggle-thumb-width: 26px; --file-margins: var(--size-4-2) var(--size-4-5); --background-modifier-cover: rgba(0, 0, 0, 0.25); --background-modifier-form-field: var(--background-secondary); --keyboard-background: var(--background-primary); --checkbox-size: 17px; }
.is-mobile.theme-dark { --color-base-00: #000; --color-base-10: #111; --color-base-20: #1e1e1e; --tag-background: hsla(var(--interactive-accent-hsl), 0.2); --modal-background: var(--background-secondary); --search-result-background: var(--background-secondary); --background-modifier-form-field: var(--background-modifier-border); --background-modifier-cover: rgba(0, 0, 0, 0.5); --background-modifier-hover: rgba(var(--mono-rgb-100), 0.15); --settings-home-background: var(--background-primary); }
.is-tablet { --nav-item-padding: var(--size-2-3) var(--size-4-3); --tab-font-size: var(--font-ui-smaller); }
.is-tablet.theme-dark { --titlebar-background: var(--background-primary); --titlebar-background-focused: var(--background-primary); --interactive-normal: var(--background-modifier-border); }
.is-phone { --border-width: 0.5pt; --divider-width: 0.5pt; --tab-outline-width: 0.5pt; --modal-header-height: 44px; --modal-community-sidebar-width: 100%; --nav-item-size: var(--font-ui-medium); }
body.is-mobile { height: 100vh; width: 100vw; caret-color: var(--caret-color); padding-bottom: 50px; }
.is-mobile .markdown-source-view.mod-cm6 .cm-content, .is-mobile .mod-cm6 .cm-line { caret-color: var(--caret-color); }
.is-mobile .markdown-source-view.mod-cm6 .cm-gutters { margin-left: -18px; }
.is-mobile .workspace > .mod-root { padding-left: var(--safe-area-inset-left); }
body.is-mobile { padding: var(--safe-area-inset-top) 0 0 0; text-size-adjust: 100%; }
.is-mobile .workspace-split.mod-left-split, .is-mobile .workspace-split.mod-right-split { display: none; }
.is-mobile .tree-item .tree-item-self { padding-right: var(--size-4-2); }
.is-mobile .input-label { display: block; text-align: left; color: var(--text-muted); margin-bottom: 8px; }
.is-mobile input[type="text"] { display: block; width: 100%; padding: 8px 12px; height: auto; }
.is-mobile .markdown-rendered pre:not(:hover) > button.copy-code-button { display: block; }
.is-mobile .markdown-rendered button.copy-code-button { width: auto; }
.is-mobile .empty-state-action-list { margin-top: 40px; }
.is-mobile .empty-state-action { background-color: var(--background-primary-alt); margin: 12px 0px; padding: 6px 30px; border-radius: var(--button-radius); text-align: center; }
.is-mobile .login-field { width: 100%; margin: 0.5em 0px; }
.is-mobile .login-field input { width: 100%; }
.is-mobile .markdown-rendered .frontmatter-container { margin-top: 20px; }
.is-mobile .markdown-rendered .heading-collapse-indicator { margin-left: -20px; }
.is-mobile .markdown-rendered ul, .is-mobile .markdown-rendered ol { padding-inline-start: 25px; }
.is-mobile .message-container { text-align: center; margin: 8px 0px; }
.is-mobile .search-result-file-match-replace-button { display: block; position: relative; padding: 6px 10px; right: 0px; margin-top: 6px; background-color: var(--background-secondary-alt); }
.is-mobile .suggestion-flair { position: relative; margin-right: 6px; left: 0px; top: 0px; }
.is-mobile .document-search-container { height: auto; margin-left: 0px; margin-right: 0px; padding: 0 var(--size-4-4) var(--size-4-2); border-bottom: var(--border-width) solid var(--background-modifier-border); }
.is-mobile .document-search-container.mod-replace-mode { height: auto; }
.is-mobile .document-search, .is-mobile .document-replace { height: auto; padding: 0px; }
.is-mobile .document-search .document-search-button, .is-mobile .document-replace .document-search-button { height: auto; padding: 6px 0px; background-color: transparent; color: var(--text-accent); }
.is-mobile .document-search input, .is-mobile .document-replace input, .is-mobile .document-search button, .is-mobile .document-replace button { width: auto; flex-grow: 1; }
.is-mobile .document-search .document-search-buttons, .is-mobile .document-replace .document-search-buttons, .is-mobile .document-search .document-replace-buttons, .is-mobile .document-replace .document-replace-buttons { display: flex; flex-grow: 1; }
.is-mobile .document-search .document-search-close-button, .is-mobile .document-replace .document-search-close-button { height: 34px; line-height: 34px; top: 0px; }
.is-tablet .mod-left-split-toggle { display: none; }
.is-tablet button:not(.clickable-icon) { padding: var(--size-4-1) var(--size-4-5); }
.is-phone button { width: 100%; }
.is-phone .vault-list-item-creation-time { display: none; }
.is-phone .vault-list-item { padding: 5px 0px; }
.is-phone .vault-list-item .flair { display: none; }
.is-phone .vault-list-item-title { flex: 1 0 auto; }
.is-phone .vault-list-item-button { margin-right: 0px; }
.suggestion-bg { display: none; }
body.is-phone .suggestion-bg { display: block; }
@keyframes fadeIn { 
  0% { opacity: 0; }
  100% { opacity: 1; }
}
@keyframes fadeOut { 
  0% { opacity: 1; }
  100% { opacity: 0; }
}
.mobile-image-viewer { position: absolute; height: 100%; width: 100%; top: 0px; left: 0px; background-color: var(--background-modifier-cover); display: flex; justify-content: center; overflow: hidden; z-index: var(--layer-modal); }
.mobile-image-viewer img { align-self: center; max-height: 100%; max-width: 100%; }
.mod-tappable { transition: opacity 0.15s ease-in-out 0s; }
.mod-tappable.mod-tap { opacity: 0.5; }
.is-mobile .document-search-container { height: auto; margin-left: 0px; margin-right: 0px; padding: 0 var(--size-4-4) var(--size-4-2); border-bottom: var(--border-width) solid var(--background-modifier-border); }
.is-mobile .document-search-container.mod-replace-mode { height: auto; }
.is-mobile .document-search, .is-mobile .document-replace { height: auto; padding: 0px; }
.is-mobile .document-search .document-search-button, .is-mobile .document-replace .document-search-button { height: auto; padding: 6px 0px; background-color: transparent; color: var(--text-accent); }
.is-mobile .document-search input, .is-mobile .document-replace input, .is-mobile .document-search button, .is-mobile .document-replace button { width: auto; flex-grow: 1; }
.is-mobile .document-search .document-search-buttons, .is-mobile .document-replace .document-search-buttons, .is-mobile .document-search .document-replace-buttons, .is-mobile .document-replace .document-replace-buttons { display: flex; flex-grow: 1; }
.is-mobile .document-search .document-search-close-button, .is-mobile .document-replace .document-search-close-button { height: 34px; line-height: 34px; top: 0px; }
.is-mobile .view-header { border-top: none; height: var(--view-header-height); }
.is-mobile .workspace-split.mod-root > .workspace-leaf:first-of-type .workspace-leaf-content, .is-mobile .workspace-split.mod-root > .workspace-leaf:last-of-type .workspace-leaf-content { border-radius: 0px; }
.is-mobile .view-header-title { padding-right: 0px; }
.is-mobile .view-header-title-container { padding-left: 24px; }
.is-mobile .view-header-title-container::after { display: none; }
.is-mobile .view-header-icon { padding: 10px; }
.is-mobile .inline-title { padding-top: 0.25em; }
.is-mobile .horizontal-main-container { position: relative; }
.is-mobile .view-header-title-container { height: 50px; }
.is-mobile .view-actions { padding: var(--size-4-2) 0; gap: var(--size-2-1); }
.is-mobile .view-header-nav-buttons, .is-mobile .view-header .view-action { --icon-color: var(--interactive-accent); --icon-color-hover: var(--interactive-accent); --icon-color-active: var(--interactive-accent-hover); --icon-color-focus: var(--interactive-accent-hover); --icon-size: var(--icon-l); --icon-stroke: var(--icon-l-stroke-width); }
.is-mobile .view-action { margin: auto 0px; width: auto; }
.is-phone .view-header-title-parent, .is-phone .view-header-title { display: block; text-overflow: ellipsis; opacity: 0.7; }
.is-phone .view-header-title-parent:focus-within, .is-phone .view-header-title:focus-within { text-overflow: unset; opacity: 1; }
.is-mobile .hotkey-list-container .setting-item { flex-direction: column; align-items: stretch; }
.is-mobile .hotkey-list-container .setting-item-control { margin-top: 10px; align-items: flex-start; }
.is-mobile .hotkey-list-container .setting-command-hotkeys { flex: 1 0 auto; }
.is-mobile .hotkey-list-container .setting-hotkey { align-self: flex-start; }
.is-tablet .horizontal-tab-nav-item, .is-tablet .vertical-tab-nav-item { padding: var(--size-4-2) var(--size-4-3); }
.is-tablet .modal.mod-settings .vertical-tab-header { max-width: none; }
.is-tablet.theme-dark .community-item, .is-tablet.theme-dark .vertical-tab-content { background-color: var(--background-secondary); }
.is-phone.theme-dark .modal.mod-settings { background-color: var(--background-primary); }
.is-phone.theme-dark .modal.mod-settings .vertical-tab-header { background-color: var(--background-primary); }
.is-phone.theme-dark .modal.mod-settings .vertical-tab-nav-item { background-color: var(--background-secondary); }
.is-phone.theme-dark .modal.mod-settings .vertical-tab-header-title { background-color: var(--background-primary); }
.is-phone .setting-item-heading { margin-top: 1.5em; }
.is-phone .vertical-tab-header-group { margin: 0px auto; width: calc(100% - var(--size-4-8)); }
.is-phone .vertical-tab-header-group-title { padding-bottom: 1em; }
.is-phone .vertical-tab-header-group-title, .is-phone .setting-item-heading .setting-item-name { color: var(--text-normal); font-weight: var(--font-bold); font-size: var(--font-ui-large); }
.is-phone .setting-item { padding: 1em 0px; border-width: var(--border-width) 0 0 0; gap: var(--size-4-1); }
.is-phone .setting-item-name { font-weight: var(--font-medium); }
.is-phone .setting-item-info { min-width: 0px; }
.is-phone .setting-item:not(.mod-toggle):not(.setting-item-heading) { flex-direction: column; align-items: flex-start; }
.is-phone .setting-item:not(.mod-toggle):not(.setting-item-heading) .setting-item-control { margin-top: 12px; width: 100%; }
.is-phone .setting-icon { margin-right: 10px; display: inline-flex; vertical-align: middle; }
.is-phone .setting-item-control select, .is-phone .setting-item-control input, .is-phone .setting-item-control button { width: 100%; margin: 0px; }
.is-phone .setting-item-control button { padding: 10px; }
.is-phone .setting-item-control select { max-width: 100%; }
.is-phone .modal.mod-settings { background-color: var(--background-secondary); }
.is-phone .modal.mod-settings .modal-title { border-bottom: var(--border-width) solid var(--background-modifier-border); }
.is-phone .modal.mod-settings .vertical-tabs-container { display: block; overflow-y: auto; }
.is-phone .modal.mod-settings .vertical-tab-header { background-color: var(--background-secondary); border-right: none; flex-grow: 1; height: 100%; min-width: 100%; padding: var(--size-4-4); width: 100%; }
.is-phone .modal.mod-settings .vertical-tab-content { background-color: var(--background-primary); padding: var(--size-4-5) max(var(--size-4-5), var(--safe-area-inset-right)) 100px max(var(--size-4-5), var(--safe-area-inset-left)); }
.is-phone .modal.mod-settings .vertical-tab-header-group-items { border-radius: var(--radius-m); overflow: hidden; }
.is-phone .modal.mod-settings .vertical-tab-nav-item { display: flex; align-items: center; height: 44px; background-color: var(--background-primary); padding: 0 var(--size-4-2) 0 var(--size-4-3); margin: 0px; border-radius: 0px; border-bottom: var(--border-width) solid var(--background-modifier-border); transition: background-color 200ms ease-in-out 0s, color 200ms ease-in-out 0s; }
.is-phone .modal.mod-settings .vertical-tab-nav-item.is-active { background-color: var(--interactive-accent); }
.is-phone .modal.mod-settings .vertical-tab-nav-item:last-child { border-bottom: none; }
.is-phone .modal.mod-settings .vertical-tab-nav-item-chevron { display: flex; margin-left: auto; color: var(--text-faint); }
.is-phone .vertical-tab-header-title { font-weight: var(--font-semibold); }
.is-phone .community-modal { width: 100%; margin-bottom: 10px; }
.is-phone .modal.mod-community-theme { min-height: unset; }
.is-phone .community-modal-sidebar { background-color: var(--background-primary); }
.is-phone .community-modal-controls { background-color: transparent; }
.is-phone .community-modal-controls .setting-item { flex: 0 0 auto; padding: 0.25em 0px; }
.is-phone .community-modal-controls .setting-item-control { flex-direction: column; align-items: flex-end; }
.is-phone .community-modal-controls .search-input-container { width: 100%; }
.is-phone .community-modal-search-results { gap: 0px; padding: 0px; }
.is-phone .community-modal-info { padding: var(--size-4-4); }
.is-phone .community-item { border-width: 0 0 var(--border-width) 0; border-radius: 0px; padding: var(--size-4-4); }
.is-phone .community-item-info { padding: 20px; }
.is-phone .community-modal-details { background-color: var(--background-primary); border: none; }
.is-phone .community-modal-readme { padding: 20px 0px; }
.is-phone .community-modal-controls { padding: 0 var(--size-4-4); }
.is-phone .community-modal-search-summary { padding: var(--size-4-1) var(--size-4-1) var(--size-4-4); }
.is-phone .mod-community-theme .community-item { display: grid; grid-template-columns: 1fr 160px; grid-auto-flow: column dense; }
.is-phone .mod-community-theme .community-item .community-item-name { grid-column: 1 / 2; }
.is-phone .mod-community-theme .community-item .community-item-author { grid-column: 1 / 2; }
.is-phone .mod-community-theme .community-item .community-item-badge.mod-update { position: static; grid-row: 4 / auto; }
.is-phone .mod-community-theme .community-item .community-item-downloads { grid-column: 1 / 2; }
.is-phone .mod-community-theme .community-item .community-item-screenshot { grid-row: 1 / span 4; height: 90px; }
.is-phone .mod-community-plugin .community-item { display: grid; grid-template-columns: 3fr 1fr; grid-auto-flow: column dense; }
.is-phone .mod-community-plugin .community-item .community-item-name { grid-column: 1 / 2; }
.is-phone .mod-community-plugin .community-item .community-item-author { grid-column: 1 / 2; }
.is-phone .mod-community-plugin .community-item .community-item-badge.mod-update { position: static; grid-row: 4 / auto; }
.is-phone .mod-community-plugin .community-item .community-item-downloads { grid-column: 2 / 2; text-align: right; color: var(--text-faint); }
.is-phone .mod-community-plugin .community-item .community-item-desc { grid-column: 1 / span 2; }
.is-phone .community-modal-button-container { flex-direction: column; }
.mobile-option-setting-item { font-size: var(--font-ui-medium); display: flex; align-items: center; margin: 8px 0px; gap: var(--size-4-1); transition: transform 1000ms ease-in-out 0s; color: var(--text-muted); }
.mobile-option-setting-item:first-of-type:last-of-type .mobile-option-setting-drag-icon { display: none; }
.mobile-option-setting-item-name { flex: 1 0 0px; color: var(--text-normal); }
.mobile-option-setting-item-option-icon { display: flex; align-items: center; justify-content: center; padding: 4px; cursor: var(--cursor); border-radius: var(--radius-s); }
:not(.is-mobile) .mobile-option-setting-item-option-icon:hover, :not(.is-mobile) .mobile-option-setting-item-option-icon:active { background-color: var(--background-modifier-hover); }
.mobile-option-setting-item-option-icon.mobile-option-setting-drag-icon { cursor: grab; }
.mobile-option-setting-item-option-icon.mobile-option-setting-drag-icon:active { cursor: grabbing; }
.mobile-option-setting-item-remove-icon { color: var(--text-error); display: flex; }
.mobile-option-setting-item-add-icon { color: var(--text-success); display: flex; }
.is-mobile .status-bar { display: none; }
.workspace-drawer { position: fixed; top: 0px; bottom: 0px; display: flex; overflow: hidden; font-size: var(--font-ui-small); min-width: var(--mobile-sidebar-width); max-width: var(--mobile-sidebar-max-width); width: 85vw; z-index: var(--layer-popover); margin: 0px; border-radius: 0px; padding-top: var(--safe-area-inset-top); background-color: var(--background-primary); }
.workspace-drawer .nav-folder.mod-root > .nav-folder-title { display: none; }
.workspace-drawer .nav-header { margin-top: auto; padding-bottom: max(var(--size-4-2), var(--safe-area-inset-bottom)); order: 10; }
.workspace-drawer .nav-header ~ .search-input-container { width: calc(100% - var(--size-4-9)); }
.workspace-drawer .workspace-leaf { background-color: transparent; }
.theme-dark .workspace-drawer { background-color: var(--background-secondary); }
.workspace-drawer.is-pinned { height: 100%; position: relative; max-width: var(--mobile-sidebar-width); z-index: var(--layer-cover); border-radius: 0px; margin: 0px; box-shadow: none; }
.workspace-drawer.mod-left { left: 0px; padding-left: var(--safe-area-inset-left); border-top-right-radius: var(--radius-xl); border-bottom-right-radius: var(--radius-xl); }
.workspace-drawer.mod-left.is-pinned { border-right: var(--divider-width) solid var(--divider-color); border-radius: 0px; }
body.is-tablet .workspace-drawer.mod-left .workspace-drawer-inner { padding-left: var(--ribbon-width); }
.workspace-drawer.mod-right { right: 0px; padding-right: var(--safe-area-inset-right); border-top-left-radius: var(--radius-xl); border-bottom-left-radius: var(--radius-xl); }
.workspace-drawer.mod-right.is-pinned { border-left: var(--divider-width) solid var(--divider-color); border-radius: 0px; }
.workspace-drawer.is-collapsed { overflow: hidden; }
.workspace-drawer .nav-buttons-container { padding-left: var(--size-4-3); padding-right: var(--size-4-3); --icon-size: var(--icon-l); --icon-stroke: var(--icon-l-stroke-width); --icon-color: var(--interactive-accent); --icon-color-hover: var(--interactive-accent); --icon-color-active: var(--interactive-accent); --icon-color-focus: var(--interactive-accent-hover); }
.workspace-drawer .nav-buttons-container .nav-action-button { flex-grow: 1; }
.workspace-drawer .workspace-drawer-actions, .workspace-drawer .nav-buttons-container { overflow: auto; flex-wrap: nowrap; }
.workspace-drawer .workspace-drawer-actions::-webkit-scrollbar, .workspace-drawer .nav-buttons-container::-webkit-scrollbar, .workspace-drawer .workspace-drawer-actions::-webkit-scrollbar-thumb, .workspace-drawer .nav-buttons-container::-webkit-scrollbar-thumb { visibility: hidden; }
.workspace-drawer .side-dock-settings { margin-bottom: 0px; }
.workspace-drawer-inner { flex: 1 1 auto; overflow: hidden; display: flex; flex-direction: column; background-color: var(--background-primary); position: relative; transition: width 150ms ease-out 0s; }
.theme-dark .workspace-drawer-inner { background-color: var(--background-secondary); }
.workspace-drawer.is-collapsed .workspace-drawer-inner { padding: 0px; width: 0px; }
.workspace-drawer-backdrop { display: block; position: fixed; z-index: var(--layer-cover); width: 100%; height: 100%; background-color: var(--background-modifier-cover); top: 0px; left: 0px; opacity: 1; transition: opacity 150ms ease-out 0s; }
.workspace-drawer.is-collapsed .workspace-drawer-backdrop { display: none; opacity: 0; }
.workspace-drawer-ribbon { position: absolute; left: 0px; top: 0px; height: 100%; overflow: auto; width: var(--ribbon-width); padding: var(--size-4-1) 0 var(--safe-area-inset-bottom); }
.workspace-drawer-ribbon::-webkit-scrollbar, .workspace-drawer-ribbon::-webkit-scrollbar-thumb { visibility: hidden; width: 0px; }
.workspace-drawer-ribbon .side-dock-actions { padding: var(--size-4-2) 0; }
.workspace-drawer-ribbon .side-dock-actions, .workspace-drawer-ribbon .side-dock-settings { gap: var(--size-4-2); }
.workspace-drawer-ribbon .side-dock-ribbon-action { padding: var(--size-4-2); }
.workspace-drawer-header { padding: var(--size-4-2) var(--size-4-5) 0 var(--size-4-5); display: flex; align-items: flex-start; }
.workspace-drawer.is-pinned .workspace-drawer-header { padding-top: 0px; }
.workspace-drawer-header-left { display: flex; flex-direction: column; flex: 1 1 auto; overflow: hidden; }
.workspace-drawer-header-name { display: flex; }
.workspace-drawer-header-switcher { display: flex; flex: 0 1 auto; position: relative; }
.workspace-drawer-header-switcher select { opacity: 0; position: absolute; }
.workspace-drawer-header-name-text { text-overflow: ellipsis; overflow: hidden; font-size: var(--font-ui-large); font-weight: var(--font-semibold); }
.workspace-drawer-header-name-chevron { --icon-size: var(--icon-m); --icon-stroke: 2.25px; color: var(--text-faint); display: flex; align-items: center; margin-left: var(--size-2-1); }
.workspace-drawer-header-name-action-icon { color: var(--text-muted); margin-left: var(--size-4-2); display: flex; align-items: center; }
.workspace-drawer-header-info { color: var(--text-muted); margin: var(--size-4-1) 0 var(--size-4-4) 0; font-size: var(--font-ui-small); }
.workspace-drawer-header-icon { --icon-size: var(--icon-l); --icon-stroke: var(--icon-l-stroke-width); padding-top: var(--size-2-2); color: var(--interactive-accent); margin-left: var(--size-4-3); }
.workspace-drawer-actions { margin: var(--size-4-4) 0 var(--size-4-3) 0; display: flex; color: var(--text-muted); }
.workspace-drawer-action-item { flex: 0 0 70px; display: flex; flex-direction: column; align-items: center; overflow: hidden; }
.workspace-drawer-action-icon { color: var(--text-faint); }
.workspace-drawer-action-short-name { font-size: var(--font-ui-small); overflow: hidden; white-space: nowrap; text-overflow: ellipsis; max-width: 80px; }
.workspace-drawer-separator { margin: 0px 0px 12px; }
.workspace-drawer-tab-option-item { display: flex; align-items: center; margin: var(--size-4-5); gap: var(--size-4-2); }
.workspace-drawer-active-tab-icon, .workspace-drawer-tab-option-item-icon { --icon-size: var(--icon-l); --icon-stroke: var(--icon-l-stroke-width); color: var(--text-normal); display: flex; }
.workspace-drawer-active-tab-icon:last-child { color: var(--interactive-accent); order: 2; }
.workspace-drawer-active-tab-back-icon { --icon-size: var(--icon-l); --icon-stroke: var(--icon-l-stroke-width); display: flex; color: var(--interactive-accent); order: 1; margin-right: var(--size-4-1); }
.workspace-drawer-tab-option-item-title, .workspace-drawer-active-tab-title { color: var(--text-normal); font-weight: var(--font-medium); font-size: var(--font-ui-medium); flex: 1 0 0px; overflow: hidden; white-space: nowrap; text-overflow: ellipsis; }
.workspace-drawer-active-tab-header { display: flex; align-items: center; padding: var(--size-4-3) var(--size-4-5) var(--size-4-4); margin: 0px; gap: var(--size-4-2); }
.workspace-drawer-tab-container { overflow: hidden; position: relative; flex: 1 0 0px; }
.workspace-drawer-tab-container > * { position: absolute; top: 0px; left: 0px; width: 100%; height: 100%; }
.workspace-drawer-active-tab-icon.mod-exit-fullscreen { display: none; }
.workspace-drawer-active-tab-container { display: flex; flex-direction: column; }
.theme-dark .workspace-drawer-active-tab-container.is-fullscreen { background-color: var(--background-secondary); }
.workspace-drawer-active-tab-container .workspace-drawer-active-tab-content .nav-files-container { padding-top: var(--size-4-3); }
.workspace-drawer-active-tab-container.is-fullscreen { position: fixed; width: 100%; top: 0px; left: 0px; background-color: var(--background-primary); margin: 0 env(safe-area-inset-right, 20px) 0 env(safe-area-inset-left, 20px); padding: env(safe-area-inset-top, 20px) 0 0; }
.workspace-drawer-active-tab-container.is-fullscreen .workspace-drawer-active-tab-back-icon { display: none; }
.workspace-drawer-active-tab-container.is-fullscreen .workspace-leaf { width: 100%; }
.workspace-drawer-active-tab-container.is-fullscreen .workspace-drawer-active-tab-header { margin: 0 env(safe-area-inset-right, 20px) 0 env(safe-area-inset-left, 20px); padding: var(--size-4-4) var(--size-4-6); }
.workspace-drawer-active-tab-content { flex: 1 0 0px; overflow: auto; display: flex; }
.workspace-drawer-active-tab-content > * { flex: 1 0 0px; width: 100%; height: 100%; }
.workspace-drawer-active-tab-content .view-header { display: none !important; }
.workspace-drawer-active-tab-content .view-content { padding-top: 4px; height: 100%; }
.workspace-drawer-active-tab-content .graph-controls { display: none; }
.workspace-drawer-active-tab-content .outline { font-size: var(--font-ui-medium); }
.is-phone .side-dock-ribbon { display: none; }
.is-phone .workspace-drawer .workspace-drawer-header-icon.mod-pin { display: none; }
.is-phone .mod-root .workspace-split:not(.mod-visible), .is-phone .mod-root .workspace-tabs:not(.mod-visible) { display: none; }
.is-tablet .workspace-drawer .workspace-drawer-header-icon.mod-settings { display: none; }
body.is-tablet .sidebar-toggle-button { padding-left: var(--size-4-2); --icon-color: var(--interactive-accent); --icon-color-hover: var(--interactive-accent); --icon-color-active: var(--interactive-accent-hover); --icon-color-focus: var(--interactive-accent-hover); --icon-size: var(--icon-l); --icon-stroke: var(--icon-l-stroke-width); }
.is-mobile .menu { border: none; max-width: 100%; }
.is-phone .menu { background-color: var(--background-secondary); max-height: 60vh; width: calc(100% - var(--safe-area-inset-left) - var(--safe-area-inset-right)); min-width: unset; position: absolute; padding-bottom: var(--safe-area-inset-bottom); border-radius: var(--radius-l) var(--radius-l) 0 0; bottom: 0px; left: 0px; right: 0px; margin: 0px auto; overflow-y: auto; top: unset !important; }
.is-phone .menu-item { padding: var(--size-4-3) var(--size-4-3); height: unset; line-height: unset; }
.is-mobile .modal { border: none; }
.is-mobile .modal-button-container { display: flex; flex-direction: column; }
.is-mobile .community-modal { width: 100%; margin-bottom: 10px; }
.is-mobile .modal.mod-community-theme { min-height: unset; }
.is-mobile .mod-confirmation .modal-close-button { display: none; }
.is-phone .modal, .is-phone .prompt, .is-phone .suggestion-container { border-radius: 0px; border: none; max-height: 100vh; width: 100vw; max-width: 100vw; min-width: unset; position: absolute; bottom: unset; padding: 0px; left: 0px; right: 0px; }
.is-phone .modal { transition: max-height 0.2s ease 0s, height 0.2s ease 0s; border-radius: var(--radius-m); bottom: 0px; height: 100%; max-height: 66vh; margin: 0px; padding: 0 var(--safe-area-inset-right) 0 var(--safe-area-inset-left); width: 100vw; }
.is-phone .modal .modal-close-button { top: var(--size-4-3); }
.is-phone .modal:focus-within { max-height: calc(100vh - var(--safe-area-inset-top)); }
.is-phone .modal .modal-title { display: block; font-size: var(--font-ui-medium); margin-bottom: 0px; padding-top: var(--size-4-3); text-align: center; }
.is-phone .modal-sidebar { background-color: var(--background-primary); }
.is-phone .modal-content { display: flex; position: relative; flex-direction: column; margin-top: 0px; overflow: auto; padding: var(--size-4-3); }
.is-phone .modal-button-container { width: 100%; padding: var(--size-4-3); margin-top: 0px; margin-bottom: var(--safe-area-inset-bottom); }
.is-phone .modal.mod-lg { max-height: 100%; }
.is-phone .modal.mod-lg .modal-title { padding-top: calc(env(safe-area-inset-top) + var(--size-4-3)); padding-bottom: var(--size-4-3); }
.is-phone .modal.mod-lg .modal-close-button, .is-phone .modal.mod-sidebar-layout .modal-close-button { top: calc(var(--safe-area-inset-top) + 10px); right: var(--size-4-5); }
.is-phone .modal.mod-sidebar-layout { bottom: 0px; top: 0px; border-radius: 0px; height: 100%; max-height: 100%; margin: 0px; padding: 0 var(--safe-area-inset-right) 0 var(--safe-area-inset-left); width: 100vw; }
.is-phone .modal.mod-sidebar-layout .search-input-container { flex-grow: 1; }
.is-phone .modal.mod-sidebar-layout .modal-title { display: block; padding-top: calc(env(safe-area-inset-top) + var(--size-4-3)); padding-bottom: var(--size-4-3); margin-bottom: 0px; }
.is-phone .modal.mod-sidebar-layout .modal-content > * { width: 100%; height: 100%; position: absolute; top: 0px; left: 0px; right: 0px; padding: 0 var(--safe-area-inset-right) 0 var(--safe-area-inset-left); }
.mobile-navbar { background-color: var(--background-primary); padding: 0 max(var(--safe-area-inset-right), var(--size-4-4)) 0 max(var(--safe-area-inset-left), var(--size-4-4)); position: absolute; left: 0px; right: 0px; bottom: 0px; }
body.is-tablet .mobile-navbar { display: none; }
.mobile-navbar-text { font-size: var(--font-ui-small); padding: var(--size-4-1) 0; white-space: nowrap; text-overflow: clip; width: 100%; -webkit-mask-image: linear-gradient(to left, rgba(0, 0, 0, 0) var(--size-4-4), #000000 var(--size-4-8)); }
.mobile-navbar-actions { --icon-size: var(--icon-l); --icon-stroke: var(--icon-l-stroke-width); --icon-color: var(--interactive-accent); --icon-color-hover: var(--interactive-accent); --icon-color-active: var(--interactive-accent-hover); --icon-color-focus: var(--interactive-accent-hover); display: flex; align-items: center; justify-content: space-between; padding: var(--size-4-2) 0 max(var(--size-4-2), var(--safe-area-inset-bottom)) 0; }
.mobile-navbar-tabs-action { align-items: center; border-radius: var(--clickable-icon-radius); border: 2px solid var(--icon-color); display: flex; font-size: calc(var(--icon-size) * 0.6); font-weight: var(--bold-weight); justify-content: center; height: 20px; width: var(--icon-size); }
.mobile-navbar-action.has-longpress-menu { position: relative; }
.mobile-navbar-action.has-longpress-menu .navbar-action-flair { --icon-size: 12px; --icon-stroke: 3px; color: var(--interactive-accent); position: absolute; left: -6px; top: 0px; height: 100%; align-items: center; display: flex; }
.is-phone .notice-container { padding: 0px; top: max(var(--size-4-1), var(--safe-area-inset-top)); left: 0px; right: 0px; max-width: 96%; margin: 0px auto; }
.is-phone .notice { background-color: var(--interactive-accent); color: var(--text-on-accent); margin: 0 auto var(--size-4-1); text-align: center; border-radius: 30px; max-width: none; box-shadow: none; }
.is-mobile .prompt { border: none; }
.theme-dark.is-mobile .prompt { background-color: var(--background-secondary); }
.theme-dark.is-mobile .prompt input.prompt-input { background-color: var(--background-secondary); }
.is-mobile .prompt-input[type="text"] { padding: var(--size-4-4); }
.is-phone .prompt { position: relative; margin: 0px auto; width: calc(100% - var(--safe-area-inset-left) - var(--safe-area-inset-right)); }
.is-phone .prompt .suggestion-hotkey { display: none; }
.is-phone .prompt { --mobile-height: 100vh; --prompt-bottom: 0px; --prompt-top: calc(var(--safe-area-inset-top) + var(--header-height) + var(--size-4-2)); border-radius: var(--radius-l) var(--radius-l) 0 0; min-width: unset; margin-bottom: var(--prompt-bottom); margin-top: var(--prompt-top); box-shadow: none; top: 0px; height: calc(var(--mobile-height) - var(--prompt-top) - var(--prompt-bottom)); }
.is-phone .prompt-input-container { border-bottom: var(--border-width) solid var(--background-modifier-border); }
.is-phone .prompt-input[type="text"] { border: none; }
.is-phone .prompt-input-cta { --icon-color: var(--interactive-accent); display: flex; align-items: center; padding: 0 var(--size-4-3); flex: 0 1 auto; }
.is-phone .prompt-instructions { display: none; }
.pull-action { position: absolute; background-color: var(--background-secondary); z-index: var(--layer-popover); color: var(--text-muted); font-size: 90%; transition: background-color 150ms ease-in-out 0s; }
.pull-action.mod-activated { background-color: var(--interactive-accent); color: var(--text-on-accent); }
.pull-down-action { top: 0px; left: 0px; right: 0px; width: 96%; max-width: 500px; margin: var(--safe-area-inset-top) auto 0 auto; padding: var(--size-4-3) var(--size-4-4); text-align: center; border-radius: 40px; }
.pull-out-action { top: 50%; padding: var(--size-4-3) var(--size-4-4); border-radius: 40px; margin: 0 var(--size-4-4); }
.mobile-toolbar { app-region: drag; flex: 0 0 auto; width: 100%; overflow-y: hidden; background-color: var(--background-primary); bottom: 0px; z-index: var(--layer-menu); }
.mobile-toolbar-options-container { height: var(--mobile-toolbar-height); display: flex; overflow: auto hidden; width: 100%; padding: 0px 10px; }
.mobile-toolbar-options-container::-webkit-scrollbar { width: 0px !important; height: 0px !important; }
.mobile-toolbar-option { display: flex; font-size: var(--font-ui-medium); color: var(--text-muted); font-family: var(--font-monospace); justify-content: center; align-items: center; min-width: 50px; position: relative; left: 0px; transition: left 200ms ease-in-out 0s; }
.mobile-toolbar-option.mod-ghost { position: absolute; transition: left 250ms ease-in-out 0s; }
.mobile-toolbar-option.mod-ghost::before { content: " "; position: absolute; width: 100%; height: 100%; top: 0px; left: 0px; border-radius: 6px; background-color: var(--interactive-accent); }
.mobile-toolbar-done-button { position: fixed; margin-top: var(--size-4-2); margin-right: var(--size-4-3); top: env(safe-area-inset-top, 20px); right: env(safe-area-inset-right, 20px); z-index: var(--layer-status-bar); }
.is-mobile .suggestion-item { padding: var(--size-4-2) var(--size-4-3); }
.is-tablet.theme-dark .suggestion-container { background-color: var(--background-secondary); }
.is-phone .suggestion-container { margin: 0px auto; padding-bottom: calc(var(--safe-area-inset-bottom) + var(--mobile-toolbar-height)); width: calc(100% - var(--safe-area-inset-left) - var(--safe-area-inset-right)); border-top: 1px solid var(--background-modifier-border); background-color: var(--background-primary); box-shadow: none; border-radius: 0px; bottom: 0px; overflow: auto; max-height: 35vh; }
.is-phone .suggestion { position: relative; }
.is-phone .suggestion-item.mod-group { border-radius: 0px; }
.is-mobile .modal.mod-publish { background-color: var(--modal-background); border-radius: 0px; height: 100%; margin: 0px; padding-top: var(--safe-area-inset-top); width: 100vw; }
.is-mobile .publish-changes-info-publishing-to { display: none; }
.is-mobile .publish-changes-add-linked-btn { width: auto; }
.is-phone .modal.mod-publish .modal-button-container { background-color: var(--modal-background); position: fixed; }
.is-phone .modal.mod-publish .modal-content { display: unset; }
.is-mobile .sync-history-list { padding: 0px; }
.is-mobile .sync-history-list-item { padding: 12px 16px; }
.is-mobile .sync-history-content-container { display: flex; flex-direction: column; max-width: unset; }
.is-mobile .sync-history-content { flex: 1 1 auto; padding: 10px; border-radius: 0px; border: none; }
.is-phone .sync-log-container { flex: 1 1 auto; }
.is-phone .modal.mod-sync-history .search-input-container { width: 100%; margin-bottom: 0px; }
.mobile-vault-chooser { width: 100%; height: 100%; background-color: var(--background-secondary); position: relative; }
.mobile-vault-chooser hr { margin: 12px 0px; }
.mobile-vault-chooser-screen { display: flex; flex-direction: column; position: absolute; left: 0px; top: 0px; width: 100%; height: 100%; }
.mobile-vault-chooser-header { display: flex; background-color: var(--background-secondary-alt); border-bottom: 1px solid var(--background-primary); color: var(--text-muted); flex: 0 0 50px; font-size: 18px; align-items: center; }
.mobile-vault-chooser-header-icon { display: flex; margin: 0px 6px 0px 10px; }
.mobile-vault-chooser-content { flex: 1 0 0px; padding: 20px; height: 100%; overflow-y: auto; }
.mobile-vault-chooser-logo-container { margin: 40px 0px; text-align: center; color: var(--text-muted); }
.mobile-vault-chooser-logo { font-size: 32px; text-transform: uppercase; font-family: "Avenir Next", sans-serif; letter-spacing: 2px; margin-bottom: 10px; }
.mobile-vault-chooser-version { font-size: var(--font-ui-small); }
.mobile-vault-chooser-empty-state { margin: 20px 0px; font-size: 17px; color: var(--text-muted); }
.mobile-vault-chooser-action-icon { color: var(--text-muted); display: flex; padding: 10px; margin: -10px 0px; }
.mobile-vault-chooser-action { display: flex; padding: 14px 0px; align-items: center; font-size: 20px; }
.mobile-vault-chooser-action-name { flex: 1 0 0px; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
.mobile-vault-chooser-action-description { color: var(--text-muted); font-size: 17px; overflow: hidden; text-overflow: ellipsis; max-width: calc(100vw - 110px); white-space: nowrap; }
.mobile-vault-chooser-field-name { color: var(--text-muted); margin: 20px 0px 10px; font-size: 18px; }
input.mobile-vault-chooser-field-input { width: 100%; font-size: var(--font-ui-medium); padding: 8px 12px; height: auto; }
.mobile-vault-chooser-button-container { margin: 20px 0px; }
.mobile-vault-chooser-button-container button { padding: 10px 20px; font-size: var(--font-ui-medium); width: 100%; }
 </style>
			<style>  </style>

			<!-- Theme Styles -->
			<style> /* Using default theme. */ </style>

			<!-- Plugin Styles -->
			<style> /*#region Code Copy */

/* Make code block copy button fade in and out */
.markdown-rendered pre:not(:hover) > button.copy-code-button
{
	display: unset;
	opacity: 0;
}

.markdown-rendered pre:hover > button.copy-code-button
{
	opacity: 1;
}

.markdown-rendered pre button.copy-code-button
{
	transition: opacity 0.2s ease-in-out, width 0.3s ease-in-out, background-color 0.2s ease-in-out;
	text-overflow: clip;
}

.markdown-rendered pre > button.copy-code-button:hover
{
	background-color: var(--interactive-normal);
}

.markdown-rendered pre > button.copy-code-button:active
{
	background-color: var(--interactive-hover);
	box-shadow: var(--input-shadow);
	transition: none;
}

/*#endregion */

/*#region Canvas */
.canvas-card-menu {
	display: none;
	cursor: default !important;

}

.canvas-controls {
	display: none;
	cursor: default !important;

}

.canvas-node-connection-point 
{
	display: none;
	cursor: default !important;

}

.canvas-menu-container {
	display: none;
}

.canvas-node-content-blocker
{
	display: none;
	cursor: pointer !important;
}

.canvas-wrapper
{
	position: relative;
	cursor: default !important;
}

.canvas-node-resizer
{
	cursor: default !important;
}

.canvas-node-container
{
	cursor: default !important;
}

/*#endregion */

/*#region Sidebars */

.sidebar {
    background-color: var(--background-secondary);
    flex: 1 0 min-content;
    display: flex;
    align-items: flex-start;
    font-size: 14px;
}

.sidebar-section-header
{
  margin: 0em 0 0em var(--sidebar-margin);
  text-transform: uppercase;
  letter-spacing: 0.06em;
  font-weight: 600;
}

.sidebar-content {
    width: var(--sidebar-width);
    line-height: var(--line-height-tight);
    display: flex;
    flex-direction: column;
    padding: 10px;
    padding-bottom: 0;
    height: 100%;
}

.sidebar-scroll-area
{
    width: 100%;
    height: 100%;
    line-height: var(--line-height-tight);
    display: flex;
    flex-direction: column;
    overflow-y: scroll;
}

.sidebar-left
{
    border-right: 1px dashed var(--divider-color);
	z-index: 1000;
	align-items: flex-end;
    flex-direction: row-reverse;
}

.sidebar-right
{
    border-left: 1px dashed var(--divider-color);
	z-index: 1000;
	align-items: flex-start;
    flex-direction: row;
}

@media print 
{
    .sidebar, .outline-container, .theme-toggle-container, .theme-toggle-container-inline, .toggle-background, .theme-toggle-input
    {
        display: none !important;
    }
}

/*#endregion */

/*#region Content / Markdown Preview View */

.webpage-container {
    background-color: var(--background-primary);
    display: flex;
    flex-direction: row;
    height: 100%;
    width: 100%;
    align-items: stretch;
    position: fixed;
}

.document-container
{
    flex-basis: var(--content-width);
}

.markdown-reading-view
{
    align-self: center;
    -ms-flex-align: center;
    width: 100%;
}

.markdown-preview-view
{
    display: flex;
    width: 100%;
    max-width: 100%;
    padding-bottom: 30em;
    align-items: flex-start;
    justify-content: center;
}

.document-container > .markdown-preview-view > .markdown-preview-sizer
{
    padding: unset;
    width: unset;
    height: unset;
    margin: unset;
    max-width: unset;
    min-height: unset;
    max-width: var(--line-width);
    flex-basis: var(--line-width);
}

/*#endregion */

/*#region Kanban */

.markdown-preview-view.kanban-plugin__markdown-preview-view {
    font-family: var(--font-text, var(--default-font));
    font-size: .875rem;
    line-height: var(--line-height-tight);
    padding: unset;
    width: unset;
    height: unset;
    position: unset;
    overflow-y: unset;
    overflow-wrap: unset;
    color: unset;
    user-select: unset;
    -webkit-user-select: unset;
}

.kanban-plugin__item-button-wrapper, .kanban-plugin__lane-grip, .kanban-plugin__lane-settings-button.clickable-icon, .kanban-plugin__item-postfix-button.clickable-icon
{
    display: none;
}

/*#endregion */

/*#region Tree */

/* Base tree */
.tree-container 
{
	/* padding-bottom: 12px; */
	/* margin: 12px; */
	/* height: 100%; */
	/* position: relative; */
	/* display: contents; */
	position: relative;
	height: 100%;
	width: auto;
	margin: var(--sidebar-margin);
	margin-top: 3em;
    margin-bottom: 0;
}

.tree-container .tree-header 
{
	display: flex;
	flex-direction: row;
	align-items: center;
	position: absolute;
	top: -3em;
}

.tree-container .tree-header .sidebar-section-header
{
    margin: 1em;
    margin-left: 0;
}

.tree-container:has(.tree-scroll-area:empty) 
{
    display: none;
}

.tree-container .tree-scroll-area 
{
	width: 100%;
	height: 100%;
	max-height: 100%;
	overflow-y: scroll;
	padding: 1em;
	padding-right: calc(1em + var(--sidebar-margin));
	padding-bottom: 3em;
	border-radius: var(--radius-m);
	position: absolute;
}

.tree-container .tree-item 
{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 0;
}

.tree-container .tree-item-children
{
    padding: 0;
    margin-left: 0;
    border-left: none;
    width: 100%;
}

.tree-container .tree-item.mod-active > .tree-item-contents > .tree-item-link
{
    color: var(--color-accent);
}

.tree-container .tree-item-contents {
    position: relative;
    display: flex;
    flex-direction: row;
    align-items: center;
    border-radius: 0.4em;
    color: var(--nav-item-color);
    width: 100%;
    margin-left: var(--tree-horizontal-spacing);
}

.tree-container .tree-item-contents:active 
{
    color: var(--nav-item-color-active);
}

.tree-container a.tree-item-link 
{
    width: 100%;
    height: 100%;
    transition: background-color 0.1s;
    border-radius: var(--radius-s);
    padding-left: calc(var(--tree-horizontal-spacing) + var(--collapse-arrow-size)/2 + 1px);
    padding-bottom: calc(var(--tree-vertical-spacing) / 2);
    padding-top: calc(var(--tree-vertical-spacing) / 2);
    color: var(--nav-item-color);
    text-decoration: none;
}

.tree-container .tree-item-icon.collapse-icon {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    border-radius: var(--radius-s);
    transition: background-color 0.1s;
    position: absolute;
    height: 100%;
}

.tree-container .tree-item.mod-tree-folder > .tree-item-contents > .tree-item-icon.collapse-icon
{
    width: 100%;
}

.collapse-icon > svg {
    color: unset !important;
}

.collapse-icon:hover 
{
    color: var(--nav-item-color-hover);
}

.tree-container a.tree-item-link:hover 
{
    cursor: pointer;
    color: var(--nav-item-color-hover);
    text-decoration: underline;
}

/* Indentation guide */

.tree-container > .tree-scroll-area > * .tree-item
{
    margin-left: calc(var(--tree-horizontal-spacing) + var(--collapse-arrow-size) / 2 + 1px);
    border-left: var(--nav-indentation-guide-width) solid var(--nav-indentation-guide-color);
}

.tree-container .tree-scroll-area > * > * > .tree-item
{
    margin-left: calc(var(--collapse-arrow-size) / 2 + 1px);
}

.tree-container .tree-item.mod-active
{
    border-left: var(--nav-indentation-guide-width) solid var(--color-accent);
}


.tree-container .tree-item:hover:not(.mod-active):not(.mod-collapsible):not(:has(.tree-item:hover)) /* Hover */
{
    border-left: var(--nav-indentation-guide-width) solid var(--nav-item-color-hover);
}

.webpage-container .tree-container .tree-item:not(.mod-collapsible) > .tree-item-children > .tree-item,
.webpage-container .tree-container > .tree-scroll-area > .tree-item,
.webpage-container .tree-container:not(.mod-nav-indicator) .tree-item
{
    border-left: none !important;
}

.webpage-container .tree-container .tree-item:not(.mod-collapsible) > .tree-item-children > .tree-item > .tree-item-contents,
.webpage-container .tree-container:not(.mod-nav-indicator) .tree-item .tree-item-contents,
.webpage-container .tree-container > .tree-scroll-area > .tree-item > .tree-item-contents
{
    margin-left: 0 !important;
}

/* Special */

.tree-container.outline-tree .tree-item[data-depth='1'] > .tree-item-contents > .tree-item-link
{
    font-weight: 900;
    font-size: 1.1em;
    margin-left: 0;
}

.tree-container .tree-item.is-collapsed > .tree-item-contents > .tree-item-icon.collapse-icon > svg
{
    transition: transform 0.1s ease-in-out;
    transform: rotate(-90deg);
}



/*#endregion */

/*#region Headers */

.collapse-icon svg.svg-icon {
    color: var(--nav-collapse-icon-color);
    stroke-width: 4px;
    width: var(--collapse-arrow-size);
    height: var(--collapse-arrow-size);
    transition: transform 100ms ease-in-out 0s;
    min-width: 10px;
    min-height: 10px;
}

div.is-collapsed > * > .heading-collapse-indicator.collapse-icon > svg
{
    transition: transform 0.1s ease-in-out;
    transform: rotate(-90deg);
}

/*#endregion */

/*#region Text Wrapping */
a {
    overflow-wrap: anywhere;
}

* 
{
    overflow-wrap: break-word;
}

/*#endregion */

/*#region Obsidian Columns Plugin */
.columnParent {
    display: flex;
    padding: 15px 20px;
    flex-wrap: wrap;
    gap: 20px;
}

.columnParent {
    white-space: normal;
}

.columnChild {
    flex-grow: 1;
    flex-basis: 0px;
}
/*#endregion */

/*#region Theme Toggle */

.theme-toggle-container {
    --toggle-width: 50px;
    --toggle-height: 23px;
    --border-radius: calc(var(--toggle-height) / 2);
    --handle-width: calc(var(--toggle-height) * 0.65);
    --handle-radius: calc(var(--handle-width) / 2);
    --handle-margin: calc((var(--toggle-height) / 2.0) - var(--handle-radius));
    --handle-translation: calc(var(--toggle-width) - var(--handle-width) - (var(--handle-margin) * 2));

    display: inline-block;
    cursor: pointer;
	margin: 10px;
}

/* animation to expand width, move handle, then contract width */
@keyframes toggle-slide-right
{
    0%
    {
        width: var(--handle-width);
        transform: translateX(0);
    }
    50%
    {
        width: calc(var(--toggle-width) * 0.5);
    }
    90%
    {
        width: var(--handle-width);
    }
    100%
    {
        transform: translateX(var(--handle-translation));
    }
}

@keyframes toggle-slide-left
{
    0%
    {
        width: var(--handle-width);
        transform: translateX(calc(var(--handle-translation) - ((var(--toggle-width) * 0.33) - var(--handle-width))));
    }
    70%
    {
        width: calc(var(--toggle-width) * 0.5);
    }
    100%
    {
        width: var(--handle-width);
        transform: translateX(0);
    }
}

/* just exapnd and contract */
@keyframes toggle-expand-right
{
    0%
    {
        width: var(--handle-width);
    }
    100%
    {
        width: calc(var(--toggle-width) * 0.33);
    }
}

@keyframes toggle-expand-left
{
    0%
    {
        width: var(--handle-width);
        transform: translateX(var(--handle-translation));
    }
    100%
    {
        width: calc(var(--toggle-width) * 0.33);
        transform: translateX(calc(var(--handle-translation) - ((var(--toggle-width) * 0.33) - var(--handle-width))));
    }
}

@keyframes toggle-contract
{
    0%
    {
        width: calc(var(--toggle-width) * 0.33);
    }
    100%
    {
        width: var(--handle-width);
    }
}

.theme-toggle-input {
    display: none;
    z-index: 1000;
}

/* Fill in dark mode / default */
.toggle-background {
    position: relative;
    width: var(--toggle-width);
    height: var(--toggle-height);
    border-radius: var(--border-radius);
	background-color: var(--background-modifier-border);

    transition: background-color 0.2s;
    z-index: 1000;

    /* box-shadow: inset 0px 0px 100px -70px var(--color-accent); */
}

/* Handle default */
.toggle-background::before 
{
    content: "";
    position: absolute;
    left: var(--handle-margin);
    top: var(--handle-margin);
    height: var(--handle-width);
    width: var(--handle-width);
    
    border-radius: var(--handle-radius);
    background-color: var(--text-normal);
    box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.2);
    animation: toggle-slide-left 0.2s ease-in-out normal both;

    z-index: 1000;
}

/* handle light*/
.theme-toggle-input:checked ~ .toggle-background::before 
{
    animation: toggle-slide-right 0.2s ease-in-out normal both;
}

.theme-toggle-input:active ~ .toggle-background::before 
{
    animation: toggle-expand-right 0.2s ease-in-out normal both;
}

.theme-toggle-input:active:checked ~ .toggle-background::before
{
    animation: toggle-expand-left 0.2s ease-in-out normal both;
}

/* sun moon icon icon default */
.toggle-background::after
{
    content: "";
    position: absolute;
    right: var(--handle-margin);
    top: calc(var(--handle-margin));
    height: var(--handle-width);
    width: var(--handle-width);
    transition: transform 0.3s;
    background: url('https://api.iconify.design/lucide/moon.svg?color=white') no-repeat center center;
    transform: scale(0.9);
}

/* sun moon icon icon light */
.theme-toggle-input:checked ~ .toggle-background::after
{
    transform: translateX(calc(var(--handle-translation) * -1)) scale(0.9);
    background: url('https://api.iconify.design/lucide/sun.svg') no-repeat center center;
}

/*#endregion */

/*#region Graph View */
#graph-canvas
{
    width: 100%;
    height: 100%;
    border: 1px solid var(--modal-border-color);
    border-radius: var(--modal-radius);
    aspect-ratio: 1/1;
}

.graph-view-container.expanded
{
    position: fixed;
    width: 60%;
    height: 90%;
    right: 20%;
    top: 5%;
    background-color: var(--background-secondary);
    z-index: 1000;
}

.graph-view-container 
{
    position: relative;
    width: 100%;
    aspect-ratio: 1/1;
    display: flex;
}

.graph-icon 
{
    cursor: pointer;
    color: var(--text-muted);
}

.graph-view-container .graph-icon > svg
{
    width: 24px;
    height: 24px;

    background-color: var(--color-base-00);
    outline-width: 6px;
    outline-color: var(--color-base-00);
    outline-offset: -1px;
    outline-style: solid;
    border-radius: 100px;
    margin: 10px;
}

.graph-view-placeholder 
{
    padding: 0;
    width: auto;
    aspect-ratio: 1/1;
    position: relative;
    flex: none;
    margin: var(--sidebar-margin);
}

.graph-view-placeholder:has(.expanded)
{
    border-radius: var(--modal-radius);
    border: 1px solid var(--modal-border-color);
}

.scale-down 
{
    transition: transform 0.2s ease-in-out;
    transform: scale(0.9);
}

.scale-up 
{
    transition: transform 0.2s ease-in-out;
    transform: scale(1);
}

.graph-expand 
{
    position: absolute;
    top: 5px;
    right: 5px;
}



/*#endregion */

/*#region Tweaks */

hr
{
    border: none;
	border-top: var(--hr-thickness) solid;
    border-color: var(--hr-color);
}

.markdown-embed-link
{
    display: none;
}

/*#endregion */
 </style>

			<!-- Snippets -->
			<style> 
 </style>
		
			
<script>

//#region Helpers

function getAbsoluteRootPath()
{
	if (typeof rootPath == 'undefined') setupRootPath(document);
	return new URL(window.location.href + "/../" + rootPath).pathname;
}

function getURLPath(url = window.location.pathname)
{
	let absoluteRoot = getAbsoluteRootPath();
	let pathname = url.substring(absoluteRoot.length);
	return pathname;
}

function getURLRootPath(url = window.location.pathname)
{
	let path = getURLPath(url);
	let splitPath = path.split("/");
	let rootPath = "";
	for (let i = 0; i < splitPath.length - 1; i++)
	{
		rootPath += "../";
	}
	return rootPath;
}

async function setTreeCollapsed(element, collapsed, animate = true)
{
	if (!element || !element.classList.contains("mod-collapsible")) return;

	let children = element.querySelector(".tree-item-children");

	if (collapsed)
	{
		element.classList.add("is-collapsed");
		if(animate) slideUp(children, 100);
		else children.style.display = "none";
	}
	else
	{
		element.classList.remove("is-collapsed");
		if(animate) slideDown(children, 100);
		else children.style.removeProperty("display");
	}
}

async function setTreeCollapsedAll(elements, collapsed, animate = true)
{
	let childrenList = [];
	elements.forEach(async element => 
	{
		if (!element || !element.classList.contains("mod-collapsible")) return;

		let children = element.querySelector(".tree-item-children");

		if (collapsed)
		{
			element.classList.add("is-collapsed");
		}
		else
		{
			element.classList.remove("is-collapsed");
		}

		childrenList.push(children);
	});

	if (collapsed)
	{
		if(animate) slideUpAll(childrenList, 100);
		else childrenList.forEach(async children => children.style.display = "none");
	}
	else
	{
		if(animate) slideDownAll(childrenList, 100);
		else childrenList.forEach(async children => children.style.removeProperty("display"));
	}
}

function toggleTreeCollapsed(element)
{
	if (!element) return;
	setTreeCollapsed(element, !element.classList.contains("is-collapsed"));
}

function toggleTreeCollapsedAll(elements)
{
	if (!elements) return;
	setTreeCollapsedAll(elements, !elements[0].classList.contains("is-collapsed"));
}

function getHeaderEl(headerDiv)
{
	let possibleChildHeader = headerDiv.firstChild;
	let isHeader = false;

	while (possibleChildHeader != null)
	{
		isHeader = possibleChildHeader ? /[Hh][1-6]/g.test(possibleChildHeader.tagName) : false;
		if (isHeader) break;

		possibleChildHeader = possibleChildHeader.nextElementSibling;
	}

	return possibleChildHeader;
}

function getPreviousHeader(headerDiv)
{
	let possibleParent = headerDiv.previousElementSibling;
	let isHeader = false;

	while (possibleParent != null)
	{
		let possibleChildHeader = getHeaderEl(possibleParent);
		isHeader = possibleChildHeader ? /[Hh][1-6]/g.test(possibleChildHeader.tagName) : false;
		if (isHeader) break;

		possibleParent = possibleParent.previousElementSibling;
	}

	return possibleParent;
}

function setHeaderOpen(headerDiv, open, openParents = true)
{
	if(headerDiv.tagName != "DIV" || !getHeaderEl(headerDiv))
	{
		console.error("setHeaderOpen() must be called with a header div");
		return;
	}

	// let selector = getHeadingContentsSelector(header);
	if (open) 
	{
		headerDiv.classList.remove("is-collapsed");
		headerDiv.style.display = "";
	}
	if (!open)
	{
		headerDiv.classList.add("is-collapsed");
	}

	let headerEl = getHeaderEl(headerDiv);

	let childHeaders = [];

	let possibleChild = headerDiv.nextElementSibling;

	// loop through next siblings showing/ hiding children until we reach a header of the same or lower level
	while (possibleChild != null)
	{
		let possibleChildHeader = getHeaderEl(possibleChild);

		if(possibleChildHeader)
		{
			// if header is a sibling of this header then break
			if (possibleChildHeader.tagName <= headerEl.tagName) break;

			// save child headers to be re closed afterwards
			childHeaders.push(possibleChild);
		}

		if (!open) possibleChild.style.display = "none";
		else possibleChild.style.display = "";

		possibleChild = possibleChild.nextElementSibling;
	}

	if(open)
	{
		// if we are opening the header then we need to make sure that all closed child headers stay closed
		childHeaders.forEach(function(item)
		{
			if (item.classList.contains("is-collapsed"))
			{
				setHeaderOpen(item, false);
			}
		});

		// if we are opening the header then we need to make sure that all parent headers are open
		if (openParents)
		{
			let previousHeader = getPreviousHeader(headerDiv);
			
			while (previousHeader != null)
			{
				let previousHeaderEl = getHeaderEl(previousHeader);

				if (previousHeaderEl.tagName < headerEl.tagName)
				{
					// if header is a parent of this header then unhide
					setHeaderOpen(previousHeader, true);
					break;
				}
				
				previousHeader = getPreviousHeader(previousHeader);
			}
		}
	}
}

let slideUp = (target, duration=500) => {

	target.style.transitionProperty = 'height, margin, padding';
	target.style.transitionDuration = duration + 'ms';
	target.style.boxSizing = 'border-box';
	target.style.height = target.offsetHeight + 'px';
	target.offsetHeight;
	target.style.overflow = 'hidden';
	target.style.height = 0;
	target.style.paddingTop = 0;
	target.style.paddingBottom = 0;
	target.style.marginTop = 0;
	target.style.marginBottom = 0;
	window.setTimeout(async () => {
			target.style.display = 'none';
			target.style.removeProperty('height');
			target.style.removeProperty('padding-top');
			target.style.removeProperty('padding-bottom');
			target.style.removeProperty('margin-top');
			target.style.removeProperty('margin-bottom');
			target.style.removeProperty('overflow');
			target.style.removeProperty('transition-duration');
			target.style.removeProperty('transition-property');
	}, duration);
}

let slideUpAll = (targets, duration=500) => {

	targets.forEach(async target => {
		target.style.transitionProperty = 'height, margin, padding';
		target.style.transitionDuration = duration + 'ms';
		target.style.boxSizing = 'border-box';
		target.style.height = target.offsetHeight + 'px';
		target.offsetHeight;
		target.style.overflow = 'hidden';
		target.style.height = 0;
		target.style.paddingTop = 0;
		target.style.paddingBottom = 0;
		target.style.marginTop = 0;
		target.style.marginBottom = 0;
	});

	window.setTimeout(async () => {
		targets.forEach(async target => {
			target.style.display = 'none';
			target.style.removeProperty('height');
			target.style.removeProperty('padding-top');
			target.style.removeProperty('padding-bottom');
			target.style.removeProperty('margin-top');
			target.style.removeProperty('margin-bottom');
			target.style.removeProperty('overflow');
			target.style.removeProperty('transition-duration');
			target.style.removeProperty('transition-property');
		});
	}, duration);
}

let slideDown = (target, duration=500) => {

	target.style.removeProperty('display');
	let display = window.getComputedStyle(target).display;
	if (display === 'none') display = 'block';
	target.style.display = display;
	let height = target.offsetHeight;
	target.style.overflow = 'hidden';
	target.style.height = 0;
	target.style.paddingTop = 0;
	target.style.paddingBottom = 0;
	target.style.marginTop = 0;
	target.style.marginBottom = 0;
	target.offsetHeight;
	target.style.boxSizing = 'border-box';
	target.style.transitionProperty = "height, margin, padding";
	target.style.transitionDuration = duration + 'ms';
	target.style.height = height + 'px';
	target.style.removeProperty('padding-top');
	target.style.removeProperty('padding-bottom');
	target.style.removeProperty('margin-top');
	target.style.removeProperty('margin-bottom');
	window.setTimeout(async () => {
		target.style.removeProperty('height');
		target.style.removeProperty('overflow');
		target.style.removeProperty('transition-duration');
		target.style.removeProperty('transition-property');
	}, duration);
}

let slideDownAll = (targets, duration=500) => {

	targets.forEach(async target => {
		target.style.removeProperty('display');
		let display = window.getComputedStyle(target).display;
		if (display === 'none') display = 'block';
		target.style.display = display;
		let height = target.offsetHeight;
		target.style.overflow = 'hidden';
		target.style.height = 0;
		target.style.paddingTop = 0;
		target.style.paddingBottom = 0;
		target.style.marginTop = 0;
		target.style.marginBottom = 0;
		target.offsetHeight;
		target.style.boxSizing = 'border-box';
		target.style.transitionProperty = "height, margin, padding";
		target.style.transitionDuration = duration + 'ms';
		target.style.height = height + 'px';
		target.style.removeProperty('padding-top');
		target.style.removeProperty('padding-bottom');
		target.style.removeProperty('margin-top');
		target.style.removeProperty('margin-bottom');
	});

	window.setTimeout( async () => {
		targets.forEach(async target => {
			target.style.removeProperty('height');
			target.style.removeProperty('overflow');
			target.style.removeProperty('transition-duration');
			target.style.removeProperty('transition-property');
		});
	}, duration);
}

var slideToggle = (target, duration = 500) => {
	if (window.getComputedStyle(target).display === 'none') {
		return slideDown(target, duration);
	} else {
		return slideUp(target, duration);
	}
}

var slideToggleAll = (targets, duration = 500) => {
	if (window.getComputedStyle(targets[0]).display === 'none') {
		return slideDownAll(targets, duration);
	} else {
		return slideUpAll(targets, duration);
	}
}

//#endregion

async function loadDocument(url, pushHistory = true, scrollTo = true)
{
	console.log("Loading document: " + url);
	
	// change the active file
	setActiveDocument(url, scrollTo, pushHistory);

	let response;

	// if(typeof embeddedDocuments == 'undefined')
	// {
	try
	{
		response = await fetch(url);
	}
	catch (error)
	{
		console.log("Cannot use fetch API (likely due to CORS), just loading the page normally.");
		window.location.assign(url);
		return;
	}
	// }
	// else
	// {
	// 	response = new Response(embeddedDocuments[url], {status: 200, statusText: "OK"});
	// }

	let doc = document.implementation.createHTMLDocument();

	if (response.ok)
	{
		let html = (await response.text()).replaceAll("<!DOCTYPE html>", "").replaceAll("<html>", "").replaceAll("</html>", "");
		doc.documentElement.innerHTML = html;

		// copy document content and outline tree
		document.querySelector(".document-container").innerHTML = doc.querySelector(".document-container").innerHTML;
		document.querySelector(".outline-tree").innerHTML = doc.querySelector(".outline-tree").innerHTML;
	
		// if the url has a heading, scroll to it
		let splitURL = url.split("#");
		let pathnameTarget = splitURL[0] ?? url;
		let headingTarget = splitURL.length > 1 ? splitURL[1] : null;
		if (headingTarget) document.getElementById(headingTarget).scrollIntoView();

		// Change the root path to match the match from the new page
		setupRootPath(doc);

		// initialize events on the new page
		initializePage(document.querySelector(".document-container"));
		initializePage(document.querySelector(".outline-tree"));

		document.title = doc.title;
	}
	else
	{
		// if the page is not able to load instead add a header saying the page doesn't exist
		document.querySelector(".markdown-preview-view").innerHTML = 
		`
		<div>
			<center style='position: relative; transform: translateY(20vh); width: 100%; text-align: center;'>
				<h1 style>Page Not Found</h1>
			</center>
		</div>
		`;

		document.querySelector(".outline-tree").innerHTML = "";

		console.log("Page not found: " + getAbsoluteRootPath() + url);
		let newRootPath = getURLRootPath(getAbsoluteRootPath() + url);
		rootPath = newRootPath;
		document.querySelector("base").href = newRootPath;

		document.title = "Page Not Found";
	}

	return doc;
}

function setActiveDocument(url, scrollTo = true, pushHistory = true)
{
	let pathnameTarget = url.split("#")[0] ?? url; // path with no header

	// switch active file in file tree
	document.querySelector(".tree-item.mod-active")?.classList.remove("mod-active");
	let treeItems = Array.from(document.querySelectorAll(".tree-item > .tree-item-contents > .tree-item-link"));
	let treeItem = undefined;
	for (let item of treeItems) 
	{
		if (item.getAttribute("href") == url)
		{
			let parent = item.parentElement.parentElement;

			parent.classList.add("mod-active");
			treeItem = parent;
			
			while (parent.hasAttribute("data-depth"))
			{
				setTreeCollapsed(parent, false, false);
				parent = parent.parentElement.parentElement;
			}

			continue;
		}
	}

	if(scrollTo) treeItem?.scrollIntoView({block: "center", inline: "nearest"});

	// set the active file in th graph view
	if(typeof nodes != 'undefined' && window.renderWorker)
	{
		let activeNode = nodes?.paths.findIndex(function(item) { return item.endsWith(pathnameTarget); }) ?? -1;
		
		if(activeNode >= 0) 
		{
			window.renderWorker.activeNode = activeNode;
		}
	}

	if(pushHistory && window.location.protocol != "file:") window.history.pushState({ path: pathnameTarget }, '', pathnameTarget);
}

//#region Initialization
function setupThemeToggle(setupOnNode)
{
	if (localStorage.getItem("theme_toggle") != null)
    {
        setThemeToggle(localStorage.getItem("theme_toggle") == "true");
    }

	// var lastScheme = "theme-dark";
	// change theme to match current system theme
	// if (localStorage.getItem("theme_toggle") == null && window.matchMedia && window.matchMedia('(prefers-color-scheme: light)').matches)
	// {
	// 	setThemeToggle(true);
	// 	lastScheme = "theme-light";
	// }
	// if (localStorage.getItem("theme_toggle") == null && window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches)
	// {
	// 	setThemeToggle(true);
	// 	lastScheme = "theme-dark";
	// }

	// set initial toggle state based on body theme class
	if (document.body.classList.contains("theme-light"))
	{
		setThemeToggle(true);
	}
	else
	{
		setThemeToggle(false);
	}

	function setThemeToggle(state, instant = false)
	{
		let toggle = document.querySelector(".theme-toggle-input");

		toggle.checked = state;

		if (instant) 
		{	
			var oldTransition = document.body.style.transition;
			document.body.style.transition = "none";
		}

		if(!toggle.classList.contains("is-checked") && state)
		{
			toggle.classList.add("is-checked");
		}
		else if (toggle.classList.contains("is-checked") && !state)
		{
			toggle.classList.remove("is-checked");
		}

		if(!state)
		{
			if (document.body.classList.contains("theme-light"))
			{
				document.body.classList.remove("theme-light");
			}

			if (!document.body.classList.contains("theme-dark"))
			{
				document.body.classList.add("theme-dark");
			}
		}
		else
		{
			if (document.body.classList.contains("theme-dark"))
			{
				document.body.classList.remove("theme-dark");
			}

			if (!document.body.classList.contains("theme-light"))
			{
				document.body.classList.add("theme-light");
			}
		}

		if (instant)
		{
			setTimeout(function()
			{
				document.body.style.transition = oldTransition;
			}, 100);
		}

		localStorage.setItem("theme_toggle", state ? "true" : "false");
	}

    setupOnNode.querySelector(".theme-toggle-input")?.addEventListener("change", event =>
	{
		console.log("Theme toggle changed to: " + !(localStorage.getItem("theme_toggle") == "true"));
		setThemeToggle(!(localStorage.getItem("theme_toggle") == "true"));
	});

    // window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => 
	// {
	// 	// return if we are printing
	// 	if (window.matchMedia('print').matches)
	// 	{
	// 		printing = true;
	// 		return;
	// 	}

    //     let newColorScheme = event.matches ? "theme-dark" : "theme-light";

	// 	if (newColorScheme == lastScheme) return;

    //     if (newColorScheme == "theme-dark")
    //     {
	// 		setThemeToggle(false);
    //     }

    //     if (newColorScheme == "theme-light")
    //     {
	// 		setThemeToggle(true);
    //     }

	// 	lastScheme = newColorScheme;
    // });

}

function setupHeaders(setupOnNode)
{
    // MAKE HEADERS COLLAPSIBLE
	setupOnNode.querySelectorAll(".heading-collapse-indicator").forEach(function (element) 
	{
		element.addEventListener("click", function () 
		{
			var isOpen = !this.parentElement.parentElement.classList.contains("is-collapsed");
			setHeaderOpen(this.parentElement.parentElement, !isOpen);
		});
	});

	// unfold header when an internal link that points to that header is clicked
	setupOnNode.querySelectorAll("a.internal-link, a.tree-item-link").forEach(function (element) 
	{
		element.addEventListener("click", function (event) 
		{
			event.preventDefault();
			let target = this.getAttribute("href");

			// if the target is a header uncollapse it
			if (target.startsWith("#")) 
			{
				console.log("Uncollapsing header: " + target);
				let header = document.getElementById(target.substring(1));
				setHeaderOpen(header.parentElement, true);
			}
		});
	});
}

function setupTrees(setupOnNode) 
{
	const fileTreeItems = Array.from(setupOnNode.querySelectorAll(".tree-container.file-tree .tree-item"));

    setupOnNode.querySelectorAll(".tree-item-contents > .collapse-icon").forEach(function(item)
	{
		item.addEventListener("click", function()
		{
			toggleTreeCollapsed(item.parentElement.parentElement);
		});
	});

	let fileTreeCollapse = setupOnNode.querySelector(".tree-container.file-tree .collapse-tree-button");
	if (fileTreeCollapse) fileTreeCollapse.addEventListener("click", async function()
	{
		let fileTreeIsCollapsed = fileTreeCollapse.classList.contains("is-collapsed");
		
		setTreeCollapsedAll(fileTreeItems, !fileTreeIsCollapsed, fileTreeItems.length < 100);

		fileTreeCollapse.classList.toggle("is-collapsed");
		fileTreeCollapse.querySelector("iconify-icon").setAttribute("icon", fileTreeIsCollapsed ? "ph:arrows-out-line-horizontal-bold" : "ph:arrows-in-line-horizontal-bold");
	});


	let outlineTreeCollapse = setupOnNode.querySelector(".tree-container.outline-tree .collapse-tree-button");
	if(outlineTreeCollapse) outlineTreeCollapse.addEventListener("click", async function()
	{
		let outlineTreeIsCollapsed = outlineTreeCollapse.classList.contains("is-collapsed");

		let items = Array.from(outlineTreeCollapse.parentElement.parentElement.querySelectorAll(".tree-item"));
		setTreeCollapsedAll(items, !outlineTreeIsCollapsed, items.length < 100);

		outlineTreeCollapse.classList.toggle("is-collapsed");
		outlineTreeCollapse.querySelector("iconify-icon").setAttribute("icon", outlineTreeIsCollapsed ? "ph:arrows-out-line-horizontal-bold" : "ph:arrows-in-line-horizontal-bold");
	});
	
	// start with all closed
	setupOnNode.querySelectorAll(".tree-container .tree-item").forEach(function(item)
	{
		if (item.classList.contains("is-collapsed")) setTreeCollapsed(item, true, false);
	});

	// make sure the icons match their starting collaped state
	setupOnNode.querySelectorAll(".tree-container > .tree-header > .collapse-tree-button").forEach(function(item)
	{
		if (item.classList.contains("is-collapsed"))
		{
			item.querySelector("iconify-icon").setAttribute("icon", "ph:arrows-out-line-horizontal-bold");
		}
		else
		{
			item.querySelector("iconify-icon").setAttribute("icon", "ph:arrows-in-line-horizontal-bold");
		}
	});
}

function setupCallouts(setupOnNode)
{
	// MAKE CALLOUTS COLLAPSIBLE
    // if the callout title is clicked, toggle the display of .callout-content
	setupOnNode.querySelectorAll(".callout.is-collapsible .callout-title").forEach(function (element) 
	{
		element.addEventListener("click", function () 
		{
			var parent = this.parentElement;
			var isCollapsed = parent.classList.contains("is-collapsed");

			parent.classList.toggle("is-collapsed");
			element.querySelector(".callout-fold").classList.toggle("is-collapsed");

			slideToggle(parent.querySelector(".callout-content"), 100);
		});
	});

}

function setupCheckboxes(setupOnNode)
{
	// Fix checkboxed toggling .is-checked
	setupOnNode.querySelectorAll(".task-list-item-checkbox").forEach(function (element) 
	{
		element.addEventListener("click", function () 
		{
			var parent = this.parentElement;
			parent.classList.toggle("is-checked");
			parent.setAttribute("data-task", parent.classList.contains("is-checked") ? "x" : " ");
		});
	});

	setupOnNode.querySelectorAll(`.plugin-tasks-list-item input[type="checkbox"]`).forEach(function(checkbox)
	{
		checkbox.checked = checkbox.parentElement.classList.contains("is-checked");
	});

	setupOnNode.querySelectorAll('.kanban-plugin__item.is-complete').forEach(function(checkbox)
	{
		checkbox.querySelector('input[type="checkbox"]').checked = true;
	});
}

function setupCanvas(setupOnNode)
{
	let focusedNode = null;

	// make canvas nodes selectable
	setupOnNode.querySelectorAll(".canvas-node-content-blocker").forEach(function (element) 
	{
		element.addEventListener("click", function () 
		{
			var parent = this.parentElement.parentElement;
			parent.classList.toggle("is-focused");
			this.style.display = "none";

			if (focusedNode) 
			{
				focusedNode.classList.remove("is-focused");
				focusedNode.querySelector(".canvas-node-content-blocker").style.display = "";
			}

			focusedNode = parent;
		});
	});

	// make canvas node deselect when clicking outside
	// document.addEventListener("click", function (event) 
	// {
	// 	if (!event.target.closest(".canvas-node")) 
	// 	{
	// 		document.querySelectorAll(".canvas-node").forEach(function (node) 
	// 		{
	// 			node.classList.remove("is-focused");
	// 			node.querySelector(".canvas-node-content-blocker").style.display = "";
	// 		});
	// 	}
	// });

}

function setupCodeblocks(setupOnNode)
{
	// make code snippet block copy button copy the code to the clipboard
	setupOnNode.querySelectorAll(".copy-code-button").forEach(function (element) 
	{
		element.addEventListener("click", function () 
		{
			var code = this.parentElement.querySelector("code").textContent;
			navigator.clipboard.writeText(code);
			this.textContent = "Copied!";
			// set a timeout to change the text back
			setTimeout(function () 
			{
				setupOnNode.querySelectorAll(".copy-code-button").forEach(function (button) 
				{
					button.textContent = "Copy";
				});
			}, 2000);
		});
	});
}

function setupLinks(setupOnNode)
{
	setupOnNode.querySelectorAll(".internal-link, .footnote-link, .tree-item-link").forEach(function(link)
	{
		link.addEventListener("click", function(event)
		{
			let target = link.getAttribute("href");
			event.preventDefault();

			// this is linking to a different page
			if (!target.startsWith("#"))
			{
				// load doc, if it is a tree link then don't scroll to the active doc in the file tree
				loadDocument(target, true, !link.classList.contains("tree-item-link"));
				return;
			}
			else
			{
				let headerTarget = document.getElementById(target.substring(1));
				setHeaderOpen(headerTarget.parentElement, true);
				headerTarget.scrollIntoView();
			}
		});
	});

    window.onpopstate = function(event)
    {
		loadDocument(getURLPath(), false);
    }
}


let sidebarWidth = undefined;
let lineWidth = undefined;
function setupResize(setupOnNode)
{
	if (setupOnNode != document) return;

	function updateSidebars()
	{
		let rightSidebar = document.querySelector(".sidebar-right");
		let leftSidebar = document.querySelector(".sidebar-left");
		let sidebarCount = (rightSidebar ? 1 : 0) + (leftSidebar ? 1 : 0);

		if (sidebarCount == 0) return;

		if(!sidebarWidth) sidebarWidth = Math.max(rightSidebar?.clientWidth, leftSidebar?.clientWidth);

		if (!lineWidth)
		{
			let docWidthTestEl = document.createElement("div");
			document.querySelector(".markdown-preview-view").appendChild(docWidthTestEl);
			docWidthTestEl.style.width = "var(--line-width)";
			docWidthTestEl.style.minWidth = "var(--line-width)";
			docWidthTestEl.style.maxWidth = "var(--line-width)";
			lineWidth = docWidthTestEl.clientWidth;
			docWidthTestEl.remove();
		}

		let letHideRightThreshold = sidebarWidth * sidebarCount + lineWidth / 2;

		if (window.innerWidth < letHideRightThreshold)
		{
			rightSidebar.style.display = "none";
		}
		else
		{
			rightSidebar.style.display = "";
		}

		let letHideLeftThreshold = lineWidth / 2 + sidebarWidth;

		if (window.innerWidth < letHideLeftThreshold)
		{
			leftSidebar.style.display = "none";
		}
		else
		{
			leftSidebar.style.display = "";
		}
	}

	window.addEventListener("resize", function()
	{
		updateSidebars();
	});

	updateSidebars();
}

function setupRootPath(fromDocument)
{
	let basePath = fromDocument.querySelector("#root-path").getAttribute("root-path");
	document.querySelector("base").href = basePath;
	document.querySelector("#root-path").setAttribute("root-path", basePath);
	rootPath = basePath;
}

let touchDrag = false;

function initializePage(setupOnNode)
{
    setupThemeToggle(setupOnNode);
    setupHeaders(setupOnNode);
    setupTrees(setupOnNode);
	setupCallouts(setupOnNode);
	setupCheckboxes(setupOnNode);
	setupCanvas(setupOnNode);
	setupCodeblocks(setupOnNode);
	setupLinks(setupOnNode);
	setupResize(setupOnNode);

	setupOnNode.querySelectorAll("*").forEach(function(element)
	{
		element.addEventListener("touchend", function(event)
		{
			if (touchDrag)
			{
				touchDrag = false;
				event.stopPropagation();
				return;
			}

			if (element instanceof HTMLElement) element.click();
		});
	});

	if(setupOnNode == document) 
	{
		document.body.addEventListener("touchmove", function(event)
		{
			event.stopImmediatePropagation();
			touchDrag = true;
		});

		setupRootPath(document);
		setActiveDocument(getURLPath());
	}
}

function initializeForFileProtocol()
{
	let graphEl = document.querySelector(".graph-view-placeholder");
	if(graphEl)
	{
		console.log("Running locally, skipping graph view initialization and hiding graph.");
		graphEl.style.display = "none";
		graphEl.previousElementSibling.style.display = "none"; // hide the graph's header
	}
}

//#endregion

window.onload = function()
{
	if (window.location.protocol == "file:") initializeForFileProtocol();
	initializePage(document);
}
</script>



</head><body class="theme-dark mod-windows is-frameless is-hidden-frameless obsidian-app show-inline-title show-view-header is-maximized" style="--zoom-factor:1; --font-text-size:16px; --line-width:50em; --line-width-adaptive:50em; --file-line-width:50em; --content-width:1200px; --sidebar-width:25em; --collapse-arrow-size:0.4em; --tree-horizontal-spacing:1em; --tree-vertical-spacing:0.5em; --sidebar-margin:12px;"><div class="webpage-container"><div class="sidebar-left sidebar"><div class="sidebar-content"><div><label class="theme-toggle-container" for="theme_toggle"><input class="theme-toggle-input" type="checkbox" id="theme_toggle"><div class="toggle-background"></div></label></div></div></div><div class="document-container"><div class="markdown-preview-view markdown-rendered node-insert-event is-readable-line-width allow-fold-headings show-indentation-guide allow-fold-lists" style="tab-size: 4;"><style id="MJX-CHTML-styles"></style><div class="markdown-preview-sizer markdown-preview-section" style="padding-bottom: ; padding-top: var(--file-margins); padding-right: var(--file-margins); padding-left: var(--file-margins); width: 100%; position: absolute;"><div class="markdown-preview-pusher" style="width: 1px; height: 0.1px; margin-bottom: 0px;"></div><div class="mod-header"><div class="inline-title" contenteditable="true" spellcheck="false" tabindex="-1" enterkeyhint="done">Configuring Tor Browser for Proxy Server Country Exclusion</div></div><div>
