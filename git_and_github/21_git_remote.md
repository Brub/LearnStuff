# Git remote

To see which remote servers you have configured, you can run the `git remote` command.
It list the shortnames of each remote handle you've specified.
If you've cloned your repository, you should at least see `origin` that is the default name Git gives to the server you cloned from

You can also specify `-v`, which shows you the URL's Git has stored for the shortname to be used when reading and writing to that remote

example: `git remote -v`

If you want to see more information about a remote, you can use `git remote show [remote-name]`

example: `git remote show origin`
