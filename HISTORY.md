## 0.2.8

* Properly parse the email original when it's attached in the last part of a multipart bounce email (@blainejohnson17, livebg/bounce_email#12). Read more about [the issue and the reasoning behind the fix here](https://github.com/livebg/bounce_email/pull/12#issuecomment-312431646).

## 0.2.7

* Extract and save the bounced email's date field in the email original (@blainejohnson17, livebg/bounce_email#11)

## 0.2.6

* Replaced 'X-Original-To' header with 'X-Failed-Recipients' (@saghaulor, livebg/bounce_email#10)
* Properly extract "To" from original email (@saghaulor, livebg/bounce_email#8)

## 0.2.5

* Fix parsing of original mail (@saghaulor, livebg/bounce_email#6)

## 0.2.4

* Parse and reassign message-ID, to, from, and subject from original mail
  (@saghaulor, livebg/bounce_email#5)

## 0.2.3

* add support for Gmail bounces (@saghaulor, livebg/bounce_email#4)

## 0.2.2

* fix a failure when an email has no subject header

## 0.2.1

* fix Ruby 1.8.7 compatibility

## 0.2.0

* new versioning due to new gem being published

## 0.1.1 2011-09-01

* extended #bounced? to consider error_status and diagnostic_code as well
* updated external gems

## 0.1.0 2011-05-27

* make use of bounce parsing in Mail gem
* renamed method to be compatible with Mail Gem
* more tests and cleanup
* forward message call to mail object if method is missing
* updated doc
* gemspec cleanup

## 0.0.1 2009-02-15

* 1 major enhancement:
* Initial release
