# Minimal manuscript viewer

## Using the Manuscript Viewer

This Digital Manuscript Viewer allows you to explore medieval manuscripts with synchronized text transcriptions and OCR data.

### Navigation

- **Read me**: View the project README and documentation
- **Guidelines**: View these usage guidelines
- **Citation**: Citation information for this project
- **Manuscripts**: Browse available manuscripts
- **Reader**: View and interact with manuscript pages

### Viewing a Manuscript

1. Navigate to the **Manuscripts** tab
2. Click on a manuscript card to open it in the **Reader** tab
3. Select a page from the left sidebar to view it

### Interacting with Pages

#### Text and Image Synchronization
- Click on any line in the transcription (right panel) to highlight its corresponding text region in the image
- Hover over text regions in the image to see the transcribed text highlighted
- The view will automatically pan to show the highlighted region when clicking from the text panel

#### Toggling Polygons
- Use the **Show Polygons** checkbox to display/hide the OCR text region boundaries
- When enabled, text regions are outlined with light blue polygons
- Highlighted regions appear in orange

#### Zooming and Panning
- Scroll to zoom in/out smoothly
- Click and drag to pan around the manuscript page
- Zoom steps are incremental for precise control

### Text Display

The transcription panel shows text organized by text regions:
- Each line is numbered for reference
- Line numbers correspond to the order they appear on the page
- Text is extracted from the PageXML OCR data

### File Formats

This viewer works with:
- **METS.xml**: Contains metadata and file references for manuscript pages
- **PageXML**: Contains OCR text and text region coordinates
- **JPEG/PNG images**: High-resolution scans of manuscript pages
- **CSV manifest**: Contains manuscript metadata and folder locations

### Tips

- For large manuscripts, loading may take a moment on first access
- The viewer works best in modern browsers (Chrome, Firefox, Safari, Edge)
- Manuscript data is loaded from the server on demand

---

For more information, see the README file or contact the project maintainers.