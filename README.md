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

    Do you want to generate tests with your gem? *rspec*
    Do you want to license your code permissively under the MIT license? *y*
    Do you want to include a code of conduct in gems you generate? *y*

And that’s it.
You’ll see a folder with the name of your gem and inside some files that bundle creates for you.