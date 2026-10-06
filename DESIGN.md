# Design

Inherited from upstream Kortix; changes here should stay close to upstream to keep merges cheap.

- Web: Radix UI primitives + utility CSS in `apps/frontend`; mobile mirrors it with `@rn-primitives` in `apps/mobile`.
- Keep one component vocabulary across web/mobile (dialogs, menus, tabs, toasts) and shared copy/logic in `packages/shared`.
- LAVA-specific branding (logo, colours) — document tokens here before overriding upstream styles.
- Accessibility: rely on Radix/RN primitives' a11y; don't replace them with custom divs.
