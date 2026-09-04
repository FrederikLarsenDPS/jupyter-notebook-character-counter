# Jupyter Notebook Character Counter

[Open the counter](https://frederiklarsendps.github.io/jupyter-notebook-character-counter/)

A single-file, browser-based counter for rendered markdown and code-cell inputs in Jupyter HTML exports. The supplied demo is published unchanged as `index.html`.

## Course limits

The course allows **10 standard pages of markdown and 10 standard pages of code**, assessed separately. At 2,400 characters per page, the limits are:

- Markdown: **24,000 characters**.
- Code: **24,000 characters**.

Divide each character count by 2,400 to obtain its page equivalent. The demo reports character totals; it does not display page equivalents or automatic over-limit warnings.

## Use

1. Export your Jupyter notebook as an HTML (`.html`) file.
2. Open the counter link above.
3. Choose your exported file or drag it into the drop zone.
4. Compare each total with its separate 24,000-character limit.

No installation or sign-in is required. The counter reads the selected file in the browser and has no server-side upload endpoint or analytics.

## Counting behavior

- Counts Unicode code points in each selected cell's DOM `textContent`, including spaces and line breaks present in that text.
- Counts rendered markdown separately from code-cell inputs.
- Excludes HTML tags and attributes, markdown heading permalinks, execution prompts, code-cell outputs, and images.
- Supports exports using the JupyterLab-style `.jp-MarkdownCell .jp-MarkdownOutput` and `.jp-CodeCell .jp-InputArea-editor pre` selectors. Other export templates, including classic notebook templates, may not be recognized.
- Counts rendered text rather than original Markdown source syntax. HTML-export formatting whitespace may affect totals.

## Maintenance

GitHub Pages serves `index.html` from the root of the `main` branch. Update that file on `main` to publish changes automatically. `.nojekyll` disables Jekyll processing. There are no build dependencies.

Only the counter and its documentation are stored in this repository; no course or student notebook is included.
