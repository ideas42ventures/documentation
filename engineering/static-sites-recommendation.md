# Static Site Recommendations

Your company will a least one static website. It’s likely your team will end up
building many static sites. These are used for marketing, prototypes, one-off
efforts, and for many different solutions.

## What Is a Static Site?

A static site is one that does not require it's own custom web server or database
to work. They’re built with browser technologies; HTML, CSS, and JavaScript.

That doesn't mean they don't do anything. Static sites can provide complex
interactions by leveraging APIs.

## High Level Recommendations

For all of these, there are other options, but these are the tools we know best.

- **Use Netlify** for hosting. This isn't the only way to host a static site, but has many benefits to help make the process fast, easy, and repeatable.
- **Use Eleventy** for a static site generator. If you're building a marketing site or other site with limited functionally that requires JavaScript, but has more than a single page, it's an excellent tool.
- **Use Create React App** for sites that have sufficient interation needs that go beyond a static site. These are considered single-page-apps (SPA). This is case-by-case. Making the decision to build an SPA will be a larger conversation with the engineering team members.

## Examples

These are existing examples of static sites within The Studio or good third-party examples.

### Static Site Generated with Eleventy

Our public site uses Eleventy and is hosted on Netlify. It's a prime example of when a static site generator is appropriate.

Repo: https://github.com/ideas42ventures/ideas42ventures.com

The site is a handful of pages with limited interactivity used for general web presence, entrepreneur recruitment, team recruitment, etc. It's one of the ways we interact with people online.

#### Tech Details

- Standard Eleventy install
- Nunjucks templates. More features than Handlebars, familiar setup
- Standard CSS (no sass, css-in-js, et al) with the [Super Simple CSS Concatenation](https://www.11ty.dev/docs/quicktips/concatenate/) approach documented in Eleventy. That's the only CSS processing necessary. It's easier to work with separate topical CSS files
- Prettier code formatting using lint-staged and husky for pre-commit hook.
- Local setup is; `yarn && yarn start`
- Staging deploys: Every pull request is deployed to a staging environment with a unique URL. We get this from Netlify with zero extra work. This is extremely valuable to QA work-in-progress
- Production deploys: Every merge to `main` deploys to production. Again, Netlify handles this with no extra setup on our part.
- For full local setup and deploy docs see the project [README](https://github.com/ideas42ventures/ideas42ventures.com/blob/main/README.md)
