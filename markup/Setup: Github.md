+++
import = []
css = []
js = []
+++

# Setup: Github

First create `yourwiki` and `yourwiki_content` repos, then:

```
cd ./yourwiki
git init
git remote add origin https://github.com/username/yourwiki.git
git submodule add https://github.com/username/yourwiki_content ./wiki
cd wiki
git remote add origin https://github.com/username/yourwiki_wiki.git
```

Finally push to both repos and create a gh-pages branch for the `yourwiki` repo, and then  your good to go, everything will be served through the `dynamic` mode and all you have to do to create new content is to update the `yourwiki_content` repo.