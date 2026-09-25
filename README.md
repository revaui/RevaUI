# Reva UI

A modern, native-web UI framework. HTML and CSS first. No JavaScript required by the core and no consumer build step required.

## Status

Reva UI 0.36 — Accessibility acceptance hardening. Core is feature-frozen; the static WCAG-oriented gate passes 51/51 checks while browser/manual acceptance remains explicitly pending.

## Principles

- Native HTML/CSS first
- Progressive enhancement
- WCAG 2.2 AA acceptance target
- Container-first responsive components
- Direction-independent LTR/RTL core
- Zero production dependencies for Reva Core
- MIT licensed

## Monorepo

- `packages/core` — canonical CSS framework
- `packages/icons` — SVG icon system
- `packages/js` — optional vanilla-JS enhancements
- `packages/react`, `vue`, `svelte` — framework adapters
- `tokens` — typed, standards-compatible design-token source
- `docs`, `examples`, `tests`, `tooling`, `labs`


## Foundation 0.3

Added the first production layout layer (`l-stack`, `l-cluster`, `l-grid`, `l-sidebar`, `l-split`, `l-center`, `l-cover`), container infrastructure, accessibility/print utilities, logical spacing helpers, and a deliberately curated responsive utility set.

## 0.4.0 — Button vertical slice

The first production component is now implemented in `packages/core/src/components/button.css` with contextual variants, five sizes, outline/ghost/link/gradient treatments, native disabled state, ARIA/Reva loading states, icon buttons, groups, density/theme/RTL compatibility, reduced-motion behavior, forced-colors support, and public component tokens. See `docs/button.html` for the smoke-test/demo.


## 0.7 Surfaces & Content
Cards, panels, wells, badges, chips, avatars, dividers and reusable content-state patterns are now included.

## 0.11 Tables & Data Presentation
Semantic tables now support striped, hover, bordered, borderless, compact and comfortable presentation; numeric cells; selected rows; sortable-header states; sticky headers/columns; responsive scrolling; opt-in container-aware stacking; and higher-level data-table toolbar/footer composition.


## 0.13 — Application Shell & Dashboard

Adds app shell, sidebar/topbar/workspace composition, toolbars, 12-column dashboard composition and widget containers.

## 0.14 — Sidebar & Advanced Navigation

Adds structured sidebar sections/groups, collapsible navigation presentation, nav rail behavior, secondary navigation, and safe-area-aware mobile bottom navigation with responsive application-shell integration.

## 0.15 — Toolbar, Filters & Search Patterns

Adds page headers, command/filter bars, search-field composition, active filter chips, bulk-action presentation, view controls and container-aware responsive command patterns.

### 0.16.0 — Metrics & Visualization Foundation
Adds metric cards, comparison/trend presentation, CSS bar visualizations, ring/donut presentation, sparklines, legends, and chart containers. Reva provides presentation and accessibility structure; applications/charting libraries own data and plotting logic.

### 0.17.0 — Stepper, Progress & Workflow Patterns
Adds responsive steppers, vertical process workflows, wizard composition, and compact status flows. Native/ARIA/Reva state contracts distinguish complete, current, pending, and error states without requiring JavaScript.

### 0.18.0 — Media & Content Presentation
Adds responsive media objects, aspect-ratio frames, semantic figures, galleries, thumbnails, image cards, media placeholders, and native `<dialog>` lightbox presentation. Reva owns presentation; application content and media behavior remain application-controlled.

### 0.20.0 — Profile, User & Identity Patterns
Adds presence-aware avatars, identity blocks, user rows, profile cards/headers, profile statistics, team/member cards, and account-menu composition. Patterns use semantic/ARIA state where applicable and remain density-, RTL-, container-, and forced-colors-aware.

## 0.20 marketing patterns

Hero sections, feature grids, pricing cards, testimonials, logo clouds, comparison wrappers and CTA compositions are included in the core presentation layer.

### 0.22 — Settings & Preferences
Adds responsive settings layouts, settings navigation, grouped preference rows, account/security patterns, destructive-action zones, and settings action bars.


### 0.22 Authentication & onboarding
Authentication shells, sign-in/registration/reset compositions, verification-code layouts, provider actions, and onboarding progress/choice patterns.

### 0.24 — Notifications & Messaging
Adds notification centers/items, unread state, inbox/message rows, conversation layouts, message bubbles, composers, system messages and typing presentation. Reva owns presentation and state contracts; applications own transport, persistence and messaging logic.


## 0.24 — File & Upload Presentation
File browser/list/grid patterns, upload queues, drag/drop presentation, attachments, storage meters, progress/error/success states. Upload logic remains application-owned.

### 0.25 — Commerce & Transaction Patterns
Adds product/order rows, cart and checkout composition, order/payment summaries, quantity controls, transaction lists, payment-method presentation, invoices and printable receipts. Reva owns presentation; applications own pricing, payments, tax, inventory and transaction logic.

### 0.28 — Rating, Selection & Choice Patterns
Adds native-input selectable cards and choice grids, read-only/interactive rating presentation, reactions, and voting controls. Reva owns presentation and state contracts; applications own persistence, scoring, and business logic.

## 0.29 Core Audit & Hardening

0.29 pauses component expansion to validate Core against the frozen architecture. It fixes public token naming drift, completes missing semantic token aliases, verifies all Reva custom-property references resolve or provide fallbacks, and adds modular CSS distribution exports. Calendar and other advanced application modules remain outside Core.


## 0.30 — Core Scope Gap Analysis

Core expansion is now bounded against the frozen v1 architecture. The remaining feature gaps are button/action completion, toast presentation, responsive navbar/mega-menu/hover-card compositions, a forms completeness pass, and explicit completion of reusable content states. Advanced modules such as Calendar, Scheduler, Kanban, Gantt and Charts remain outside Core. See `docs/core-scope-0.30.md`.


### 0.32 — Toast & Transient Feedback
Adds safe-area-aware toast regions, semantic success/info/warning/error toast presentation, actions and dismiss controls, density integration, reduced-motion/reduced-transparency behavior, and forced-colors support. Core deliberately does not implement automatic dismissal timers; applications own toast lifecycle and choose appropriate live-region semantics.

### 0.33 — Navigation Completion
Adds native-details responsive navbar composition, mega-menu and hover/focus-card patterns, plus `glide` navigation. Glide has a CSS-only fallback; the optional `@reva/js` `GlideNavigation` enhancement moves one indicator between hovered/focused items and restores it to the active item. Reduced motion removes travel animation.


### 0.34 — Forms Completeness Audit & Completion
Closes the bounded Forms Core gap: textarea sizing now follows the shared five-size control scale; choice groups, responsive horizontal fields and form grids are formalized; loading/busy presentation is control-relative and reduced-motion safe; forced-colors checked states are hardened; and `.select.customizable` adds a progressive native customizable-select path with a normal native fallback. See `docs/forms-audit-0.34.md` and `docs/forms-complete.html`.

### 0.35 — Content States Completion & Core Feature Freeze
Completes the reusable content-state family with explicit empty/default, no-results, error, success, offline, permission-required and maintenance presentations plus compact composition and public component tokens. Accessibility semantics remain application-controlled so live-region urgency matches the actual event. This closes the bounded feature gaps from the 0.30 Core scope audit; Core now enters feature freeze and moves to hardening/testing/documentation rather than new feature families.


### 0.36 — Accessibility Acceptance Audit
Hardens the feature-frozen Core against the WCAG 2.2 AA acceptance contract. Adds explicit increased-contrast behavior and a 24px target token, corrects official semantic/gradient contrast relationships, tightens compact action targets, improves reduced-motion and ARIA-disabled behavior, and audits accessible names across the demos. The automated/static gate passes 51/51 checks. This is not yet a claim of full WCAG conformance; browser, keyboard, screen-reader, zoom/reflow, touch and visual acceptance remain pending. See `docs/accessibility-acceptance-0.36.md`.
