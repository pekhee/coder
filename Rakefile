require "fileutils"

namespace :data do
  task :gen do
    tmp = Dir.mktmpdir "coder"
    puts tmp
    Dir.glob("*").each do |f|
      File.write "#{tmp}/#{f}", `./tokenizer #{f}`
    end
  end

  task :clean do
    Dir.glob("/tmp/coder*").each {|f| FileUtils.rm_rf f}
  end
end
