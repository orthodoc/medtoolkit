require 'html-proofer'

task :test do
  sh "bundle exec jekyll clean"
  sh "bundle exec jekyll build --config=_config.yml,_config_prod.yml"
  HTMLProofer.check_directory("./_site", {
    :url_ignore => [/linkedin.com/]
  }).run
end
