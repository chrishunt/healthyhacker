JEKYLL_DIR = "/Users/chris/Dropbox/src/healthyhacker/jekyll"

desc 'Build site and update static files'
task :build do
  if Dir.pwd != JEKYLL_DIR
    puts "You are in the wrong directory."
    next
  end

  find_command = 'find .. \
    -mindepth 1           \
    -maxdepth 1           \
    ! -name ".git"        \
    ! -name "jekyll"      \
    ! -name ".gitignore"  \
    ! -name ".nojekyll"'

  system find_command
  puts "\nAre you sure you want to delete all these? ^^"

  if STDIN.gets.strip == "yes"
    system 'bundle exec jekyll build'
    system "#{find_command} | xargs rm -r"
    system 'cp -r _site/* ../'
  else
    puts 'Thank goodness I asked!'
  end
end

desc 'Take site offline'
task :offline do
  if Dir.pwd != JEKYLL_DIR
    puts "You are in the wrong directory."
    next
  end

  system 'cp ../offline.html ../index.html'
end
