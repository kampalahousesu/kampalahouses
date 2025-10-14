How to create a proper favicon.ico and make your logo show in tabs and search engines

1) Create favicon.ico from PNG
   - Use an online tool (e.g., https://favicon.io/ or https://realfavicongenerator.net/) or by running ImageMagick locally:
     magick convert icon-deal.png -define icon:auto-resize=64,48,32,16 favicon.ico
   - Place the generated favicon.ico file in this folder (public/img/favicon.ico)

2) Update the site's canonical URL in HTML
   - Open public/index.html and replace every occurrence of https://yourdomain.com/ with your real site URL (include https://)
   - This ensures the JSON-LD organization logo and Open Graph image point to valid absolute URLs.

3) Test
   - Clear browser cache (Ctrl+F5) and reload the site. The tab icon (favicon) should appear.
   - Use the Facebook/Twitter/Open Graph debugger to refresh cache for social previews:
     - Facebook Sharing Debugger: https://developers.facebook.com/tools/debug/
     - Twitter Card Validator: https://cards-dev.twitter.com/validator

Notes:
 - Modern browsers support PNG favicons, but some older tools expect an ICO file. Generating favicon.ico with multiple sizes is recommended.
 - For best social previews, create 1200x630 PNG images and reference them in og:image and twitter:image with an absolute URL.
