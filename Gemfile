source "https://rubygems.org"

# (Optional) declare Ruby used in Actions and locally
# ruby "~> 3.2"

gem "jekyll", "~> 4.3"
gem "jekyll-theme-chirpy", "~> 7.3"

group :jekyll_plugins do
  gem "jekyll-paginate"
  gem "jekyll-redirect-from"
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
  gem "jekyll-include-cache"
  # gem "jekyll-archives" # Only if you add the archive layouts back in
end

group :development do
  gem "webrick", "~> 1.8" # for `bundle exec jekyll serve` on Ruby 3+
end

platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]
