require 'rake/testtask'
require 'find'
require 'bundler/gem_tasks'

desc 'Run tests'
task :default => :test

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'Display inventory of all files'
task :inventory do
  Find.find('../todolist_project') do |name|
    next if name.include?('/.') # Excludes files and directories with . names
    puts name if File.file?(name)
  end
end