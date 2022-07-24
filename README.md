# hcilab.github.io
The webpage for the UNB HCI Lab.


## Maintaining and Editing

### Requirements

Ruby - https://rubyinstaller.org/downloads/

RubyGEMs - https://rubygems.org/pages/download

Jekyll - https://jekyllrb.com/docs/installation/

Bundler - https://bundler.io/

CMake and/or Make seem to not be real requirements.


Guide: https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll

### Setup & Dev

Run:
`bundle update github-pages`
`bundle install`

If an error appears, run `gem install nokogiri` then the two lines above. This should already work with the above, but just in case.

Additionally, due to using Ruby 3 and some of these "gems", in order to build and serve it locally, we had to add webrick to the gemfile. Do not remove this.

To locally serve and test:
`bundle exec jekyll serve`

If this fails, due to something like "cannot load such file", follow the workaround here:
https://github.com/jekyll/jekyll/issues/8523

To edit the site, do not edit anything under _site folder. This is the built version of the website and is local only. Instead, edit appropriate files in _includes, _layouts and then root-level files as needed.

### Misc

This site uses a modified version of the **Agency Jekyll Theme**

To edit/add members, projects, or some other site settings, you can do so via the **_config.yml** file. This won't update live when you serve the jekyll site, so just ctrl+c on the terminal and re-run the serve command if you update anything here.

Publications should auto populate based on what is in _publications folder.

Note: When building locally, resources and links/anchors will work appropriately, however if pushing to a private fork of the repository on your own github account, they may not. Any url's or anchors from say, the nav bar, will require you to put manually into the url /hcilab.github.io after your username.github.io. Some resources won't be located such as if they are in the CSS file, unless it's rendered as a variable coming from _config.yml.
