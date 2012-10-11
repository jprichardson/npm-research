Node.js - npm-research
================

Nice little utility to help you research NPM packages.


Why?
----

You don't want to always reinvent the wheel do you? Neither do I. Well, this will help you research NPM packages a bit more. It does this by performing `npm search` and then parsing out the package names and retreiving the `homepage` and `repository` urls. It Then opens these up in your browser. This way you can see how many stars the project has and investigate the quality of the code and documentation.



Installation
------------

    npm install -g npm-research



Usage
------

    $ npm-research


    npm-research [0.0.1]

      Usage: npm-research [some search terms...]



Example
-------

    $ npm-research string csv

    Searching...

      Opening https://github.com/adioo/a-csv...
      Opening https://github.com/trentm/node-csvrow...
      Opening http://stringjs.com...

    Done.


Todo
----

I'll probably add more options in the coming months, such as sorting by Github stars, not opening anything in the browser, favorite authors, etc.


License
-------

(MIT License)

Copyright 2012, JP Richardson  <jprichardson@gmail.com>


