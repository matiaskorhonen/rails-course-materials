begin
  require 'slidedown'
rescue LoadError
end


task :default => ["slides"]

desc "Generate HTML for all slides"
task :slides do
  slides = FileList['slides/*.md']
  
  slides.each do |slide|
    print slide
    status = system "slidedown '#{slide}' > '#{slide.chop.chop}html' --template relative"
    puts status ? "\t\tdone" : "\t\tFAILED!"
  end
end
