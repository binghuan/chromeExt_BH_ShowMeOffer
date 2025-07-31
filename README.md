# Show Me The Offer (Chrome Extension)

A Chrome extension that provides instant access to salary information and company reviews when browsing job posting websites in Taiwan.

## Overview

The concept is to show a messages board to talk about the company's salary and working status. It's designed for professionals who want to research companies and salary information when job hunting or considering career moves.

## Features

- **Multi-platform Support**: Works across major Taiwanese job search websites including:
  - 104.com.tw (台灣104人力銀行)
  - 1111.com.tw (1111人力銀行)
  - yes123.com.tw (yes123求職網)
  - 518.com.tw (518人力銀行)
  - ejob.gov.tw (台灣就業通)
  - LinkedIn
  - Glassdoor

- **Instant Salary Information**: Automatically detects company information on job posting pages and provides direct links to salary data on Glassdoor

- **Company Database**: Pre-loaded with 80+ major companies in Taiwan including:
  - Tech giants (TSMC, MediaTek, ASUS, HTC, Foxconn)
  - Foreign companies (Google, Microsoft, IBM, Intel, NVIDIA)
  - Consulting firms (Deloitte, PwC, KPMG, McKinsey)
  - And many more

- **Floating Interface**: Non-intrusive floating button that expands to show salary information in an embedded iframe

## How It Works

1. **Automatic Detection**: When you visit a supported job website, the extension automatically detects the company name and website
2. **Data Matching**: Matches the detected company against the pre-loaded database of companies
3. **Salary Button**: If a match is found, displays a floating "Show Me The Offer" button
4. **Instant Access**: Click the button to view salary information and company reviews in an embedded Glassdoor iframe

## Installation

1. Download or clone this repository
2. Open Chrome and navigate to `chrome://extensions/`
3. Enable "Developer mode" in the top right
4. Click "Load unpacked" and select the extension directory
5. The extension will be installed and ready to use

## Technical Details

- **Manifest Version**: 2
- **Permissions**: Access to job search websites, context menus, tabs, and storage
- **Technologies**: JavaScript, jQuery, Bootstrap CSS
- **Architecture**: Content scripts, background page, and message passing between components

## File Structure

```
├── manifest.json          # Extension configuration
├── data/
│   ├── background.js      # Background script for message handling
│   ├── content_script.js  # Main content script
│   ├── featureList.js     # Feature flags and constants
│   ├── preloadedData.js   # Company database
│   └── lib/
│       ├── utils.js       # Utility functions for company detection
│       ├── actionTable.js # Action definitions
│       └── jquery-1.11.0.min.js
└── icons/                 # Extension icons
```

## Supported Companies

The extension includes salary data links for 80+ companies including major Taiwanese and international corporations. The database covers companies across various industries:

- **Technology**: TSMC, MediaTek, ASUS, HTC, Foxconn, etc.
- **Software**: Google, Microsoft, IBM, Adobe, SAP, etc.
- **Consulting**: Deloitte, PwC, KPMG, McKinsey, etc.
- **Finance**: Morgan Stanley, J.P. Morgan, Citi, etc.
- **Manufacturing**: 3M, Applied Materials, Corning, etc.

## Privacy & Security

- No personal data collection
- Only accesses company information visible on job posting pages
- Uses existing public salary data from Glassdoor
- All processing happens locally in your browser

## Contributing

Feel free to contribute by:
- Adding more companies to the database
- Supporting additional job search websites
- Improving the UI/UX
- Reporting bugs or suggesting features

