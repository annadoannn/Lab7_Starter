# Lab 7 - Unit & E2E Testing
By **Anna Doan**

**Questions**

**1. Where would you fit your automated tests in your Recipe project development pipeline? Select one of the following and explain why.**

1. Within a GitHub action that runs whenever code is pushed
2. Manually run them locally before pushing code
3. Run them all after all development is completed

> I selected: *1. Within a GitHub action that runs whenever code is pushed* because this allows continuous integration and ensures that broken code is caught immediately after each push, before it’s merged or deployed.

**2. Would you use an end to end test to check if a function is returning the correct output? (yes/no)**

> No. E2E tests check full workflows, not isolated logic. Unit tests are more appropriate for function output.

## Notes
### Expose: E2E Testing with Jest-Puppeteer

> *To prevent interference between tests, `localStorage.clear()` and `page.reload()` are used before cart-count tests to ensure that the page starts in a clean state.*








