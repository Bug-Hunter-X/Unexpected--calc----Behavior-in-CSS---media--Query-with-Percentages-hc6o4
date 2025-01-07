# Unexpected calc() Behavior in CSS @media Query with Percentages

This repository demonstrates an uncommon issue related to the CSS `calc()` function when using percentage units within a `@media` query. The percentage calculation is relative to the parent element's width, not the viewport width, which can lead to unexpected results.

## Problem

The `calc()` function is used to dynamically calculate lengths. However, the percentage unit within `calc()` within a `@media` query behaves unexpectedly. It's relative to the parent container's width, not the viewport's width. This creates a discrepancy when the parent's width is smaller than the viewport's width.

## Solution

To address this, instead of relying solely on percentage units within `calc()`, it's recommended to either:

1.  Use viewport units (e.g., `vw`) to calculate width relative to the viewport, or
2.  Ensure the parent container occupies the full viewport width.

The solution example utilizes viewport units to achieve the desired layout.