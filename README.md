https://www.youtube.com/watch?v=aHMvY8FMMH0

There are some scripts on GitHub that supposedly perform a similar
job, but I believe this one is the smallest:

~~~
$ grep -Ev '^#|^$' windows-iso-url | wc -l
28
~~~

It's actually a makefile.

## Usage

This should print a list of URLs:

    $ ./windows-iso-url

You may need to run it in a temporary directory because it saves its
state in a bunch of `step*` text files (which it autoremoves).

## Loicense

MIT
