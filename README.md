# NAME

PerlX::QuoteOperator::URL - Quote-like operator returning http request for the URL provided.

# VERSION

Version 1.02

# SYNOPSIS

    use PerlX::QuoteOperator::URL;

    my $content = qURL( http://transfixedbutnotdead.com );   # does HTTP request

# DESCRIPTION

This module provides a Quote-like operator which returns a HTTP request using the  LWP::Simple module.

Please see [PerlX::QuoteOperator](https://metacpan.org/pod/PerlX::QuoteOperator) for more detail on Quote-like operators.

For now here is another example:

    use PerlX::QuoteOperator::URL 'qh';
    use JSON qw(decode_json);

    say decode_json( qh{ http://twitter.com/statuses/show/6592721580.json } )->{text};

    # => "He nose the truth."
    

# EXPORT

By default 'qURL' is exported to calling package/program.

This can be changed by providing a name of your own choice:

    use PerlX::QuoteOperator::URL 'q_http_request';
    

# FUNCTIONS

## import

Standard import subroutine.

# SEE ALSO

NB. This module use to be part of the PerlX::QuoteOperator distro.  It was removed at 0.05 (23rd Feb 2015)

- [PerlX::QuoteOperator](https://metacpan.org/pod/PerlX::QuoteOperator)
- [Acme::URL](https://metacpan.org/pod/Acme::URL)
- [http://transfixedbutnotdead.com/2009/12/16/url-develdeclare-and-no-strings-attached/](http://transfixedbutnotdead.com/2009/12/16/url-develdeclare-and-no-strings-attached/)
- [http://transfixedbutnotdead.com/2009/12/26/couple-of-cpan-pressies/](http://transfixedbutnotdead.com/2009/12/26/couple-of-cpan-pressies/)

# CONTRIBUTORS

Brian Rossmajer (https://github.com/BrianRossmajer) for Directory::Scratch removal patch at 1.01

# AUTHOR

Barry Walsh, `<draegtun at cpan.org>`

# BUGS

Please report any bugs or feature requests to [https://github.com/draegtun/PerlX-QuoteOperator-URL/issues](https://github.com/draegtun/PerlX-QuoteOperator-URL/issues)

# SUPPORT

You can find documentation for this module with the perldoc command.

    perldoc PerlX::QuoteOperator::URL

You can also look for information at:

- Github issues and pull requests

    [https://github.com/draegtun/PerlX-QuoteOperator-URL/issues](https://github.com/draegtun/PerlX-QuoteOperator-URL/issues)

- AnnoCPAN: Annotated CPAN documentation

    [http://annocpan.org/dist/PerlX-QuoteOperator-URL](http://annocpan.org/dist/PerlX-QuoteOperator-URL)

- CPAN Ratings

    [http://cpanratings.perl.org/d/PerlX-QuoteOperator-URL](http://cpanratings.perl.org/d/PerlX-QuoteOperator-URL)

- Search CPAN

    [http://search.cpan.org/dist/PerlX-QuoteOperator-URL/](http://search.cpan.org/dist/PerlX-QuoteOperator-URL/)

# ACKNOWLEDGEMENTS

Inspired by this blog post: [http://ozmm.org/posts/urls\_in\_ruby.html](http://ozmm.org/posts/urls_in_ruby.html) and wanting to learn [Devel::Declare](https://metacpan.org/pod/Devel::Declare)

# DISCLAIMER

This is (near) beta software.   I'll strive to make it better each and every day!

However I accept no liability _whatsoever_ should this software do what you expected ;-)

# COPYRIGHT & LICENSE

Copyright 2015- Barry Walsh (Draegtun Systems Ltd | [http://www.draegtun.com](http://www.draegtun.com)), all rights reserved.

This program is free software; you can redistribute it and/or modify it
under the terms of either: the GNU General Public License as published
by the Free Software Foundation; or the Artistic License.

See http://dev.perl.org/licenses/ for more information.
