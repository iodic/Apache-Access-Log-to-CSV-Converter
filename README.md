 ======================================
 = Apache Access Log to CSV Converter =
 ======================================

Takes an Apache log of the form:

```
123.45.67.890 - - [23/Sep/2011:12:13:32 -0400] "GET / HTTP/1.1" 200 2279 "http://www.some-referrer.com/referral-page/" "Some User Agent 1.0.1"
```

and converts it to:

```
"IP","Time","Request_Type","Path","Response","Referral_Domain","Referral_Path","User_Agent"
"123.45.67.890","2011-09-23 12:13:32","GET","/","200","http://www.some-referrer.com/","/referral-page/","Some User Agent 1.0.1"
```

Note that this was developed for my logs, so if yours are in a different format
you'll have to tweak the regular expressions. Hey, at least it's a start for you :)

 ================
 = INSTRUCTIONS =
 ================

Use it via command line as...
`path/to/script.php relative/path/to/input_file relative/path/to/output_file.csv`

e.g.:
`/bin/apache_log_to_csv_converter.php access_log access_log.csv`

 ===========
 = License =
 ===========
Copyright (c) 2011 Matt Boynes <m@boyn.es>

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
