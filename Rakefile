require "rake"

namespace :tex do
  desc "Generate LaTeX file"
  task :generate do
    puts "Generating LaTeX file from Markdown"
    system("pandoc -s -w context README.md -o resume.tex")
    puts "Done"
  end
end

namespace :pdf do
  desc "Generate PDF file"
  task :generate do
    puts "Generating PDF file from LaTeX"
    system("pandoc -s --latex-engine=xelatex -V CJKmainfont='PingFang SC Regular' -V mainfont='Monaco' -V geometry:margin=1in README.md  -o resume.pdf")
    puts "Done"
  end
end
