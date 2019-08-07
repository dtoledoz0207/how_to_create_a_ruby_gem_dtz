# How to create a Ruby Gem

This document describes how to create a Ruby Gem with Bundler, an easy way to start your first gem because Bundler generates some specifications files for you.

## Getting Started
Firstly open your terminal and run this command:

    $ gem install bundler

Then run the next command to check the bundle version:

    $ bundle -v
    Bundler version 1.17.2

If you can see the bundle version that mean that bundle has been installed successfully

## Creating a gem
Run the following command and Bundle will create some specifications files for you

    $ bundle gem name_of_my_gem

If is the first time that you make a gem, in the terminal you will see some configuration questions, for this example we are going to use rspec for the test and you only have to type the following answers:

    Do you want to generate tests with your gem? rspec
    Do you want to license your code permissively under the MIT license? y
    Do you want to include a code of conduct in gems you generate? y

And that’s it.
You’ll see a folder with the name of your gem and inside some files that bundle creates for you.

### Setting up
Go to your gem folder
    
    $ cd name_of_your_gem

We are going to start making some changes in the `gemspec` file, this file appears something like that: `name_of_my_gem.gemspec`

We need to change all TODO text with our gem information, the principal values are:

```ruby
spec.name = "name_of_your_gem"
spec.authors = ["Your name"]
spec.email = ["youremailaddress@email.com"]
spec.summary = %q{a summary about your gem}
spec.description = %q{a description about your gem}
spec.homepage = "you can put your GitHub repository url here"
```

And finally we are going to comment the metadata condition or delete it.

## RSPEC
After that we are ready to do our first rspec test.

The tests file is in the `spec` folder. We need to write our rspec tests in the spec file that looks like this: `name_of_my_gem_spec.rb`

In the begin this file has only two test, the first is to check if the version is not nil and the second it’s only an example that it’s going to show us an error.
Now we are going to run our `spec` file. First we need to be in the root of our gem, then we need to type the next command in the terminal:

    $ bundle exec rspec spec/name_of_my_gem_spec.rb

That will show us if the tests are correct or failed. For this example, our gem just passed a test, the second one was wrong because expect a false value and the response was true.

Now we know where we have to write our rspec tests and how to run our spec file. The next step is to know where we have to write our principal code for the gem.