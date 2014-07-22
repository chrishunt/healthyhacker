desc 'Build site and update static files'
task :build do
  system 'jekyll build'
  system '
    find ..                 |
    grep -v "^..$"          |
    grep -v "^../.git"      |
    grep -v "^../jekyll"    |
    grep -v "^../.nojekyll" |
    xargs rm -r'
  system 'cp -r _site/* ../'
end

desc 'Take site offline'
task :offline do
  system 'cp ../offline.html ../index.html'
end
