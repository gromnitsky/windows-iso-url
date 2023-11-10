https://www.youtube.com/watch?v=5jnmDNxSiAo

There are some scripts on Github that supposedly do the similar job,
but I believe this one is the smallest:

~~~
$ grep -Ev '^#|^$' windows-iso-url | wc -l
45
~~~

It's actually a GNU Make's makefile:

~~~
$ head -3 windows-iso-url
#!/usr/bin/make -sf
# requires bash, 'dnf install dialog curl' and 'gem install nokogiri'
# to debug: make -f windows-download v=1
~~~

## Usage

This should print a list of URLs:

    $ mkdir tmp && cd tmp
    $ windows-iso-url

You only need to run in a tmp dir, because it saves its state in a
bunch of `step*` text files.

## Loicense

MIT
