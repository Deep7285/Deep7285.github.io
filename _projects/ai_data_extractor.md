---
layout: page
title: AI Data Extractor
description: Web app pipeline combining GenAI and OCR to extract structured data from unstructured documents and scientific figures.
img: assets/img/data_extractor_1.png
importance: 1
category: side-projects
related_publications: false
---

Built a Full-stack web-based Gen-AI tool for a financial company to automate data extraction from a variety of complex documents. Users can upload PDFs, images, or DOCX files; an AI-powered pipeline extracts key fields (details, tax breakdown, etc.) and saves the results to a consolidated spreadsheet. The system processes data in memory and only holds it temporarily, and files are not stored to help protect privacy. The site is fully responsive across mobile, tablet, and desktop. The project emphasizes cost-effectiveness, with ongoing work on new features and further cost optimization. 

**Application Previews:**  
![Data Extractor UI](/assets/img/data_extractor_1.png)  
![Extracted Results View](/assets/img/data_extractor_2.png)  

#### What it does

- Accepts uploaded documents or images (PDFs, PNGs, scanned figures)
- Runs OCR to extract raw text and identify structured regions
- Uses a GenAI model to interpret and reformat extracted content into structured output
  (tables, key-value pairs, numerical data)
- Returns machine-readable output ready for further analysis
- limited free access
#### Why it's useful

For researchers dealing with legacy data locked in paper figures, or anyone trying to
aggregate information from heterogeneous document sources, manual extraction is the
bottleneck. This pipeline reduces that bottleneck without requiring domain-specific
training for each document type.

#### Stack

`Python` · `OCR (Tesseract / EasyOCR)` · `GenAI API` · `` · `Pandas`
`Vanilla HTML/CSS/JavaScript` . `Cloudflare Workers (serverless edge backend)` . `Cloudflare KV (user + session store)`. `Google Gemini Flash` .`vision OCR` . `pdf.js (client-side PDF to image conversion)` . `Mammoth.js (DOCX text extraction)` . `SheetJS (Excel generation in the browser)` . `Wrangler CLI (Cloudflare local dev + deploy)`

#### Links

- GitHub: [Deep7285/data-extractor](https://github.com/Deep7285/data-extractor)
- website:[deep7285.github.io/data-extractor/#extract](https://deep7285.github.io/data-extractor/#extract)