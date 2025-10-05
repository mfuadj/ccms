source "https://rubygems.org"

gem "jekyll", "~> 4.3.3"
gem "jekyll-theme-chirpy", "~> 7.3"
gem "webrick", "~> 1.8" # for local `jekyll serve` on Ruby 3+

group :jekyll_plugins do
  gem "jekyll-include-cache"
end

platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]