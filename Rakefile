begin
  require 'slidedown'
rescue LoadError
end


task :default => ["slides"]

desc "Generate HTML for all slides"
task :slides do
  slides = FileList['slides/*.md']
  
  slides.each do |slide|
    puts slide
    `slidedown #{slide} > #{slide.chop.chop}html`
  end
end
