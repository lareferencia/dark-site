source "https://rubygems.org"

# This configuration is optimized for GitHub Pages
# For local development, you can use: bundle exec jekyll serve

# GitHub Pages compatible dependencies
gem "github-pages", group: :jekyll_plugins

# Required for Ruby 3.0+
gem "webrick", "~> 1.8"

# Custom project tools (not used by GitHub Pages)
gem 'thor'
gem 'stringex'

# Plugins supported by GitHub Pages
group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-seo-tag"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
