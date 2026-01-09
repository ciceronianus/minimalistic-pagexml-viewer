# Minimal PageXML Viewer

A tiny, static viewer for datasets created with PAGE XML. It lets you publish and browse manuscripts directly from a GitHub repository via GitHub Pages—no server, no build step, just HTML + JSON.

## Purpose
- Make PAGE XML datasets easy to view and share on the web.
- Work entirely on GitHub Pages (or any static hosting).
- Discover pages from `mets.xml` (with JSON/CSV fallbacks), show the page image, transcription text, and optional region polygons.

## Quick Start (GitHub Pages)
1. Upload your data folders to the repository root (see Structure below).
2. Edit `manuscripts.json` to list your manuscripts (example below).
3. Enable GitHub Pages in your repo settings (Source: main branch, root).
4. Open your site (e.g., `https://<user>.github.io/<repo>/`) and pick a manuscript.

### Expected Structure per manuscript
```
<manuscriptFolder>/
	mets.xml                # preferred (Transkribus export works)
	# OR mets.json          # fallback: array of { image, pagexml }
	# OR mets.csv           # fallback: CSV [image,pagexml]
	page/
		<page-1>.xml
		<page-2>.xml
		...
	# images may be in the manuscript root or subfolders as referenced by METS
```

Images must be reachable via the paths referenced in `mets.xml` (or JSON/CSV). If your METS points to `p012.jpg`, place that image next to `mets.xml` or adjust paths consistently.

### `manuscripts.json` format
```json
[
	{
		"manuscriptFolder": "Chronicle_of_Dalimil",
		"title": "Chronicle of Dalimil - NKP XII E 17",
		"sourceUrl": "https://example.org/source",   
		"description": "Short description shown in the library grid."
	}
]
```

Fields:
- `manuscriptFolder`: folder name in this repo containing the manuscript files.
- `title`: label shown in the library.
- `sourceUrl`: optional link to the original source.
- `description`: short summary for users.

## Using the Viewer
- Library: pick a manuscript from the grid (data from `manuscripts.json`).
- Reader: see page image and PAGE XML text; navigate pages via the sidebar.
- Layout: toggle stacked/side‑by‑side and adjust panel sizes.
- Polygons: turn on “Show polygons” to overlay `TextRegion` polygons over the image.
- Docs in app: the About tab renders this README, `guidelines.md`, `viewer.md`, and `CITATION.cff`.

## Local Preview
Most browsers block `file://` fetches. Use a simple HTTP server from the repo root:

```bash
python3 -m http.server 8000
# then open http://localhost:8000/
```

## Examples
- [Late Medieval Latin Dataset](https://htr-school-vienna.github.io/2025--late-medieval-latin/)


## Sample Data
> Sample data prepared by the Late Medieval Latin Group in [Winter School: HTR of Historical Sources, 2025](https://www.oeaw.ac.at/imafo/das-institut/detail/htr-of-historical-sources). See the complete [dataset](https://github.com/HTR-School-Vienna/2025--late-medieval-latin).

#### Supervisors of the Late Medieval Group
- Jan Odstrčilík
- Zuzana Čermáková-Lukšová
- Annamária Kovács







