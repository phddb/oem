desc "Commit both jekyll code and static site to their two github repos. Usage 'rake deploy['venice_updates']'"
task :deploy, [:comment] do |task,args|
  cmd1 = "git commit -am '#{args[:comment]}'; git push origin master"
  puts cmd1
  `#{cmd1}`

  cmd2 = "jekyll build; cd _site; git add .; git commit -am #{args[:comment]}; git push origin master"
  puts cmd2
  `#{cmd2}`
end
