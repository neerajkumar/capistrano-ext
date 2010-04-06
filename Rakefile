begin
  require 'echoe'
rescue LoadError
  abort "You'll need to have `echoe' installed to use capistrano-ext's Rakefile"
end

require "./lib/capistrano/ext/version"

version = Capistrano::Ext::Version::STRING.dup
if ENV['SNAPSHOT'].to_i == 1
  version << "." << Time.now.utc.strftime("%Y%m%d%H%M%S")
end

Echoe.new('capistrano-ext', version) do |p|
  p.changelog        = "CHANGELOG.rdoc"

  p.author           = "Jamis Buck"
  p.email            = "jamis@jamisbuck.org"
  p.summary          = "Useful task libraries and methods for Capistrano"
  p.url              = "http://www.capify.org"

  p.need_zip         = true

  p.dependencies     = ["capistrano >=1.0.0"]
end