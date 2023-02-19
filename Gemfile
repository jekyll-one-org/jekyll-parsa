# ------------------------------------------------------------------------------
# ~/Gemfile
# Provides package information to bundle all Ruby gem needed
# for Jekyll and J1 Theme (managed by Ruby Gem Bundler)
#
# Product/Info:
# https://jekyll.one
#
# Copyright (C) 2023 Juergen Adams
#
# J1 Theme is licensed under the MIT License.
# See: https://github.com/jekyll-one-org/j1-template/blob/main/LICENSE.md
# ------------------------------------------------------------------------------

# ------------------------------------------------------------------------------
# Define the (download) source, Ruby GEMs are to be loaded from REMOTE
#
source 'https://rubygems.org'

# ------------------------------------------------------------------------------
# Jekyll
# ------------------------------------------------------------------------------
# NOTE:
# J1 Theme is using Jekyll v4.0 and above
#
# ------------------------------------------------------------------------------
#
gem 'bundler'
gem 'jekyll', '~> 4.0'
gem "kramdown", ">= 2.3.0"

# ------------------------------------------------------------------------------
# GEM needed for the Jekyll and J1 dev environment
#
# NOTE:
# For the build (npm|yarn), J1 Theme is using scss_lint
# for linting the SCSS (Sass) components.
#
# ------------------------------------------------------------------------------
# NOTE:
# scss_lint is based on old gem 'sass', '~> 3.5.5'. A replacement
# is needed (?) for a linter using the new Ruby Sass GEM (sassc)
# gem 'scss_lint', '~> 0.56.0', require: false
#
# ------------------------------------------------------------------------------
gem 'sassc', '~> 2.4'

# ------------------------------------------------------------------------------
# Install Webrick GEM (internally used Web Server) if Ruby V3 is used
#
install_if -> { RUBY_VERSION =~ /3/ } do
  gem 'webrick', '~> 1.7'
end

# ------------------------------------------------------------------------------
# Jekyll Plugins
# If any (additional) Jekyll Plugins are used, they goes here
#
group :jekyll_plugins do
  # Base Jekyll Plugins (required)
  #
  gem 'jekyll-archives'
  gem 'jekyll-paginate'
  gem 'jekyll-seo-tag'
  gem 'jekyll-sitemap'

  # Additional Supporting GEMs (optional)
  #
  # gem 'jekyll-tagging'
end

# ------------------------------------------------------------------------------
# Platform specific GEM
#
# NOTE:
# Windows does not include zoneinfo files (timezone support).
# To provide zoneinfo, tzinfo-data gem is bundled on win platforms
#
# ------------------------------------------------------------------------------
# NOTE:
# Windows Directory Monitor (WDM) required to monitor directories
# for changes
#
# ------------------------------------------------------------------------------
#
install_if -> { Gem.win_platform? } do
  gem 'tzinfo-data'
  gem 'wdm', '>= 0.1.1'
end

# ------------------------------------------------------------------------------
# Timezone support (multi-platform)
#
gem 'tzinfo', '>= 1.2.2'
