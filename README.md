# sparkjoy assets

The files [sparkjoy](https://github.com/max-sixty/sparkjoy) keeps out of its own
repository, so that neither its history nor an install of the plugin carries them:

- `evals/requests/<case>/<hash>.json.gz`: a case's request, as the plugin's fork sends
  it, without what sparkjoy's `evals/build.py` takes out before publishing, named for
  the hash of its JSON;
- `evals/results/<started>-<random>.jsonl`: the results of one batch of
  `evals/run.py`'s runs, one row each;
- `images/<name>/<hash>.<extension>`: an image sparkjoy's README and docs show, such
  as a chart `model/docs.py` draws, named for the hash of its bytes.

Files are only ever added here, each under a name no other file takes, so `main` holds
everything ever published. sparkjoy's `evals/requests.json` names the request each case
sends, its README and docs link each image here, and its `model/sparkjoy_assets.py`
fetches files from here and publishes new ones. Don't edit them by hand.
