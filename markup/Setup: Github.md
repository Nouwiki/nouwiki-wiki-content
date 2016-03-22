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

Finally push to both repos and create a gh-pages branch for the `yourwiki` repo, and then  you're good to go, everything will be served through the `dynamic` mode and all you have to do to create new content is to update the `yourwiki-content` repo.

Since GitHub Pages hosting is expected to be fairly common we plan to make this doable with fewer commands.
<!-- -->