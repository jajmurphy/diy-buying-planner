# Patio Buying Planner MVP

A zero-backend, zero-paid-API static prototype for a UK DIY purchase-planning business.

## Run locally
Open `index.html` in a browser. No build step is required.

## Deploy free
Suitable for GitHub Pages, Cloudflare Pages or Netlify static hosting. No backend is required.

## Core logic
- Patio area = length x width
- Paving target = area x (1 + waste %)
- Sub-base compacted volume = area x depth
- Mortar theoretical volume = area x bed depth
- Mortar sand/cement split = selected volumetric ratio
- Paving pack optimiser searches integer combinations and minimises cost, then surplus, then pack count
- Other material package counts require user-entered product coverage/yield to avoid unsupported bulk-density assumptions

## Construction caveat
Defaults are editable planning assumptions based on manufacturer guidance, not universal instructions. Always follow the paving/product manufacturer's installation requirements and account for site conditions.
