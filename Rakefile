# require 'html-proofer'

desc "Clean the old builds"
task :clean do
  sh "bundle exec jekyll clean"
end

desc "Build the site"
task :build => [:clean] do
  puts "Building site"
  out = `bundle exec jekyll build --config=_config.yml`

  if $?.to_i == 0
    puts  "Building succeeded"
  else
    abort "Building failed: #{$?.to_i}\n" +
          "#{out}\n"
  end
end

desc "Test the build"
task :test => [:build] do
  sh "htmlproofer --url-ignore \"/linkedin.com/\" ./_site"
end

desc "Publish to S3"
task :publish => :build do
  puts "Publishing to S3"
  puts `s3_website push`
  puts "Published"
end

task :default => [:test]
