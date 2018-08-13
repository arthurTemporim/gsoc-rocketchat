# Documentation Contribution Guidelines

First of all, thank you for your interest in contributing to Rocket.Chat Website.
If this is the first Open Source project you will contribute to,
we strongly suggest reading GitHub's excellent guide
["Contributing to Open Source"](https://guides.github.com/activities/contributing-to-open-source/).

## Running the website locally

- install ruby (version 2.5 or higher recommended, if using any version prior to 2.5 you will need to install bundler with `gem install bundler`).
- This step is for only macOS users:
  - You will need to have either `xcode` or the `xcode command line tools` installed. To install the command tools use `xcode-select --install`. Don't forget to accept the `sudo xcodebuild -license` command.
  - Depending on your setup you might need to install [nokogiri](http://www.nokogiri.org/tutorials/installing_nokogiri.html) and its dependencies manually.
- Fork the appropriate repository to your account.
- Clone your fork.
- Run `bundle install` inside of the cloned folder.
- Start the server with `bundle exec "jekyll serve --incremental --safe"`
