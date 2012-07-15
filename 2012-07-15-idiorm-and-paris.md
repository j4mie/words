# Idiorm and Paris: Seeking a new maintainer

[Jamie Matthews](http://twitter.com/j4mie), July 15 2012.

*tl;dr: Idiorm and Paris are officially looking for a new maintainer. If you're interested, please [contact me](mailto:jamie.matthews@gmail.com).*

Back in early 2010, frustrated with the complexity of existing PHP database tools and their unsuitability for quick web application projects, I started work on a deliberately simple, small object-relational mapper. The result was a pair of libraries, [Idiorm](https://github.com/j4mie/idiorm/) and [Paris](https://github.com/j4mie/paris).

They seemed to strike a chord with a certain part of the PHP community, and they have since become my most popular projects on GitHub, with almost 500 and almost 300 watchers respectively.

However, after working hard on them for a year or so, maintenance slowed down and eventually stopped. This was for a few reasons:

* I started my own company, [DabApps](http:/dabapps.com), which took up a lot of the spare time I'd previously spent on open source work.
* I stopped using PHP completely and switched to Python.
* Both tools had reached the point where I was happy with their feature set, and so the motivation to add new features was very much reduced.
* I began to feel that the test suite is inadequate, and no longer felt comfortable with testability of the code.

Since then, the issues and pull requests have piled up, and I've continued to ignore them. I'd like to apologise for this: if you've put in hard work to find and fix and issue in a project, you deserve more than silence for your efforts. **I'm sorry to everyone who's tried to make a contribution over the past year and been ignored**.

I have long held on to the idea that I'd return to Idiorm and Paris at some point in the future, but this is looking increasingly unlikely, due to time pressures and my lack of motivation to write PHP.

However, I'd love to see the code continue to be used and to grow. For this reason, **I'd like to find a new maintainer for Idiorm and Paris**, who I'd give full commit access to the repositories.

Ideally, this will be someone who's a heavy user of the library, and understands the code inside out. More importantly, it should be someone who "gets" the motivation for building a *minimalist* database tool for PHP. There are some features that it just doesn't make sense to add, because they would compromise the simplicity of the code.

Here's an outline of what I think the first steps for the next maintainer would be:

* Identify any critical bugs in the list of open issues. If there is already a corresponding pull request that fixes the issue, it should be reviewed and merged.
* Publish the libraries on [Packagist](http://packagist.org/).
* Triage the outstanding feature requests and prioritise them to decide which of them make sense to add to Idiorm. Review any of these that include pull requests, and merge. Close any that don't make sense, with an explanation of why.
* Improve the test suite. Currently, the tests only cover the generated SQL (which is better than nothing) but ideally they'd also cover higher-level functional behaviour - does the correct data get loaded into the correct objects, and is it available by accessing the correct properties? Perhaps moving to PHPUnit (and away from my own hand-hacked test code) would be a good idea.
* Make decisions about the long-term future of the library. At what point does it make sense to drop support for PHP 5.2? Should multiple database connectivity be added? Can this be done without changing the API much? Should the libraries be converted to use the [PSR-1 coding standard](https://github.com/pmjones/fig-standards/blob/psr-1-style-guide/proposed/PSR-1-basic.md)?

If you're interested in taking over maintenance of Idiorm and Paris, please get in touch by emailing me at [jamie.matthews@gmail.com](mailto:jamie.matthews@gmail.com). Include a couple of paragraphs with your thoughts on the library, how you use it, and how you'd proceed.

Thanks!
