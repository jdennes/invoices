require 'date'

desc "Generate your invoice for the current month"
task :invoice do
  now  = DateTime.now
  # Find the last day in the current month
  last = DateTime.civil now.year, now.month, -1

  filename = File.join(
    File.dirname(__FILE__),
    "_posts",
    last.strftime('%Y-%m-%d-invoice.markdown'))

  monthly_data = 
"---
layout:         post
title:          \"Invoice – #{last.strftime('%B, %Y')}\"
date:           #{last.strftime('%Y-%m-%d 10:00:00')}
invoice_number: \"#{last.strftime('%Y%m-GITHUB')}\"
period:         \"#{last.strftime('%B, %Y')}\"
---
"

  invoice_template = File.open(
    File.join(
      File.dirname(__FILE__),
      "invoice-template.md"), "r").read

  # Glue the monthly data and the invoice template together, and save
  # the invoice.
  File.open(filename, 'w') { |f| f.write(monthly_data + invoice_template) }
  p "Generated your monthly invoice. Saved to: #{filename}"
end

desc "Run the invoices app"
task :run do
  sh "jekyll serve --watch"
end

task :default => :run
