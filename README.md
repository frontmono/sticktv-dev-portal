# sticktv-dev-portal

## Develop

Steemit Portal was built with [Jekyll](http://jekyllrb.com/) version 3.1.6, but should support newer versions as well.

Install the dependencies with [Bundler](http://bundler.io/):

~~~bash
$ bundle install
~~~

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

You can now test locally at
~~~bash
http://localhost:4000
~~~

Optionally, when running `jekyll` commands through Bundler, append `--host x.x.x.x` with the external IP address of the server to be able to connect remotely:
~~~bash
$ bundle exec jekyll serve --host x.x.x.x
~~~
~~~make
make 
~~~


