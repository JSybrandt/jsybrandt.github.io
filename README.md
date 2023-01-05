Hey Justin.

If you're  reading this, you're probably confused about how this website works
(it was a while since you set it up).

This is a fork of an old hugo site you had. The big difference is that now we
deploy using the .github/workflows/hugo web hook. This was in beta when you
enabled it. Maybe it needs updating.

The way this works is that whenever you push a new commit to "main" you should
see an update on the website in ~2min.

Hopefully its easy! You can always debug locally by running `hugo server`.
