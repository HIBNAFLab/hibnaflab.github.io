# Website visitor tracking (Google Analytics 4)

GitHub Pages does not provide a built-in visitor analytics dashboard.

1. Create a Google Analytics account and a GA4 web data stream for https://hibnaflab.github.io/.
2. Copy your Measurement ID (format G-XXXXXXXXXX).
3. In each HTML file (index.html, collaborators/index.html, tools/index.html), add the following snippet immediately before </head>, replacing G-XXXXXXXXXX with your actual ID:

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

4. Commit the updates to GitHub, wait for Pages deployment, and check Realtime in Google Analytics.

Google Analytics measures visits/page views and users, but does not provide a perfectly accurate count of all unique visitors; tracking may be blocked by browser settings or consent controls. Depending on your visitors and jurisdiction, you may need a privacy notice and consent mechanism. Do not publish your Google Analytics API secrets (the Measurement ID is public).

Alternative: privacy-oriented analytics services may offer limited free plans, but check current terms before selecting one.

No live counter is included yet, because a genuine tracking service must be configured.
