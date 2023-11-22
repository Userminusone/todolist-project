require "bundler/gem_tasks"
require "rake/testtask"
require 'find'

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'Lists every file in your project'
task :list do
  Find.find(".") do |path|
    next if path.include?('/.')
    puts "todolist_project#{path[1..]}" if File.file?(path)
  end
end
