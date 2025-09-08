# WelcomingWeb Accessibility Widget – GTM Template (Light)

Loads the WelcomingWeb Accessibility Widget via CDN with a single required field: **Widget ID**.

## Install & use
1. In GTM: **Templates → Tag Templates → Import** `template.tpl`.
2. Create a tag: **Tags → New → WelcomingWeb Accessibility Widget**.
3. Fill **Widget ID** (UUID).
4. (Optional) **Requires Consent** (e.g., `functional` or `functional,analytics`) if you gate loading via CMP.
5. (Optional) **CSP Nonce** if your site uses a nonce and you want the injected `<script>` to carry it.
6. Trigger on **All Pages** (or as needed) → Publish.

## What the template injects
A single `<script>` tag:
- `src="https://cdn-01.welcomingweb.com/a11y-widget.bundle.js"`
- `data-widget-id="..."` (required)
- `data-requires-consent="..."` (optional)
- `data-csp-nonce="..."` (optional)

All styling/positioning/behavior defaults come from the server configuration.

## Optional: consent gating
The tag can wait for consent categories before initializing. You can grant via your CMP’s GTM consent integration or manually:
```html
<script>
  // Example manual grant (use the categories you configured)
  window.welcomingWeb = window.welcomingWeb || {};
  window.welcomingWeb.grantConsent && window.welcomingWeb.grantConsent();
</script>
