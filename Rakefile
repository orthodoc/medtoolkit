# Rake tasks
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
  sh "bundle exec htmlproofer --url-ignore \"/#.*/,/linkedin.com/\" ./_site"
end

desc "Publish to S3"
task :publish => [:build] do
  puts "Publishing to S3"
  sh "bundle exec s3_website push"
  puts "Published"
end

desc "Run a live server"
task :serve do
  puts "Start a live server at 127.0.0.1:4000"
  sh "bundle exec jekyll liveserve"
end

task :default => [:test]
