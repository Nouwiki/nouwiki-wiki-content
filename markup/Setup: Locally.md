+++
import = []
css = []
js = []
+++

# Setup: Locally

1. `npm i -g git+https://github.com/Nouwiki/Nouwiki.git`
2. `nouwiki forge ./wiki_directory`
3. `nouwiki build ./wiki_directory` <- only needed for static or dynamic modes
4. `nouwiki serve ./wiki_directory` <- now visit the site at the port specified, usually `8080` at [http://localhost:8080/](http://localhost:8080/)