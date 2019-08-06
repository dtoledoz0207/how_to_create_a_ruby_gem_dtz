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