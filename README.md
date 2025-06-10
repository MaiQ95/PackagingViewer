# PackagingViewer

## ⚠️ Local testing note

Due to browser security restrictions, this project may not work correctly if you open `index.html` directly from the filesystem (`file://...`). The `fetch()` call used to load `data.json` will be blocked by CORS policy.

### ✔ To test locally:

- Use a local web server (e.g. with [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension in VS Code)
- Or run a Python server:
  ```bash
  python -m http.server

**PackagingViewer** is a lightweight HTML + JavaScript application that dynamically renders packaging tables for multiple customers based on external JSON input. It is designed for internal or demo use cases where packaging instructions need to be displayed or printed in a structured form.

## Features

- Load packaging data from a JSON file
- Display packaging breakdown per customer and product
- Generate separate HTML tables for each product with calculated packages
- Support for last partial packages (`last_package`)
- Page-break layout for clean print separation per customer
- Basic styling via external CSS

## Technologies

- HTML5
- JavaScript (ES6+)
- External JSON file
- CSS (custom, print-friendly)
- [Optional data source] Microsoft Excel + Power Query

## JSON Structure (sample)

```json
{
  "packages": [
    {
      "Customer A": [
        {
          "item_name": "Item A",
          "full_packages": 2,
          "max_sheets": 3,
          "last_package": 2
        }
      ],
      "Customer B": [
        {
          "item_name": "Item B",
          "full_packages": 4,
          "max_sheets": 2,
          "last_package": 0
        }
      ]
    }
  ]
}