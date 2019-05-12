---
title: Frequently Asked Questions
---

If you want to ask a new question, do so on the [Mailing list](mailing-list.md). If you get
your question answered on the mailing list, please add the question and
answer here for other people to find.

I'm having some kind of "ImportError: cannot import name XYZ" bug when starting gPodder. What can I do?
-------------------------------------------------------------------------------------------------------

Please check if you have all dependencies installed (the ImportError
should already give you a clue what's missing). If it's some
gpodder-internal module that cannot be loaded, this probably means that
you have installed different versions of gPodder on your system that
conflict. Make sure to remove all locally-installed gPodder files from
`/usr/local` and also check which gPodder version is installed in `/usr`
and remove the installed gpodder package if necessary. Then, install the
newest version from your distribution or via the Download page on
gPodder.org. If you still have problems, please file a [bug report](https://github.com/gpodder/gpodder/issues).

Where are my downloaded episodes?
------------------------------

You can find the answer in the [user manual](user-manual.html#gpodder-home-folder-and-download-location).

No, you won't.  The User Manual is incorrect.  All explanations and examples are wrong for Debian Linux.
The correct answer is: Your home directory is /home/[your_user_name]/gPodder, and the downloaded podcasts
are in /home/[your_user_name]/gPodder/Downloads.

If you are having a problem with storage space, you can move all of your files to an external disk.
For example, I have a USB 5TB external drive called /d12. So, I did this (while gPodder is not running):

mkdir -p /d12/podcasts/gPodder
cd ~/gPodder
mv -iv Downloads /d12/podcasts/gPodder
ln -s /d12/podcasts/gPodder/Downloads Downloads

Then restart gPodder.

I believe my gPodder configuration is corrupted - how do I start out with a fresh config?
--------------------------------------------------------------------------------

gPodder stores all its settings in `gPodder` under your home directory
(e.g. `/home/yourname/gPodder/`). To restart with a fresh config, quit
gPodder, remove the folder `~/gPodder/` and all its contents and
re-start gPodder. All your settings and channel subscriptions will be
lost and you can start out with a fresh config. If you changed the
location of your download folder before you have to delete the gPodder
folder in your self defined location

How do I change the download directory?
-----------------------------------

You can find the answer in the [user manual](user-manual.html#changing-the-downloads-folder-location-and-the-gpodder-home-folder).

How do I subscribe to channels that require HTTP authentication?
----------------------------------------------------------------

Simply add your username and password into the URL when adding a
channel. gPodder will automatically see the provided authentication data
and use it to authenticate to the web server. The syntax is
`http://USERNAME:PASSWORD@example.org/files/feed.xml`.

If your user name consists of an email and the authentication don't work
you have to upgrade to gPodder 3.x

gPodder doesn't start on Windows
--------------------------------------------------------------

Please try uninstalling gPodder and re-installing. If it doesn't solve it,
see the [Windows specific section](windows.md) of the documentation.
