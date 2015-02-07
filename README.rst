mutt-notmuch-py
===============

This is a version of the original mutt-notmuch script with some tweaks to work with replica of my IMAP folders.

It will interactively ask you for a search query and then symlink the matching
messages to ``$HOME/.cache/mutt_results``.

Add this to your muttrc.

::

    macro index / "<enter-command>unset wait_key<enter><shell-escape>mutt-notmuch.py -G PATH_TO_Maildir<enter><change-folder-readonly>~/.mutt/cache_mutt_results<enter>" \
            "search mail (using notmuch)"

This script overrides the ``$HOME/.cache/mutt_results`` each time you run a
query.

Install this by adding this file somewhere on your PATH.

Only tested on Linux.

License
-------

BSD, short and sweet
