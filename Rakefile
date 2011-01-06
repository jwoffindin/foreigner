require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'
require 'rspec/core/rake_task'

desc 'Default: run specs.'
task :default => :spec

desc 'Run the specs'
Rspec::Core::RakeTask.new(:spec) do |t|
  #t.spec_opts = ['--colour --format progress --loadby mtime --reverse']
  #t.spec_files = FileList['spec/**/*_spec.rb']
end

desc 'Generate documentation for the foreigner plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'Foreigner'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gemspec|
    gemspec.name = "jwoffindin-foreigner"
    gemspec.summary = "Foreign keys for Rails migrations for PostgreSQL, MySQL and Sqlite3. Based on sparkfly-foreigner"
    gemspec.description = "Allows you to add foreign keys to your migrations and enforce them"
    gemspec.email = "john.woffindin@sla-mobile.com.my"
    gemspec.homepage = "http://github.com/jwoffindin/foreigner"
    gemspec.authors = ["Ho-Sheng Hsiao","John Woffindin"]
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler not available. Install it with: gem install jeweler"
end

