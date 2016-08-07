# Gazette listing

This is a simple Jekyll website listing South African Gazettes that [Code for South Africa](http://codes4sa.org)
has scraped.

The structure is simple. Each jurisdiction (province) and year has an entry in the ``_gazettes`` directory, which
Jekyll treats as a collection. All the gazette info is taken from ``_data/gazettes.json`` which is grouped
by jurisdiction and year. Jekyll then does the hard work of generating the listings for each jurisdiction and year.

# Running locally

1. Clone the repo
2. Run ``bundle install``
3. Run ``jekyll server --watch``

# Updating

To update this list from the production index:

    curl http://code4sa-gazettes.s3.amazonaws.com/archive/index/gazette-index-latest.jsonlines -O
    python build-index.py
    git add _data _gazettes
    git commit -m "Updated index"
    git push

# License

MIT License.