+++
import = []
css = []
js = []
+++

# Setup: Github

First create `yourwiki` and `yourwiki-content` repos, then:

```
cd ./yourwiki
git init
git remote add origin https://github.com/UserName/yourwiki.git
git submodule add https://github.com/UserName/yourwiki-content ./wiki
cd wiki
git remote add origin https://github.com/UserName/yourwiki-content.git
```

Finally push to both repos and create a gh-pages branch for the `yourwiki` repo.

Now for someone else to edit its recommended that you clone the gh-pages repo instead of the content repo, but pull in the content repo as well, then push the content repo and an updated reference in the gh-pages repo to that new content repo commit.

```
git clone https://github.com/UserName/yourwiki.git
cd ./yourwiki
git clone https://github.com/01AutoMonkey/yourwiki-content.git ./wiki
# *edit in-browser*
cd ./wiki
git push
cd ..
git submodule update
git add --all
git commit -m "submodule reference update"
git push -u origin master && git push -f origin master:gh-pages
```