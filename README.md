Welcome to my personal repository.

Ilias Bartolini blog made with jekyll

### Run and build

Prerequisites
~~~
gem install bundler
bundle install
~~~

Running it locally
~~~
bundle exec jekyll serve
~~~

The `.gitlab-ci.yml` file will automatically publish this website at <http://fab.academany.org/2018/labs/barcelona/students/ilias-bartolini/>

### Managing images

We have a personal quota of 3MB/week to keep small our .git repository size.  
This is a small command to resize images in batch.  
~~~
mkdir resized && mkdir _original && find . -maxdepth 1 -iname '*.[jp][pn]g' | xargs -L1 -I{} convert -resize 600 -quality 50 "{}" resized/"{}".jpg && mv *.[jp][pn]g _original/
~~~

The `_original` folder is not served by jekyll and is filtered in `.gitignore`. Files will be kept only locally as reference.
