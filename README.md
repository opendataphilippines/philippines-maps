# Philippines Maps (SVG Dataset)

This repository contains **vector maps of the Philippines** in SVG format, organized hierarchically by **region → province → city/municipality → barangay**.

The goal is to provide clean, editable, and programmatically usable maps for visualization, calamity tagging, data dashboards, or research.

## 📂 Directory Structure

```
philippines-maps/
├─ README.md
├─ /_shared/ # palettes, styles, metadata
│ ├─ palette.gpl # calamity severity colors
│ ├─ style.css # shared SVG styles
│ └─ metadata.json # lookup codes & names
├─ /overview/
│ ├─ philippines-regions.svg
│ └─ philippines-provinces.svg
├─ /r01-ilocos/
│ ├─ r01-overview.svg
│ └─ provinces/
│   └─ ph-pangasinan/
│     ├─ ph-pangasinan.svg
│     └─ cities/
│       ├─ ph-manaoag.svg
│ 		└─ ph-mapandan.svg
└─ /r07-central-visayas/
  ├─ r07-overview.svg
  └─ provinces/
    └─ ph-cebu/
      ├─ ph-cebu.svg
      └─ cities/
        ├─ ph-bantayan.svg
        ├─ ph-madridejos.svg
        └─ ph-santa-fe.svg
```

## 🏷️ Naming Conventions

- **Regions:** `rXX-name` (e.g., `r01-ilocos`, `r07-central-visayas`)  
- **Provinces:** `ph-<province>` (e.g., `ph-pangasinan`, `ph-cebu`)  
- **Cities/Municipalities:** `ph-<name>.svg` (e.g., `ph-manaoag.svg`, `ph-bantayan.svg`)  
- **Barangays:** `ph-<city>-brgy-<barangay>.svg`  

**SVG IDs**
- Provinces: `province-PH-CEB`  
- Cities/Municipalities: `mun-PH-072226` (PSA code if available)  
- Barangays: `brgy-PH-072226-0123`

# 🎨 Colors

The `/shared/palette.gpl` defines standard calamity severity levels:

- 🟩 Green — Not Affected  
- 🟨 Yellow — Slightly Affected  
- 🟧 Orange — Moderately Affected  
- 🟥 Red — Severely Affected  
- 🟪 Purple — Critical  

## 💻 Usage Example

Embed an SVG and color programmatically:

```html
<object type="image/svg+xml" data="r07-central-visayas/provinces/ph-cebu/ph-cebu.svg"></object>

<script>
  // Example: color Cebu City red
  const el = document.querySelector('#mun-PH-072226'); 
  if (el) el.style.fill = '#F44336';
</script>
```

## 📌 Sources
Traced from official reference maps (PhilGIS, PSA shapefiles, NAMRIA).

Processed and simplified manually in Inkscape.

## 📜 License
Free for personal, academic, and research use.

For commercial projects, please attribute and check underlying data sources.

---

# OpenDataPH Maps

Here's our attempt to open source (possibly) all maps of the Philippines to SVG format. This should be helpful when creating an application that use maps and can be manipulated to your needs.

## Contribute

For now, you can message us through our Facebook page, https://www.facebook.com/opendataphilippines We might create a Community/Group there if we get more traction. Thank you!

## Donate

Bitcoin Address: 3CrkyfB5pz86kJCqy7bYqgvNnBkNNfuAZ6

![Bitcoin Address](https://chart.apis.google.com/chart?cht=qr&chs=300x300&chl=3CrkyfB5pz86kJCqy7bYqgvNnBkNNfuAZ6)
