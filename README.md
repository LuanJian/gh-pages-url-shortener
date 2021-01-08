# GitHub Pages URL Shortener

This is a minimal URL shortener that can be entirely hosted on GitHub pages. It does not need the maintenance of any servers or databases and can be hosted entirely on GitHub for free!

## 👨‍🏫 Demo

1. [https://luanjian.github.io/gh-pages-url-shortener/1](https://luanjian.github.io/gh-pages-url-shortener/1) should link to this repo.

2. To add a new short link, add an issue with the title being the link you want
   to shorten (including the `http(s)://`) to
   [https://luanjian.github.io/gh-pages-url-shortener/issues](https://luanjian.github.io/gh-pages-url-shortener/issues).

3. The newly created short url can be accessed via `https://luanjian.github.io/gh-pages-url-shortener/{issue_number}`

## ☕️ Use

1. Fork the repo before cloning your fork.
2. Set up GitHub pages for your forked repo.
   a. In your forked repo, **click the Settings tab** and scroll down to the
      GitHub Pages section.
   b. Then select the **main branch** source and click on the **Save** button.
   c. <img src="https://i.imgur.com/kjinFX9.png" alt="How to create GitHub page" height="176px">
3. If you are using your own domain:
   a. [Set your domain up for GitHub pages.](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain)
   b. Change the URL in `CNAME` file to your domain.
4. If you are using GitHub page's default domain i.e. Something like
   `https://<username>.github.io/<repo-name>/`
   a. Delete the `CNAME` file.
   b. Change `var PATH_SEGMENTS_TO_SKIP = 0;` at the top of `404.html` to
      `var PATH_SEGMENTS_TO_SKIP = 1;`.
      1. This is as GitHub domains have an additional path segment (the repo name) after the host name.
5. Create a new repo as a database. (Or you could use your forked repo)
   a. Update `var GITHUB_ISSUES_LINK = "<your-github-issues-link>";` at the top of `404.html` accordingly afterwards.
      1. Format for `GITHUB_ISSUES_LINK`:
         `https://api.github.com/repos/{owner}/{repo}/issues/`
      2. Remember the trailing `/`!
6. Push your changes to your forked repo, and your low cost and cool as heck URL shortener will be ready for use!
