Use [Mastodon Comments](https://joinmastodon.org/) as a comment system.

[Mastodon Comments](https://joinmastodon.org/) is a federated microblogging network,
based on the [ActivityPub](https://www.w3.org/TR/activitypub/) protocol.
Users can respond to anchor posts in the Fediverse.

The settings for [Mastodon Comments](https://joinmastodon.org/) can be passed to the plugin as follows
(see the [quickstart guide](https://cactus.chat/docs/getting-started/quick-start/)
and [configuration reference](https://cactus.chat/docs/reference/web-client/#configuration)
for more details, including the full list of configuration options):

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
