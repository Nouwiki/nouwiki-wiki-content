+++
import = []
css = []
js = []
+++

# Setup: Locally

1. `nouwiki forge ./wiki_directory`
2. `nouwiki build ./wiki_directory` <- only needed for static or dynamic modes

Then you can choose from:

1. Viewing the wiki statically by opening up static.html in a browser.
2. View the wiki statically or dynamically by serving the wiki directory with something like `http-server` or `python -m SimpleHTTPServer` (you can choose from `index.html`, `static.html`, and `dynamic.html`, `index.html` being whatever is set to default in nouwiki.toml at the time of the last build).
3. Fully-featured Nouwiki Server by doing `nouwiki serve ./wiki_directory` and visiting the site at the port specified, usually `8080` at [http://localhost:8080/](http://localhost:8080/)