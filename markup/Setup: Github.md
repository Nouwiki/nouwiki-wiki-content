+++
import = []
css = []
js = []
+++

# Setup: Github

> Note: At some point this process will be simplified.

First create `yourwiki` and `yourwiki-content` repos, then hook them into your wiki:

```
cd ./yourwiki
git init
git remote add origin https://github.com/UserName/yourwiki.git
git submodule add https://github.com/UserName/yourwiki-content ./wiki
cd wiki
git remote add origin https://github.com/UserName/yourwiki-content.git
```

Then push to both repos and create a gh-pages branch for the `yourwiki` repo.

To then edit and push those edits you either edit in-browser through `nouwiki serve` where changes automatically get commited or you edit through a text editor and you commit them yourself, and finally you push to your content repo, but don't forget to update the submodule reference in the main repo to the latest commit as well.

The following are the steps necissary to update the wiki:

```
git clone https://github.com/UserName/yourwiki.git
cd ./yourwiki
git clone https://github.com/UserName/yourwiki-content.git ./wiki
# *edit in-browser*
cd ./wiki
git push
cd ..
git submodule update
git add --all
git commit -m "submodule reference update"
git push -u origin master && git push -f origin master:gh-pages
```