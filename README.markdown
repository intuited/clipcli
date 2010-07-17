clipcli
=======

Lightweight Python command-line interface to the GTK clipboard.

Dependencies
------------

- argparse:
  Included with Python 2.7; otherwise installable via

      easy_install argparse

Usage
-----

clipcli [-h] [-f FILE] [-d] [-l] [TARGET]

positional arguments:
  TARGET                display the contents of this target

optional arguments:
  -h, --help            show this help message and exit
  -d, --debug           enable debug tracing
  -f FILE, --file FILE  the file to which output will be directed
  -l, --list            list available targets

Examples
--------

These examples were created
after copying from Chrome the words "The argparse module"
at the beginning of the [argparse documentation]
[http://docs.python.org/library/argparse.html].

    $ clipcli -l
    TIMESTAMP
    TARGETS
    MULTIPLE
    COMPOUND_TEXT
    STRING
    TEXT
    UTF8_STRING
    text/html
    text/plain

    $ clipcli text/plain
    The argparse module

    $ clipcli text/html | tidy -c -q -i 2>/dev/null
    <!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">

    <html>
    <head>
      <meta name="generator" content=
      "HTML Tidy for Linux (vers 25 March 2009), see www.w3.org">
      <meta http-equiv="content-type" content=
      "text/html; charset=us-ascii">

      <title></title>
      <style type="text/css">
    span.c2 {-webkit-border-horizontal-spacing: 0px; -webkit-border-vertical-spacing: 0px; -webkit-text-decorations-in-effect: none; -webkit-text-size-adjust: auto; -webkit-text-stroke-width: 0px; border-collapse: separate; color: rgb(0, 0, 0); font-family: 'Liberation Serif'; font-size: medium; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; line-height: normal; orphans: 2; text-align: auto; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px}
      tt.c1 {background-color: transparent; padding-top: 0px; padding-right: 1px; padding-bottom: 0px; padding-left: 1px; font-size: 0.95em; font-weight: bold;}
      </style>
    </head>

    <body>
      <span class=
      "Apple-style-span Apple-style-span c2">The<span class="Apple-converted-space">&Acirc;&nbsp;</span><tt class="xref docutils literal c1"><span class="pre">argparse</span></tt><span class="Apple-converted-space">&Acirc;&nbsp;</span>module</span>
    </body>
    </html>
