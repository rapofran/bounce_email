# bounce-email

This Ruby library is for determining the bounce type of an email message. It determines whether the bounce is hard or soft, if is an "out of office mail", etc.

## Build Status
[![Build Status](https://api.travis-ci.org/livebg/bounce_email.png)](https://travis-ci.org/livebg/bounce_email)

## SYNOPSIS:

Follow this tutorial to handle bounce-emails: [http://keakaj.com/wisdom/2007/08/08/verp-on-rails](http://keakaj.com/wisdom/2007/08/08/verp-on-rails/)

Basic usage:

     require "bounce_email"

     bounce = BounceEmail::Mail.new(STDIN.read)

     # Do something with bounce info
     bounce.bounced? # true/false
     bounce.code # e.g. "5.1.1"
     bounce.reason # e.g. "Something about the address specified in the message caused this DSN."
     bounce.type  #  "Permanent Failure", "Persistent Transient Failure", "Success" -- BounceEmail::TYPE_HARD_FAIL, TYPE_SOFT_FAIL, TYPE_SUCCESS


## Compatibility

Compatible with Ruby 1.8.7, 1.9.x, 2.0.0 and 2.1.0.

## REQUIREMENTS:

[mail](http://rubygems.org/gems/mail) gem is required with `bounce_email` gem.
The `mail` gem is used for primary bounce handling, which catches about 50% of
all bounces. `bounce_email` tries to catch remaining bounce emails.

See discussion here: [https://github.com/mikel/mail/issues/103](https://github.com/mikel/mail/issues/103)

## Other implementations:

  * (PERL) [https://github.com/rjbs/mail-deliverystatus-bounceparser](https://github.com/rjbs/mail-deliverystatus-bounceparser)


## TODO:

  * Mode code cleanup.
  * Don't hardcode comparison strings, move to external file which can be extended easily.
  * More test: extend for more bounces.
  * Is OUT of office type needed? If yes, implement as an optional part.
  * Merge into Mail Gem?

## CONTRIBUTIONS:

Please fork on github & add new conditions under "get_status_from_text" if you discover creative new mailserver responses.

Updated by Pedro Visintin 2010
Updated by Tobias Bielohlawek 2011


## LICENSE:

(The MIT License)

Copyright (c) 2011 Tobias Bielohlawek, Agris Ameriks

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
