git clone https://github.com/11ty/eleventy-base-blog.git blog-tech
cd blog-tech
npm install

rm -rf .git
git init
git add .
git commit -m "Initial commit of base 11ty template"
git branch -M main
git remote add origin https://github.com/Jallalbrahimi/blog-tech.git
git push -u origin main


Edit _data/metadata.js with your blog’s information.
Delete the block related to configuration init from _includes/layouts/home.njk.

rename .github/workflows/gh-pages.yml.sample to gh-pages.yml
Go to the repository’s Settings on GitHub.
In the GitHub Pages section change:
    Source: Deploy from a branch
    Branch: gh-pages/(root)

package.json scripts section
"scripts": {
  "build-ghpages": "npx @11ty/eleventy --pathprefix=/blog-tech/",
}
