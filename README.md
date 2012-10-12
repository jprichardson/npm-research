Node.js - npm-research
================

Nice little utility to help you research NPM packages.


Why?
----

You don't want to always reinvent the wheel do you? Neither do I. Well, this will help you research NPM packages a bit more. It does this by performing `npm search` and then parsing out the package names and retreiving the `homepage` and `repository` urls. It can then open up the repo urls in your browser. This way you can see how many stars the project has and investigate the quality of the code and documentation.



Installation
------------

    npm install -g npm-research



Usage
------

    $ npm-research

    npm-research [0.1.0]

      Usage: npm-research [some search terms...] [options]

      Options:

        -b, --browser   Open repos in browser
        -g, --gte [num]   Only display/open those who have a dependents greater than specified number i.e. more popular



Example
-------

Perform basic research. Find the package name and description. Show the number of packages that depend upon the package. This way you can gauge popularity of the package.


    $ npm-research string csv

    Searching...

              name  deps    description
            a-csv   [0] :  A CSV parsing/stringify module
           csvrow   [0] :  parse a CSV row string
           string  [16] :  string contains methods that aren't included in the vanilla JavaScript string such as escaping HTML, decoding HTML entities, stripping tags, etc.

    Done.



Example 2
---------

Perform research, but filter out projects that have less than `1` depenedent. Open the repositories in your browser so that you can investigate the code.

    $ npm-research string csv --gte 1 --browser

    Searching...

              name  deps    description
           string  [16] :  string contains methods that aren't included in the vanilla JavaScript string such as escaping HTML, decoding HTML entities, stripping tags, etc.

    Done.



Misc.
----

After each NPM package information is downloaded, it is then cached for two days. This information can be found in `$HOME/.npm-research/packages.json`.



Todo
----

Unfortunately `npm search` is slows balls and TJ Holowaychuk's `npm-search` isn't working right now. Maybe leverage Google search to speed things up?



License
-------

(MIT License)

Copyright 2012, JP Richardson  <jprichardson@gmail.com>


