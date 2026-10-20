# DUOS articles: editor trial

A throwaway trial for [DT-4234](https://broadworkbench.atlassian.net/browse/DT-4234). It holds the 36
duos.blog articles as a Docusaurus site, published to
https://kevinmarete.github.io/duos-blog-trial/ about two minutes after each save to `main`.
Nothing here is the real site, so feel free to break it.

## The task

Write one short article, publish it, and check that it shows up on the site. Do it once in each
editor below, then say which you would want to use every day, and where you got stuck.

| Editor | How to open it | Sign in |
| --- | --- | --- |
| Sveltia CMS | https://kevinmarete.github.io/duos-blog-trial/admin/ | "Sign In Using Access Token" with a GitHub token (see below). "Sign In with GitHub" does not work on this trial |
| Pages CMS | https://app.pagescms.org, then pick `kevinmarete/duos-blog-trial` | Sign in with GitHub |
| GitHub's editor | "Edit this page" at the bottom of any article, or "Add file" on the `blog` folder | Already signed in to GitHub |

**GitHub token for Sveltia:** open https://github.com/settings/tokens/new?scopes=public_repo&description=DUOS%20editor%20trial,
set an expiry of 7 days, click Generate token, and paste the token into Sveltia. Fine-grained tokens
can't reach a repo on another person's account, so use this classic one. Delete it when the trial is over.

## How the site is built

`blog/` holds the posts, `src/pages/` the help and about pages, and `static/article-images/` the
images. `.github/workflows/deploy.yml` builds and deploys on every push to `main`.
