# frozen_string_literal: true

source "https://rubygems.org"

gemspec

gem "jekyll-seo-tag"
gem "jekyll-sitemap"
gem "jekyll-remote-theme"

# https://github.com/jekyll/jekyll/issues/8523#issuecomment-751409319
# When running locally, we run into the following error —
# `require': cannot load such file -- webrick (LoadError)
# adding this avoids it
gem "webrick"

# adding the following gems to support removal of "github-pages" dependency
gem "jemoji"
gem "kramdown-parser-gfm"

# Windows directory monitoring
gem 'wdm', '>= 0.1.0' if Gem.win_platform?
