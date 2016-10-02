require "bundler/gem_tasks"
begin
  require "chefstyle"
  require "rubocop/rake_task"
  RuboCop::RakeTask.new(:style) do |task|
    task.options << "--display-cop-names"
  end
rescue LoadError
  STDERR.puts "\n*** chefstyle not available. (sudo) gem install chefstyle to run unit tests. ***\n\n"
end

task default: [:spec, :style]
