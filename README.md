# Tweet archiver #

This Python script and the related files will download your tweets from Twitter and save them in a plaintext archive file on your computer. It is intended to be run periodically to add recent tweets to an existing archive file. The script (in a slightly earlier version) is described in [this blog post][1]. If you already have an archive of tweets in ThinkUp, you might find [this post][2] useful in turning it into a plaintext archive. If you are starting an archive from scratch, [this post and script][3] by Tim Bueno will be helpful.

The files in the repository are:

* `archive-tweets.py`. This is the script that does the archiving. It can be stored anywhere and should be run periodically via a system like `cron` or `launchd`.
* `twitter.txt`. This is the archive file itself, currently empty. It should be kept in a folder named `twitter` inside your Dropbox folder.
* `twitter-credentials`. This file should be renamed `.twitter-credentials` and saved in your home directory. The values for `consumerKey`, `consumerSecret`, `token`, and `tokenSecret` must be provided by Twitter. Go to the [Twitter developer site][4], click the "Create an app" link, and follow the instructions given there for creating an app. When you're done, you'll be given the four credentials—long strings of letters and numbers—you'll need.
* `lastID.txt`. This file holds the ID number of the most recently archived tweet. It should be kept in the same folder as `twitter.txt`.

You don't *have* to keep your archive in Dropbox, but that's a convenient place to be able to access your tweets from any of your computers. The directory for the archive can be changed by editing Line 10 of `archive-tweets.py`.



[1]: http://www.leancrew.com/all-this/2012/07/archiving-tweets-without-ifttt/
[2]: http://www.leancrew.com/all-this/2012/07/archiving-tweets/
[3]: http://www.timbueno.com/2012/07/07/rolling-my-own-automatic-tweet-archiver
[4]: https://dev.twitter.com/
