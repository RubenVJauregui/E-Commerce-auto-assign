# E-Commerce Auto-Assign Instructions

These are the current business instructions being used/discussed for E-Commerce / Dropship auto-assignment. This document is informational only; it does not execute WMS mutations by itself.

## Scope

Target Bay 2 / E-Commerce dropship work only.

## Eligibility Filters

Only include WMS outbound orders/pick work where all of the following are true:

1. **Order Type** is Dropship Order / DS.
2. Customer is in the configured E-Commerce customer list for the applicable side:
   - Bay 2 left-side E-Commerce customer list.
   - Bay 2 right-side Mezzanine customer list.
3. Order or pick work is still operationally eligible.
4. Do not include completed, closed, cancelled, shipped, or otherwise ineligible work.
5. Do not assign work that already has an active assignment unless the workflow explicitly allows reassignment.

## Left-Side Bay 2 Dropship Customers

- AMZN PREP - MATTRESSES
- AMZN PREP - RGS
- AS EVER ENTERPRISES, LLC
- BABYARK INC
- BOUNDLESS EC US LLC
- DELTA ELECTRONICS
- DUPRAY USA LLC
- ELEVATE BRANDS OPCO LLC
- NET HEALTH SHOPS LLC
- NZXT
- PRISMA INTERNATIONAL LLC
- RIO ROUTER INC
- ROAR BEVERAGES INC
- SIMPLE MODERN
- SLINGER BAG AMERICAS INC.
- STRETTON ONLINE LTD
- SUN NINJA LLC
- THE MURRIETA RHINO HOLDCO LLC
- TINYYO LIMITED
- TORQUAY ETRADING LLC
- TRIPLELITE, LLC
- UNIVERA BRANDS

## Right-Side Mezzanine Dropship Customers

- MAMMA CHIA
- THE FEELIST
- OPAL CAMERA
- BIRD OF CONDOR
- BUMP
- FLAG AND ANTHEM
- VAONIS
- EMBER
- VITA COCO DTC
- COME READY
- PUNK BUNNY
- THE OUAI
- BYTE DANCE - TIKTOK
- ZEN
- RECOVERY
- MUSE
- RISEANDSHINE
- WATERPLUS
- UPTIME ENERGY
- FHIRST
- KACE TEA
- SPLENDOR WATER

## Assignment Safeguards

Before any live assignment mutation:

1. Resolve customer names to WMS customer IDs/org IDs.
2. Resolve assignee names/usernames to WMS user IDs.
3. Confirm the pick task/order status is assignable.
4. Confirm the endpoint and request schema for wave, batch-pick, or assignment creation.
5. Confirm the success response and rollback/retry behavior.
6. Do not execute any mutation unless explicitly approved.

## Operational Rule

The dashboard may display eligible work, counts, and prepared queues, but real WMS actions such as wave creation, batch pick creation, or picker assignment must be treated as live mutations and require explicit confirmation.

## Current Dashboard Behavior

The live Valley View dashboard should only display/filter the eligible dropship work for these customer lists unless a separate confirmed mutation workflow is requested.
