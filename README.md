# Smiling Coast: A Travel Guide to The Gambia

**Author:** Emmanuel Adenuga
**Course:** Web Programming 1, CSS Grid and Flexbox Website Project

A small, responsive two-page travel guide for first-time visitors to The Gambia, built with
semantic HTML and hand-written CSS only (no frameworks, templates or JavaScript).

- **Live site:** https://adeemma477.github.io/gambia-travel-guide/
- **Repository:** https://github.com/adeemma477/gambia-travel-guide

## Pages

| Page | Sections |
|---|---|
| `index.html` (Home) | Hero, Quick facts, Top destinations, Gallery, Travel tips + "Before you go" sidebar |
| `plan.html` (Plan your trip) | Introduction, 5-day itinerary, When to go (season table), Trip enquiry form |

## Folder structure

```
gambia-travel-guide/
├── index.html
├── plan.html
├── README.md
├── css/
│   └── styles.css
└── images/
    └── *.svg   (8 original illustrations)
```

## Where Grid and Flexbox are used

| Component | Layout method | Why |
|---|---|---|
| Hero (text + image) | **Grid**: 1 column → 2 columns at 64rem | Two regions side by side that should stack on phones |
| Destination cards | **Grid**: `repeat(auto-fit, minmax(16rem, 1fr))` | 2-D card layout that goes from 1 → 2 → 4 columns automatically |
| Gallery | **Grid**: wide images use `grid-column: span 2` | Rows *and* columns at the same time, with mixed image sizes |
| Travel tips | **Grid**: `grid-template-areas` ("intro intro" / "tips aside") | Named page regions with a sidebar on desktop that stack on mobile |
| Itinerary, enquiry form | **Grid** | Day cards in columns; form fields in 2 columns on wider screens |
| Navigation, header, footer | **Flexbox** | One row of items that needs spacing, alignment and wrapping |
| Quick facts, buttons, checkboxes | **Flexbox** with `flex-wrap` | Items in a row that wrap when space runs out |
| Inside each card | **Flexbox** (column) + `margin-top: auto` | Pushes the card footer to the bottom so cards line up |

## Responsive approach

- Mobile-first stylesheet: base styles are for phones; `min-width` media queries at **40rem** and **64rem** add more columns.
- `max-width` containers instead of fixed widths; `img { max-width: 100%; height: auto; }`.
- Relative units (`rem`) for fonts, spacing and breakpoints.
- Tested at 1366px (desktop) and 375px (phone), with no horizontal scrolling.

## Accessibility

Semantic elements (`header`, `nav`, `main`, `section`, `article`, `aside`, `figure`, `footer`),
a logical heading order, descriptive `alt` text, labelled form fields, a "skip to main content"
link, `aria-current` on the active nav link and a visible `:focus-visible` outline.

## Credits

All illustrations are original SVG artwork made for this project. Travel information is
general guidance only; check official sources before you travel.
