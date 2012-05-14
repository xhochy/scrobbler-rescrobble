require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "scrobbler-rescrobble"
    gem.summary = %Q{Scrobbles tracks that one user has heard to an other user's account}
    gem.email = "uwelk@xhochy.org"
    gem.homepage = "http://github.com/xhochy/scrobbler-rescrobble"
    gem.authors = ["Uwe L. Korn"]
    # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
  end

rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |t|
  t.pattern = 'spec/*_spec.rb'
end
task :default => :spec

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  if File.exist?('VERSION.yml')
    config = YAML.load(File.read('VERSION.yml'))
    version = "#{config[:major]}.#{config[:minor]}.#{config[:patch]}"
  else
    version = ""
  end

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "scrobbler-rescrobble #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

