require 'awesome_print'
require 'pry'

task :default do
  puts `CLICOLOR_FORCE=1 scss-lint`
  abort if $?.exitstatus != 0
  Dir.glob('scss/*.scss').each do |file|
    puts `sass #{file}:static/css/#{File.basename(file, '.*')}.css`
  end
  puts `hugo`
end