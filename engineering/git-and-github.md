# Using Git and GitHub

### Contents

- [Flow](#flow)
- [Commits](#commits)
- [Pull Requests](#pull-requests)
- [Code Reviews](#code-reviews)

## Flow

99% of the time, you don't want to make changes directly on the `main` branch of any repo. Instead use branches and pull requests. We use a version of [GitHub flow](https://guides.github.com/introduction/flow/).

When working on documentation, bug fix, feature, or any other change to a repo:

1. Create a new branch off of `main`
   - Example; `git checkout -b ll-updates-og-meta`
1. Use descriptive names prefixed with your initials. If there’s an issue number, include that, followed by a couple words to describe the work;
   - Good; `tg-fixes-broken-link`, `ml-234-adds-faq-page`
   - Not so good; `changes`, `fix-bug`, `updates`
1. Work, work, work. Making commits to your branch along the way. See [Commits](#commits) below for tips

## Commits

Commits and messages should be atomic and deliberate.

- Make small, focused commits in your branches. You want each commit to be as specific as possible
  - Good; Add one file and commit with the message; "Updates meta description"
  - Not so good; Add 37 files and commit with the message; "fixes"
- The idea behind small commits is that if you need to, you can pluck any individual commit out and review it, change it, move it to another branch, etc
- Write commit messages where the commit is the subject and it will do a thing in the future tense
  - Good; "Adds about page", "Fixes cross browser style issues", "Updates react version"
  - Not so good; "updates", "changes", "did things"
  - **Caveat**: Because you're working in your own branch, if the "bad" commits make it in, that's OK and happens. Because we squash commits you will clean that up later

## Pull Requests

Pull requests are how we make changes to codebases. They're also a way to leave a trail of documentation for a codebase as it matures over time. PR descriptions, commit messages, branch names, et al give insight into decisions.

- Open pull requests early, you don't need to wait until you’re done with the work. Pull requests are a signal to the team what you're working on
- Write thorough desriptions.
  - Descriptions need to explain the what and why for the changes
  - Imagine the person reading the description has no context about the work you've done, then write from that perspective
  - If you need someone to QA a UI, give instructions for what they need to do to see the changes; Is this available on a staging URL? Do they need to run this locally? Do they need to reinstall dependencies?
- Don’t merge other team members’ pull requests unless you have coordinated with them first
- Only use the squash commit strategy in GitHub (this will be the setting for the repo)
  - Clean up the squashed commit message. It should only contain pertinent information about the final changeset and should be written in the same style as commit messages; commit is the subject and is doing things in the future tense
  - Use as much space as you need in the message, but make the first line 50 characters or less, then add a blank line and continue writing from there. GitHub adds a nice tap-to-expand for this
- Delete branches after they've been merged to `main`. We have this set to automattic on most repos
- Delete stale branches. We will do periodic cleanups and ask if you still need branches

## Code Reviews

- **Code reviews are not mandatory**
- Repos should not have their main branch set to require code reviews unless there is a very specific reason

Code reviews and feedback in general are a gift. When you get feedback, welcome it. Learn from it. When you give feedback, be kind. You should request code reviews on pull requests when you want or feel like you need feedback. This could be because you're trying something new and want another opinion. Or when you're working on a particularly important piece of a codebase.

Again, code reviews are not mandatory. You should feel comfortable merging code when you're confident in your changes.
