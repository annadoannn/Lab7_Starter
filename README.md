# Lab 7 - Unit & E2E Testing
By **Anna Doan**

***"Check Your Understanding"* Questions**

**1. Where would you fit your automated tests in your Recipe project development pipeline? Select one of the following and explain why.**

1. Within a GitHub action that runs whenever code is pushed
2. Manually run them locally before pushing code
3. Run them all after all development is completed

> I selected: **1. Within a GitHub action that runs whenever code is pushed** because this allows continuous integration and ensures that broken code is caught immediately after each push, before it’s merged or deployed. It prevents broken code from being merged or deployed and encourages early debugging during development.

**2. Would you use an end to end test to check if a function is returning the correct output? (yes/no)**

> No. E2E tests are designed to simulate real user workflows across the full application stack. They are not intended to test isolated functions. Unit tests are more appropriate for checking individual function outputs.

**3. What's the difference between navigation and snapshot mode?**
> **Navigation mode** analyzes your web page as it loads from a URL, simulating the full page load experience from a user's perspective. It captures metrics like: performance, structure, cumulative layout shift, etc. In more specific words: First Contentful Paint (FCP), Largest Contentful Paint (LCP), and Total Blocking Time (TBT) are some metrics. 
> On the other hand, **Snapshot mode** analyzes the page's current DOM state at a single point in time. It's better for identifying static accessibility or layout issues, but does not measure load performance. 


**4. Name three things we could do to impove the CSE 110 shop site based on the Lighthouse results?**
> The three things we can improve on are:
> - Compress and resize images to reduce load time. 
> - add a `<meta name="viewport>` tag for responsive design on mobile devices. 
> - Use <link rel="preconnect"> for `https://fakestoreapi.com` to reduce connection setup time and improve FCP and LCP by initiating early network connections.

## Notes
### Expose: E2E Testing with Jest-Puppeteer

> *To prevent interference between tests, `localStorage.clear()` and `page.reload()` are used before cart-count tests to ensure that the page starts in a clean state.*








