require 'redcarpet'

task :html do
  buffer   = ""
  markdown = Redcarpet::Markdown.new(Redcarpet::Render::HTML)

  Dir["./posts/*.md"].each_with_index do |file, i|
    buffer << "<h1>##{i}</h1>\n"

    data = File.read(file)
    html = markdown.render(data)

    buffer << html
  end

  puts buffer
end