# Page Speed and Core Web Vitals Quality Gate

> Quality gate for page speed performance and Core Web Vitals compliance. Must pass before landing pages receive paid traffic at scale.

## Section 1: Core Web Vitals Assessment
- [ ] Largest Contentful Paint (LCP) is under 2.5 seconds (Good threshold)
- [ ] Interaction to Next Paint (INP) is under 200 milliseconds (Good threshold)
- [ ] Cumulative Layout Shift (CLS) is under 0.1 (Good threshold)
- [ ] Core Web Vitals are measured using real user data (Chrome UX Report / PageSpeed Insights field data) when available
- [ ] Lab data is used as a supplement (Lighthouse, WebPageTest) for diagnostic purposes

## Section 2: Loading Performance
- [ ] Total page load time is under 3 seconds on a 4G mobile connection
- [ ] Time to First Byte (TTFB) is under 800ms (server response time)
- [ ] First Contentful Paint (FCP) is under 1.8 seconds
- [ ] Total page weight is under 2MB (including all resources: HTML, CSS, JS, images, fonts)
- [ ] Number of HTTP requests is minimized (under 50 for landing pages)

## Section 3: Image Optimization
- [ ] Images are served in next-gen formats: WebP or AVIF (with JPEG/PNG fallbacks)
- [ ] Images are properly sized (not serving 2000px images in 400px containers)
- [ ] Lazy loading is implemented for below-the-fold images (loading="lazy" attribute)
- [ ] Hero/above-the-fold images are preloaded for faster LCP
- [ ] Image compression is applied without visible quality loss (85% quality for JPEG, lossless for PNG with transparency)

## Section 4: Code and Resource Optimization
- [ ] Critical CSS is inlined in the <head> for above-the-fold rendering
- [ ] Non-critical CSS and JavaScript are deferred or loaded asynchronously
- [ ] JavaScript bundles are minified and tree-shaken (no unused code shipped to the browser)
- [ ] Third-party scripts (analytics, chat widgets, tracking pixels) are loaded asynchronously and do not block rendering
- [ ] Font loading strategy is implemented: font-display: swap with preloaded WOFF2 files
- [ ] Browser caching headers are configured with appropriate max-age values (static assets: 1 year, HTML: short/no-cache)

## Section 5: Infrastructure and Delivery
- [ ] CDN (Content Delivery Network) is configured for static asset delivery
- [ ] GZIP or Brotli compression is enabled on the server for text-based resources
- [ ] HTTP/2 or HTTP/3 is enabled on the server
- [ ] SSL/TLS certificate is valid and connection uses HTTPS
- [ ] Server-side rendering (SSR) or static site generation (SSG) is used for landing pages (not client-side rendering that delays content)

## Section 6: Monitoring
- [ ] Page speed is tested on both mobile and desktop (mobile is the priority for ad traffic)
- [ ] Performance budget is established: maximum page weight, maximum JS size, target LCP
- [ ] Automated performance monitoring alerts on regression (Lighthouse CI, SpeedCurve, or similar)
- [ ] Page speed is re-tested after any content or code changes to the landing page

## Approval
- **Minimum pass rate**: 20/24 items (83%)
- **Reviewer**: cro-specialist-agent + dev-ops-agent
- **Escalation**: LCP above 4 seconds or CLS above 0.25 are hard blocks; page must be optimized before receiving paid traffic
