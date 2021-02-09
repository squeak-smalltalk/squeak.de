require 'html-proofer'

task :test do
    sh "bundle exec jekyll build"
    opts = {
        :check_html => true,
        :empty_alt_ignore => true,
        :only_4xx => true,
        :url_ignore => [
          "#",
          /^(https?\:\/\/)?(www\.)?youtube\.com\/.+$/,
          "http://2denker.de/",
          /^(https?\:\/\/)?(www\.)?twitter\.com\/.+$/,
          /^(https?\:\/\/)?(www\.)?zoom\.us\/.+$/ ],
        :typhoeus => {
          :ssl_verifypeer => false,
          :ssl_verifyhost => 0 }
    }
    HTMLProofer.check_directory('./_site', opts).run
end