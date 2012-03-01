#!/usr/bin/env rake
# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require File.expand_path('../config/application', __FILE__)
require 'rubygems'

task :default => :serve

###########################################################################
# Rake Tasks
###########################################################################
desc "For a first install, rvm creates an empty gemset mcl_auth. Run rake :install to install & run bundler, populating that gemset."
task :install do
	sh "gem install bundler"
	sh "bundle install"
end

desc "Serve on localhost with port 4000, dev environment"
task :serve do
  sh "rails s --binding 127.0.0.1 --port 4000 --env development"
end

OmniauthPure::Application.load_tasks

