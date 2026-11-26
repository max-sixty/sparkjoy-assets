# sparkjoy assets

The data [sparkjoy](https://github.com/max-sixty/sparkjoy)'s evals read and write,
kept here so that neither sparkjoy's history nor an install of the plugin carries it:

- `evals/requests/<case>/<hash>.json.gz`: a case's request, as the plugin's fork sends
  it, without what sparkjoy's `evals/build.py` takes out before publishing, named for
  the hash of its JSON;
- `evals/results/<started>-<random>.jsonl`: the results of one batch of
  `evals/run.py`'s runs, one row each.

Files are only ever added here, each under a name no other file takes, so `main` holds
everything ever published. sparkjoy's `evals/requests.json` names the request each case
sends, and its `evals/sparkjoy_assets.py` fetches files from here and publishes new ones.
Don't edit them by hand.
