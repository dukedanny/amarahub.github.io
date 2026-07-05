#!/usr/bin/env rake

desc 'Initial setup'
task :bootstrap do
  puts 'Installing Bundle...'
  puts `bundle install`
end

desc 'Build the site (category pages generated when PRODUCTION=YES)'
task :build do
  puts `bundle exec jekyll build`
end

desc 'Serve the site locally at http://localhost:4000'
task :serve do
  puts 'Starting local server (category pages skipped for speed)...'
  system 'bundle exec jekyll serve'
end

task default: :serve
