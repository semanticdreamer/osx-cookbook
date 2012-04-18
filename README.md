#OS X Cookbook

Update the [RubyGems][rubygems] system software:

    sudo gem update --system

Install [Homebrew][homebrew] - "*The missing package manager for OS X*":

    /usr/bin/ruby -e "$(/usr/bin/curl -fksSL https://raw.github.com/mxcl/homebrew/master/Library/Contributions/install_homebrew.rb)"

Check your system for potential problems and fix them - if any (exits with a non-zero status if any problems are found). Repeat... until it tells you "*Your system is raring to brew.*" :-)

    brew doctor

Install [Vagrant][vagrant] - "*Create and configure lightweight, reproducible, and portable development environments.*":

    sudo gem install vagrant

Install [Veewee][veewee] - "*tool to easily build vagrant base boxes*":

    sudo gem install veewee

##Miscellaneous

* [Kalenderwoche in Mac-OS X anzeigen](http://www.macwelt.de/artikel/_Tipps/371756/kalenderwoche_in_mac_os_x_anzeigen/1)

[rubygems]: http://rubygems.org/ "RubyGems"
[homebrew]: http://mxcl.github.com/homebrew/ "Homebrew"
[vagrant]: http://vagrantup.com/ "Vagrant"
[veewee]: https://github.com/jedi4ever/veewee "Veewee"