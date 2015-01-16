# Invoices

This is a very quick Jekyll-based thing which allows me to do monthly invoicing by running `script/invoice`.

To use this yourself, fork and clone, then follow these instructions:

1. Setup:

  ```sh
  $ script/setup
  ```

2. Create your own `_config.yml` file (this will contain sensitive information and is included in `.gitignore`, as is the `_posts` directory where your invoices will exist):

  ```sh
  $ cp _config.yml.example _config.yml
  ```

  Edit your `_config.yml` file. Edit and add as many `invoice_line_items` as you like.

3. Run the app:

  ```sh
  $ script/server
  ```

  That starts the app at [http://localhost:4000](http://localhost:4000). You shouldn't see any invoices there yet though.

4. Generate an invoice:

  Without any arguments, this creates you an invoice for the current month:

  ```sh
  $ script/invoice
  "Generated your monthly invoice."
  "Markdown file saved to: /Users/jdennes/projects/invoices/_posts/2015-01-31-invoice.markdown"
  "PDF file saved to:      /Users/jdennes/projects/invoices/_posts/_pdfs/2015-01-31-invoice.pdf"
  ```

  You can also create an invoice for a specific date by passing the date as an argument to `script/invoice`:

  ```sh
  $ script/invoice 2018-08-20
  "Generated your monthly invoice."
  "Markdown file saved to: /Users/jdennes/projects/invoices/_posts/2018-08-20-invoice.markdown"
  "PDF file saved to:      /Users/jdennes/projects/invoices/_posts/_pdfs/2018-08-20-invoice.pdf"
  ```

  If you visit [http://localhost:4000](http://localhost:4000) now, you'll see your generated invoice listed there.

  And you'll find the PDF version of your invoice saved in `_posts/_pdfs`:

  ```sh
  $ open /Users/jdennes/projects/invoices/_posts/_pdfs/2015-01-31-invoice.pdf
  ```

That's it!
