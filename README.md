# NAME

RT-Extension-OneClickClose - sets status of a given Ticket to resolved
and returns to the previous Search/Results page

# DESCRIPTION

Sometimes it is cumbersome to go through several pages and to close
a ticket, OneClickClose resolves a ticket and returns to the previous
Search Page. Just add AfterSubmit=1 to the "Close" Link

# RT VERSION

Works with RT 4.2

# INSTALLATION

- `perl Makefile.PL`
- `make`
- `make install`

    May need root permissions

- Edit your `/opt/rt4/etc/RT_SiteConfig.pm`

    If you are using RT 4.2 or greater, add this line:

        Plugin('RT::Extension::OneClickClose');

    For RT 4.0, add this line:

        Set(@Plugins, qw(RT::Extension::OneClickClose));

    or add `RT::Extension::OneClickClose` to your existing `@Plugins` line.

    to use it use an URL like this

    '<B><A HREF="\_\_WebPath\_\_/Ticket/Update.html?Status=resolved&SubmitTicket=1&id=\_\_id\_\_&AfterSubmitReturn=1">OneClickClose</a></B>/TITLE:OneClickClose'

- Clear your mason cache

        rm -rf /opt/rt4/var/mason_data/obj

- Restart your webserver

# AUTHOR

Mark Hofstetter University of Vienna  <mark.hofstetter@univie.ac.at>

# BUGS

All bugs should be reported via web to

    L<https://github.com/MarkHofstetter/RT-Extension-OneClickClose/issues>.

# LICENSE AND COPYRIGHT

This software is Copyright (c) 2015 by Mark Hofstetter

This is free software, licensed under:

    The GNU General Public License, Version 2, June 1991
