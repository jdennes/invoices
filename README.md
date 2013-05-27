This is a very quick Jekyll-based thing which allows me to do monthly invoicing by running `rake invoice`.

To use this yourself, fork and clone, then follow these instructions:

1. Install dependencies.

  ```sh
  $ bundle install
  ```

2. Create your own `_config.yml` file.

  ```sh
  $ cp _config.yml.example _config.yml
  ```

  Edit your `_config.yml` file. Everything should be pretty obvious.

3. Run the app.

  ```sh
  $ bundle exec rake run
  ```

  That starts the app at [http://localhost:4000](http://localhost:4000). You probably won't see any invoices there yet though.

4. Create an invoice for the current month.

  ```sh
  $ bundle exec rake invoice
  "Generated your monthly invoice. Saved to /Users/you/invoices/_posts/2013-05-31-invoice.markdown"
  ```

  If you visit [http://localhost:4000](http://localhost:4000) now, you should see your generated invoice listed there.
  
  Click it to view it, then PDF it and email it!

That's it!
