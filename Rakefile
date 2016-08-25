require 'html-proofer'

task :test do
    sh "bundle exec jekyll build"
    opts = {
        :check_html => true,
        :empty_alt_ignore => true,
        :only_4xx => true,
        :url_ignore => ["#", /^(https?\:\/\/)?(www\.)?youtube\.com\/.+$/]
    }
    HTMLProofer.check_directory('./_site', opts).run
end