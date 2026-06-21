# Bug Report: Price Tag Overlaps Tariff Card Text on Mobile Viewports (iPhone SE)

**Status:** Open  
**Severity:** Medium  
**Priority:** Medium  
**Environment:** Urban Routes Web App - Mobile Safari Sim (Viewport: 375x667)

### 📝 Description
When shrinking the viewport to small mobile screens (e.g., iPhone SE/Android small), the price badge element in the "Confort" or "Flash" tariff options overlaps the descriptive text below it. This makes the tariff price illegible for users on smaller screens.

### 🔄 Steps to Reproduce
1. Open Urban Routes in Chrome or Safari.
2. Open Developer Tools (F12) and toggle the Device Toolbar.
3. Select **iPhone SE** (or set viewport width to `375px`).
4. Select a Route to trigger the Tariff selection card component.
5. Observe the text formatting inside the "Confort" tariff button.

### ❌ Actual Result
The text element indicating the price (`$15 USD`) shifts downward and overlaps the text wrapper containing the tariff description ("Includes blanket and tissues"), causing a collision of fonts.

###  Expected Result
The card layout should adjust dynamically using CSS Flexbox/Grid (or media queries) to stack the price above or below the text, or scale down the font size to prevent overlapping.

### 📌 Environment Specifications
* **Tested Breakpoint:** 375px width
* **Affected Browsers:** Chrome Mobile, Safari iOS
