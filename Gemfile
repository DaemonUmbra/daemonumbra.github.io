source "https://rubygems.org"

# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# This will help ensure the proper Jekyll version is running.
# Happy Jekylling!
# gem "jekyll", "~> 3.8.3"

# This is the default theme for new Jekyll sites. You may change this to anything you like.
gem "jekyll-theme-hacker"

# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
gem "github-pages", group: :jekyll_plugins

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "octokit"
  gem "jekyll-github-metadata"
  gem "jekyll-feed"
  gem "jekyll-redirect-from"
  gem "jekyll-sitemap"
  gem "jekyll-mentions"
end

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.0" if Gem.win_platform?

# Undeclared Transitive Dependencies
gem "webrick"

# Additional Bits & Bobs
gem "dotenv"

# Security Vulnerability Fixes
gem "nokogiri", ">= 1.10.4"
gem "rubyzip", ">= 2.0.0"
gem "activesupport", ">= 4.1.11"
gem "kramdown", ">= 2.3.0"
