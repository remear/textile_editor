require 'rake'
require 'rake/gempackagetask'
require 'rake/testtask'
require 'rake/rdoctask'

begin
  require 'jeweler'

  Jeweler::Tasks.new do |s|
    s.name = 'textile-editor'
    s.author = "Ben Mills"
    s.email = "ben@unfiniti.com"
    s.summary = "Provide textile toolbar to textareas"
    s.homepage = "http://unfiniti.com"
    
    s.test_files = Dir['test/**/*']
  end
rescue LoadError
  puts "Jeweler not installed."
  exit 1
end


desc 'Default: run unit tests.'
task :default => :test

desc 'Test the textile_editor plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for the textile_editor_helper plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'TextileEditor'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
