Renewable Funding: Code Challenge
=================================

This is the application developed to meet the challenge requirements presented by Renewable Funding. I appreciate the opportunity to display my solution. It was a fun application to create.

## Setup

* Change the version of ruby in in_house_code_challenge/.ruby_version to match your installed version. Mine was MRI 2.2.3
* Make sure you are using rbenv.
* Run: bundle install
* Run: bundle exec rake db:migrate or bin/rake db:migrate
* Run: bundle exec rake db:seed to create the default user, or bin/rake db:seed.
* I was running on Ubuntu 14.04 on Linux, using the sqlite3 database, and RSpec.

## Running the application
* bin/rails s
* alternate: bin/rails server -b 0.0.0.0 (If your browser is on windows and your app is in VirtualBox.)

## Interaction with the application as a user
* Enter http://localhost:3000 in your browser. You will be redirected to a login page.
* Login. The only user in the data base after seeding is 'tableman@csv.org' with password 'upload4you'
* Click the file upload button, find your file and click upload. (../example_files/example_data.csv)
* The results page will show the total purchases for the upload and total purchases in the database, as well as the orders in the database.
* Multiple uploads will add the same data multiple times. The total will continue to grow.

## Running tests
This application is setup with binstubs and spring, to save time and typing.
* bundle exec rake spec
* alternate: bin/rake

## Philosophy
This application was developed using TDD, implementing just enough code to make the tests pass, and just enough tests to meet requirements. Of course, much could be done to improve how robust, secure, beautiful and intuitive this application is. But these factors should be be driven by product management based on business cases. Without a case, additional time would be spent before establishing the corresponding value of the improvements.

Test cases are not exhaustive, and all exist in the spec directory. I didn't write tests for associations and validations, since those are just rails. I did test the requirements.
