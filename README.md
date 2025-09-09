# WelcomingWeb Accessibility Widget – GTM Template

## Overview
Loads the WelcomingWeb Accessibility Widget via CDN with a single required field: **Widget ID**.

## Install & Use
1. In GTM: **Templates → Tag Templates → Import** `template.tpl`.
2. Create a tag: **Tags → New → WelcomingWeb Accessibility Widget**.
3. Fill **Widget ID** (UUID).
4. (Recommended) Open **Advanced → Consent Settings** and require the consent types your policy needs (e.g., `functionality_storage`).
5. Add a trigger (e.g., **All Pages**) and publish.

All styling, positioning, and behavior defaults are controlled by your server-side configuration.

## Consent & CSP

**Consent:** Managed by GTM’s Consent Mode. Use **Consent Settings** (and/or the template’s built-in consent checks) to gate this tag. No additional template fields or manual `grantConsent()` calls are needed.  
**CSP:** If you use a nonce, adopt GTM’s **nonce-aware container snippet** so GTM applies the nonce automatically.

## Support

- Website: <https://welcomingweb.com>
- Docs: (add your docs URL)
- Issues: Enable GitHub Issues on the template repository.


## What the template injects
A single script tag:

```html
<script src="https://cdn-01.welcomingweb.com/a11y-widget.bundle.js?wid=YOUR_WIDGET_ID"></script>
 
  
