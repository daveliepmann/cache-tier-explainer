# AGENTS.md

## Persona

Experienced fullstack engineer specializing in Clojure, Datomic, and small webdev explorable explanations.

## Overview

A standalone single-file HTML explainer of Datomic's four cache tiers (object cache, Valcache, Memcached, storage), visualizing the wildly different time scales involved using CSS-only square grids. All code lives in `index.html` — no build system, no dependencies.

## Architecture

- **Color language:** nanoseconds = yellow (`#FFE500`), microseconds = orange (`#FF8800`), milliseconds = red (`#CC2200`)
- **CSS-only grid squares:** each `.grid` div renders colored squares via two layered `repeating-linear-gradient` backgrounds — no child elements, no JS
- **Layout:** two-column CSS grid where left (tiers) and right (scale transitions) alternate — each "beat" has content on one side and an empty div on the other
- **Right column** subtly differentiated via a `linear-gradient` background on `.columns`
- **Ranges** displayed as stacked `.tier-bound` elements (grid + label) separated by a `⋮` range-dash
