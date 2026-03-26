# Anti-Generic Patterns (Blocklist)

Avoid these patterns unless the user explicitly requests them.

1. Default navigation with no domain context.
2. Generic metrics dashboard unrelated to product KPIs.
3. Generic placeholder copy (e.g. “Welcome back”, “Get started”) without context.
4. Random spacing that ignores token/grid rules.
5. Typography with no clear hierarchy.
6. All screens look like the same cross-domain template.
7. Excessive custom components when DS components already fit.
8. Error states without recovery actions.
9. Visually polished UI but weak flow completion (not task-oriented).
10. Adding out-of-scope features without user approval.

## Non-Genericity Heuristics
- Each screen includes >=2 domain-specific elements.
- Copy/action labels reflect actual user task context.
- Layout decisions are directly tied to flow objectives.

## Mobile-Specific Anti-Patterns
11. Ignoring safe area insets and gesture-conflict zones.
12. Form/composer hidden behind keyboard without recovery behavior.
13. Same interaction model on iOS/Android when platform conventions differ.
14. Dense desktop-like layout copied directly into phone viewport.
15. Animations that hurt scroll/input responsiveness.
