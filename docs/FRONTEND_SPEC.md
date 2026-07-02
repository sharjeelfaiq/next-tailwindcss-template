# Frontend Specification

## Document Control

| Field | Value |
| --- | --- |
| Project | {{ProjectName}} |
| Owner | {{DesignOrFrontendOwner}} |
| Status | {{Draft/In Review/Approved}} |
| Last updated | {{YYYY-MM-DD}} |

## Experience Goals

- {{Goal1Example: Make the primary workflow clear on first visit}}
- {{Goal2Example: Keep repeated tasks fast for returning users}}
- {{Goal3Example: Build mobile-first layouts that scale cleanly to desktop}}
- {{Goal4Example: Maintain accessible keyboard and screen-reader behavior}}

## Target Interfaces

| Interface | Audience | Primary task | Priority |
| --- | --- | --- | --- |
| {{PublicMarketingSite}} | {{VisitorPersona}} | {{ConversionTask}} | {{P0/P1/P2}} |
| {{DashboardOrAppArea}} | {{AuthenticatedPersona}} | {{CoreWorkflow}} | {{P0/P1/P2}} |
| {{AdminArea}} | {{AdminPersona}} | {{OperationalTask}} | {{P0/P1/P2}} |

## Brand Direction

| Attribute | Guidance |
| --- | --- |
| Personality | {{BrandPersonality}} |
| Visual tone | {{VisualTone}} |
| Voice | {{VoiceAndTone}} |
| Trust signals | {{TestimonialsCertificationsLogosMetrics}} |
| Conversion focus | {{PrimaryCTAAndSecondaryCTA}} |

## Typography

| Token | Use | Font | Size guidance | Notes |
| --- | --- | --- | --- | --- |
| Display | Hero or major page title | {{FontFamily}} | {{SizeRange}} | Use sparingly. |
| Heading | Section and page headings | {{FontFamily}} | {{SizeRange}} | Maintain clear hierarchy. |
| Body | Paragraphs and labels | {{FontFamily}} | {{SizeRange}} | Optimize for readability. |
| Mono | Code, IDs, technical values | {{FontFamily}} | {{SizeRange}} | Use only when semantic. |

## Color System

| Token | Value | Usage | Accessibility notes |
| --- | --- | --- | --- |
| `--color-background` | {{ColorValue}} | Page background | {{ContrastNotes}} |
| `--color-foreground` | {{ColorValue}} | Primary text | {{ContrastNotes}} |
| `--color-primary` | {{ColorValue}} | Primary actions | {{ContrastNotes}} |
| `--color-secondary` | {{ColorValue}} | Secondary actions or accents | {{ContrastNotes}} |
| `--color-danger` | {{ColorValue}} | Destructive actions and errors | {{ContrastNotes}} |
| `--color-success` | {{ColorValue}} | Success states | {{ContrastNotes}} |

## Spacing And Layout

| Area | Guidance |
| --- | --- |
| Page gutters | {{MobileTabletDesktopGutters}} |
| Section spacing | {{VerticalSpacingScale}} |
| Content width | {{MaxWidthPolicy}} |
| Grid | {{GridPolicy}} |
| Radius | {{RadiusScale}} |
| Shadows | {{ShadowPolicy}} |

## Responsive Behavior

| Breakpoint | Layout behavior | Navigation behavior | Content priority |
| --- | --- | --- | --- |
| Mobile | {{MobileLayout}} | {{MobileNav}} | {{PrimaryContentFirst}} |
| Tablet | {{TabletLayout}} | {{TabletNav}} | {{SecondaryContentRules}} |
| Desktop | {{DesktopLayout}} | {{DesktopNav}} | {{FullContentRules}} |

## Navigation

| Navigation area | Items | Access | Behavior |
| --- | --- | --- | --- |
| Header | {{Items}} | {{Public/Auth}} | {{StickyOrStatic}} |
| Sidebar | {{Items}} | {{Auth/Admin}} | {{CollapsedOrPersistent}} |
| Footer | {{Items}} | Public | {{SEOAndSupportLinks}} |
| Breadcrumbs | {{Routes}} | {{Public/Auth}} | {{WhenShown}} |

## Component Inventory

| Component | Purpose | States | Accessibility requirements |
| --- | --- | --- | --- |
| Button | {{ActionPurpose}} | Default, hover, focus, disabled, loading | Keyboard focus visible, descriptive text or label. |
| Input | {{DataEntryPurpose}} | Empty, focus, error, disabled, success | Associated label and error messaging. |
| Modal/Dialog | {{DialogPurpose}} | Open, closing, loading | Focus trap, escape close policy, labelled title. |
| Table/List | {{DataDisplayPurpose}} | Empty, loading, error, populated | Semantic markup and sortable labels if applicable. |
| Toast/Alert | {{FeedbackPurpose}} | Info, success, warning, error | Screen-reader announcement policy. |

## Forms

| Concern | Requirement |
| --- | --- |
| Labels | Every input has a visible or accessible label. |
| Validation | Errors are specific, close to the field, and available to assistive tech. |
| Submission | Loading and disabled states prevent duplicate submissions. |
| Recovery | Users can correct errors without losing valid input. |
| Required fields | Required status is clear without relying only on color. |

## UI States

- Empty states: {{EmptyStateGuidance}}
- Loading states: {{LoadingStateGuidance}}
- Error states: {{ErrorStateGuidance}}
- Success states: {{SuccessStateGuidance}}
- Disabled states: {{DisabledStateGuidance}}
- Offline or degraded states: {{OfflineStateGuidance}}

## Accessibility

- [ ] Use semantic HTML before custom roles.
- [ ] Maintain logical heading order.
- [ ] Ensure all interactive elements are keyboard reachable.
- [ ] Provide visible focus states.
- [ ] Meet {{WCAGTarget}} color contrast.
- [ ] Add alt text for meaningful images and empty alt for decorative images.
- [ ] Respect reduced-motion preferences.
- [ ] Test with screen reader basics for critical workflows.

## Icons And Images

| Asset type | Source | Usage rules |
| --- | --- | --- |
| Icons | {{IconLibraryOrCustomSet}} | Use consistent stroke, size, and accessible labels where needed. |
| Product images | {{Source}} | Show real product, workflow, or result where possible. |
| Illustrations | {{Source}} | Use only when they clarify the experience or brand. |
| Avatars/logos | {{Source}} | Provide fallbacks and size constraints. |

## Dark Mode

| Area | Requirement |
| --- | --- |
| Support level | {{Required/Optional/NotPlanned}} |
| Theme storage | {{System/Manual/AccountPreference}} |
| Tokens | {{DarkModeTokenPolicy}} |
| Testing | {{ContrastAndVisualQARequirements}} |

## SEO And Metadata

| Page type | Metadata | Structured data | Notes |
| --- | --- | --- | --- |
| Home | {{TitleDescriptionOG}} | {{SchemaTypeOrNone}} | {{CanonicalPolicy}} |
| Content page | {{TitleDescriptionOG}} | {{SchemaTypeOrNone}} | {{CanonicalPolicy}} |
| App page | {{TitleDescriptionRobots}} | None | {{IndexingPolicy}} |

## Performance

- Prefer Server Components unless interactivity requires client components.
- Keep layout shifts low with explicit image, media, and container dimensions.
- Lazy load non-critical media and heavy client-only components.
- Use responsive images and avoid oversized assets.
- Keep animation lightweight and optional for reduced motion.
- Monitor Core Web Vitals for public pages and interaction latency for app pages.

## Frontend Folder Guidelines

```text
src/
  app/
    {{route}}/
      page.tsx
      loading.tsx
      error.tsx
  components/
    {{component-name}}.tsx
  hooks/
    use-{{hook-name}}.ts
  lib/
    {{utility-name}}.ts
  types/
    {{type-name}}.ts
```

## Coding Standards

- Use TypeScript for component props and shared data shapes.
- Keep components small enough to understand without cross-file hunting.
- Prefer composition over large prop-driven conditionals.
- Avoid duplicate UI variants when an existing component can be extended cleanly.
- Keep class names readable and consistent with the existing Tailwind style.
- Do not leave console debugging statements in committed code.

## Frontend QA Checklist

- [ ] Mobile, tablet, and desktop layouts reviewed.
- [ ] Keyboard navigation works for critical flows.
- [ ] Focus states are visible.
- [ ] Loading, empty, error, disabled, and success states are covered.
- [ ] Images have correct sizing and alt behavior.
- [ ] Metadata and heading hierarchy are correct for public pages.
- [ ] No text overlaps or overflows in supported viewports.
