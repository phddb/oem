desc "Commit both jekyll code and static site to their two github repos. Usage 'rake deploy['venice_updates']'"
task :deploy, [:comment] do |task,args|
  cmd1 = "git commit -am '#{args[:comment]}'; git push origin master"
  puts "\n> #{cmd1}\n"
  `#{cmd1}`

  cmd2 = "jekyll build; cd _site; echo 'www.oneequallmusick.org' | tee CNAME; git add .; git commit -am '#{args[:comment]}'; git push origin master"
  puts "\n> #{cmd2}\n"
  `#{cmd2}`
end
