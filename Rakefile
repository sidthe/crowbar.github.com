require "bundler"
Bundler.setup(:default)

require "jekyll"
require "tmpdir"

desc "Generate website"
task :generate do
  Dir.mkdir("_site") unless File.directory? "_site"
  
  Jekyll::Site.new(
    Jekyll.configuration({
      "source" => ".",
      "destination" => "_site"
    })
  ).process
end

desc "Publish website"
task :publish => [:generate] do
  Dir.mktmpdir do |tmp|
    Fileutils.cp_r "_site/", tmp
    Dir.chdir tmp

    system "ls -ali #{tmp}"

    # system "git init"
    # system "git add ."

    # system "git commit -m 'Site updated at #{Time.now.utc}'"
    # system "git remote add origin git@github.com:crowbar/crowbar.github.com.git"
    # system "git push origin master --force"
  end
end
