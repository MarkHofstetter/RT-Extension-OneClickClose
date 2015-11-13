# NAME

RT-Extension-OneClickClose - \[One line description of module's purpose here\]

# DESCRIPTION

\[Why would someone install this extension? What does it do? What problem
does it solve?\]

# RT VERSION

Works with RT \[What versions of RT is this known to work with?\]

\[Make sure to use requires\_rt and rt\_too\_new in Makefile.PL\]

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

- Clear your mason cache

        rm -rf /opt/rt4/var/mason_data/obj

- Restart your webserver

# AUTHOR

Best Practical Solutions, LLC <modules@bestpractical.com>

# BUGS

All bugs should be reported via email to

    L<bug-RT-Extension-OneClickClose@rt.cpan.org|mailto:bug-RT-Extension-OneClickClose@rt.cpan.org>

or via the web at

    L<rt.cpan.org|http://rt.cpan.org/Public/Dist/Display.html?Name=RT-Extension-OneClickClose>.

# LICENSE AND COPYRIGHT

This software is Copyright (c) 2015 by Mark Hofstetter

This is free software, licensed under:

    The GNU General Public License, Version 2, June 1991
