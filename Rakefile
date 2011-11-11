require 'rubygems'
require 'bundler/setup'
require "bundler/gem_tasks"
require 'rspec/core/rake_task'
require 'cucumber/rake/task'

RSpec::Core::RakeTask.new do |t|
  t.pattern = 'spec/**/*_spec.rb'
end

Cucumber::Rake::Task.new(:cucumber) do |t|
  t.fork = true
  t.cucumber_opts = ['--format', (ENV['CUCUMBER_FORMAT'] || 'progress')]
end

desc "Default: run the cucumber scenarios"
task :default => [:spec, :cucumber]

