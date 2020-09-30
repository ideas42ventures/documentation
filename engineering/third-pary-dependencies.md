# Third Party Dependencies

Guidlines, preferences, and ideas about using third-party software

## JavaScript

### Yarn over npm

We prefer to use Yarn instead of npm on all projects. There's not a ton of backing behind this reasoning, it's largely a preference. A couple light reasons;

- You can type less: `yarn my-script` vs `npm run my-script`. Yarn allows you to omit `run` for custom scripts
- Political reasons: npm has a checkered past in the JS community. There are numerous examples of the company making decisions that are bad
- It's not owned by GitHub: We use GitHub for so much, good to have a least one tool that's outside of a single company's control

#### Do: Ignore npm lock file

We don't want projects to have both a `yarn.lock` and `package-lock.json`. It's too much to manage. To avoid this, projects should add `package-lock.json` to their `.gitignore`.

### Always use exact versions

When using third party dependencies, always use exact versions. That is, versions without `^` or `~`. We do not want third-party dependencies updating without our knowledge and explicit permission to do so. Over the years, this has been the cause of many broken builds resulting in pulled out and grey hairs.

#### Do: Set config for exact version

Yarn and npm default to `^` you can and should change this in your config:

```
yarn config set save-prefix ""
```
