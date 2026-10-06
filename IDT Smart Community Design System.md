# IDT Smart Community Design System

Calm, clean and friendly. A feed-first interface for residents and admins, with generous space, large type and big touch targets. Version 1.0 for the prototype build.

WCAG 2.1 AAMobile firstDesktop 1366–1440

## 1. Color

A harbor-teal primary gives calm and trust. Dusk indigo separates community content from personal content. Marigold is used sparingly for one highlight per screen. Everything else is soft neutrals. Contrast ratios are measured on the listed pairing.

**Harbor (primary)**`#1F6F78`\
White text 5.9:1 ✓

**Dusk (secondary)**`#4A4E9C`\
White text 7.4:1 ✓

**Marigold (accent)**`#F2B544`\
Ink text 9.1:1 ✓

**Ink (text)**`#14262B`\
On Mist 15:1 ✓

**Slate (muted text)**`#4A5E63`\
On white 6.6:1 ✓

**Mist (background)**`#F5F8F7`

**Surface**`#FFFFFF`

**Surface 2 / fill**`#EAF1F0`

**Line**`#D3DFDD`\
Decorative borders only

**Error**`#B3261E`\
On white 6.5:1 ✓

**Success**`#2E7D4F`\
On white 5.3:1 ✓

### Usage rules

| Color | Use for | Never for |
| --- | --- | --- |
| Harbor | Main action per screen, active nav, links, own message bubbles | Large background areas |
| Dusk | Community-wide content tags, admin badges, official announcements | Primary buttons |
| Marigold | One highlight: “Happening today” or a new-count badge | Text on white, more than once per screen |
| Error / Success | Validation and confirmation, always paired with an icon or text | Color as the only signal |

Dark mode tokens are included in this page's CSS (toggle your device theme). Harbor lifts to `#5CC0C9` and Dusk to `#A9ADF0` for contrast on dark surfaces.

## 2. Typography

**Bricolage Grotesque** for headlines: friendly, slightly quirky and distinct from generic social apps. **Figtree** for everything else: open, very readable at small sizes. Both are on Google Fonts. Fallbacks: Georgia, system-ui.

Good morning, Priya

Courtyard clean-up this Saturday

Rooftop garden volunteers needed

Join your neighbors on the roof terrace to plant herbs for the shared kitchen. Tools and snacks are provided; all ages welcome.

Posted by Block C committee · 2 hours ago

| Style | Font | Mobile / Desktop | Weight | Line height | Tracking |
| --- | --- | --- | --- | --- | --- |
| Display | Bricolage | 32 / 44 | 700 | 1.15 | -0.02em |
| Headline | Bricolage | 24 / 30 | 700 | 1.2 | -0.01em |
| Title | Figtree | 18 / 20 | 600 | 1.3 | 0 |
| Body | Figtree | 16 / 16 | 400 | 1.6 | 0 |
| Label | Figtree | 14 / 14 | 600 | 1.4 | 0.01em |
| Caption | Figtree | 13 / 13 | 500 | 1.4 | 0.01em |

Minimum text size is 13px, and only for captions. Keep line length under 70 characters. Use sentence case everywhere and avoid all-caps labels.

## 3. Layout & spacing

All spacing uses an 8px scale: `4 · 8 · 16 · 24 · 32 · 48 · 64`. Use 16 inside cards’ elements, 24 card padding on desktop, and 32+ between sections. When in doubt, add space instead of a divider.

**Mobile (\<768)**

Screen margin 16 · card gap 12 · card padding 16 · radius 16 · one column

**Tablet (768–1199)**

Margin 24 · card gap 16 · feed max 640 centered · icon-rail nav

**Desktop (≥1200)**

Margin 32 · 240px nav · feed 600–680 · 320px right rail · card padding 24

Radius: 12 inputs and images, 16 cards, 999 buttons and chips. One soft shadow only, for floating elements: `0 8px 24px rgba(20,38,43,.12)`. Cards otherwise rely on a 1px line border.

## 4. Components

### Buttons

Height 48px, 24px side padding, 16px/600 label. One primary button per screen.

States:

### Inputs

Height 48px, 12px radius, label always visible above the field. Outlined is the default; filled is for search and chat.

Outlined Filled Focused Error Add at least 10 characters so we can find the problem. Disabled

### Cards, chips and tags

### Content card

16px radius, 1px line border, 16–24px padding. Image on top when useful; one action at the bottom.

AllMaintenanceSafety

CommunityFor youToday

Chips filter (40px tall, 8px apart). Tags label (read-only).

## 5. Navigation

Same five destinations everywhere: Home, Calendar, Messages, Updates, Profile. Active state is Harbor color plus a bold label and a 3px indicator on mobile or a soft pill on desktop. The shape changes, the logic stays the same.

[Home](#nav)[Calendar](#nav)[Messages](#nav)[Updates](#nav)[Profile](#nav)

Mobile bottom bar: 64px tall, 24px icons, 11px labels, 48px+ targets

IDT Community

[Home](#nav)[Calendar](#nav)[Messages](#nav)[Updates](#nav)[Profile](#nav)

Desktop left nav: 240px at 1366+, 48px rows, icon plus 15px label, pill active state

## 6. Key screens

Mock data only illustrates appearance. Scroll sideways to see all six.

Tuesday, 6 October

#### Good morning, Priya

Announcement\
**Water off 10–12 tomorrow**\
Block C, for pipe repair.

Today **Yoga on the lawn**\
6:30 PM · Garden court

Report issueBook roomPay

AK

**Anil K.**\
Lost a grey cat near Block B…

Map preview

[Home](#screens)[Calendar](#screens)[Messages](#screens)[Updates](#screens)[Profile](#screens)

Home: greeting, announcement, next event, quick actions, posts, map, news

#### Calendar

OctMine

**Diwali potluck**Sat 17 Oct · 7 PM · Clubhouse

42 going

**Yoga on the lawn**\
Today · 6:30 PM

Calendar: event card with RSVP default and confirmed states

RS

**Ravi, Block C**

Is the lift fixed yet?

Technician arrives at 4 PM.

Thanks, I'll keep an eye out.

Messages: 18px bubbles, 4px tail corner, 80% max width

#### Updates

CommunityFor you

Community\
**Parking rules change Monday**

For you\
**Issue #214 is in progress**\
Lift repair · Block C

For you\
**Your RSVP is confirmed**

Updates: Dusk bar and tag for community, Harbor for personal

PN

#### Priya Nair

Unit 12B · Resident

**My unit**\
Block C, Floor 12

**Notifications**\
Events, issues, messages

Admin only\
**Manage residents**\
**Post announcement**\
**Review issues (8)**

Profile: resident view; the Dusk panel appears only for admins

#### Report an issue

LiftWaterNoiseOther

What's wrong?

**Add a photo**\
Tap to upload

Issue form: category chips, labeled field, photo drop area, one primary action

## 7. Responsive behavior

Desktop is a re-composed layout. The bottom bar becomes a left nav, the single column becomes a centered feed, and a right rail holds the calendar and map so they are no longer buried under the feed.

IDT Community

[Home](#responsive)[Calendar](#responsive)[Messages](#responsive)[Updates](#responsive)[Profile](#responsive)

#### Good morning, Priya

**Water off 10–12 tomorrow**

**Anil K.** Lost a grey cat near Block B…

**Ravi S.** Anyone up for badminton tonight?

Today\
**Yoga on the lawn**

Map preview

| Breakpoint | Layout |
| --- | --- |
| \< 768 | Single column, bottom nav, quick actions as horizontal chips |
| 768 – 1199 | Centered feed (max 640), 72px icon-only left rail |
| ≥ 1200 (target 1366–1440) | 240px labeled nav, 640px feed, 320px right rail, 1280 max container |

## 8. Motion

Motion confirms an action or shows what changed. It never decorates. Animate only `transform` and `opacity`, and honor `prefers-reduced-motion` by removing all movement.

| Moment | Behavior | Duration | Easing |
| --- | --- | --- | --- |
| Button press | Scale to 0.97 | 150ms | ease-out |
| Hover / focus | Background and shadow fade | 200ms | ease-out |
| Card reveal | Fade plus 8px rise, first load only | 250ms | cubic-bezier(.2,.8,.2,1) |
| Page change | Cross-fade, 12px slide on mobile | 300ms | ease-in-out |
| Modal / sheet | Sheet rises from bottom, backdrop fades | 300ms | cubic-bezier(.2,.8,.2,1) |
| Feed scroll | Native scroll, no parallax; skeleton cards while loading | n/a | n/a |

## 9. Accessibility

**Contrast**

Body text 4.5:1 or better, large text and UI components 3:1. Every pairing listed in section 1 passes AA.

**Touch targets**

48px minimum for buttons, inputs and nav items (44px absolute floor for compact RSVP). 8px minimum gap between targets.

**Focus**

3px Harbor outline with 3px offset on every interactive element. Never remove it. Tab order follows visual order.

**Meaning beyond color**

Errors use text plus a message; status uses a label; active nav uses weight and an indicator.

**Semantics**

Use `nav`, `main`, buttons for actions and links for navigation. Alt text on informative images, labels on all inputs.

**Scaling**

Use rem units. Layouts must survive 200% zoom with no horizontal scrolling.

## 10. Implementation notes

**Stack**

React + Vite, Tailwind CSS with tokens in `tailwind.config`, Radix UI primitives for modal, tabs and focus handling, lucide-react icons, Storybook for the component library.

**Tokens**

Define colors, spacing, radius and type as CSS variables (see this page's `:root`). Components read tokens only; no raw hex values in component code.

**Consistency**

Build each component once with variants and states in Storybook before using it on a screen. Review new screens against the spacing scale and one-primary-button rule.

**Handoff**

Export tokens as JSON, icons as SVG (24px, 2px stroke), and photos as WebP at 1x and 2x. Keep the Figma file's styles named to match the token names.

IDT Smart Community prototype, design system v1.0