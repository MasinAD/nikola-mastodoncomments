Use [Mastodon Comments](https://joinmastodon.org/) as a comment system.

[Mastodon Comments](https://joinmastodon.org/) is a federated microblogging network,
based on the [ActivityPub](https://www.w3.org/TR/activitypub/) protocol.
Users can respond to anchor posts in the Fediverse.

The settings for Mastodon Comments can be passed to the plugin as follows:

```python
COMMENT_SYSTEM = "mastodon"
COMMENT_SYSTEM_ID = "<YOUR-SITE_NAME>"
GLOBAL_CONTEXT = {
    ...
    "mastodon_config": {
        'host': 'nerdculture.de',
        'account_id': '109270094542366763',
        'account': 'fluchtkapsel'
        }
    }
```
See [this page](https://khendrikse.netlify.app/blog/find-your-mastodon-account-id/) on how to find your Mastodon account id.

You need to copy the files `mastodon.js` and `mastodon.css` from `assets/files/{css,js}/` to `files/{css,js}/` respectively.
