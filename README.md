Use [Mastodon](https://joinmastodon.org/) as a comment system for static site generator [Nikola](https://getnikola.com).

Mastodon is a federated microblogging network, based on the [ActivityPub](https://www.w3.org/TR/activitypub/) protocol.
Users can respond to anchor posts in the Fediverse.

# How to configure
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

# How to install
You need to copy the files `mastodon.js` and `mastodon.css` from `assets/files/{css,js}/` to `files/{css,js}/` respectively. Additionally, it requires DOMpurify which you can install by
```
wget https://raw.githubusercontent.com/cure53/DOMPurify/main/dist/purify.min.js
```
in your `files/js` folder.

# How to use
This plugin fetches Mastodon posts which are in reply to a post that is referred to in a Nikola page's or post's meta data. Ideally, you write a blog entry, link to that blog entry on Mastodon and grab this Mastodon post's ID. Put this ID in the post's or page's meta data:
```
.. mastodon: 12345678901234567890
```

# Credits
This plugin is basically a port of the work for Ghost and Hugo done by
* [Simon Detheridge](https://sd.ai/blog/2023-10-19/integrating-mastodon-and-ghost/)
* [Carl Schwan](https://carlschwan.eu/2020/12/29/adding-comments-to-your-static-blog-with-mastodon/)
* [Veronica Berglyd Olsen](https://berglyd.net/blog/2023/03/mastodon-comments/)
