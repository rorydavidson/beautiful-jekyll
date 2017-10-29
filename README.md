# My GitHub Pages

Pretty much built on the shoulders of others, and based upon **Beautiful Jekyll**, *Copyright 2016 [Dean Attali](http://deanattali.com)*

My change is to make the magic happen using travis to build the [source branch](https://github.com/rorydavidson/rorydavidson.github.io/tree/source) and deploy as static HTML into master.

I used [travis.yml](https://github.com/rorydavidson/rorydavidson.github.io/blob/source/.travis.yml) set up based upon a [deploy script](https://github.com/rorydavidson/rorydavidson.github.io/blob/source/bin/deploy) which goes into the generated site directory and pushes it to the master branch of the repository.

So any changes I make on the source branch that are pushed to GutHub are picked up by travis, and the static pages are automatically generated and pushed back to master so that the pages then get displayed by GitHub without any problems.

For more details on Beautiful Jekyll, go see the excellent [README file with great instructions](https://github.com/daattali/beautiful-jekyll/blob/master/README.md).
