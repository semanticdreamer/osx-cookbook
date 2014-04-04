# OS X Cookbook

Update the [RubyGems][rubygems] system software:

    sudo gem update --system

Make `--no-ri --no-rdoc` the system wide default for gem install:

    sudo vi /etc/gemrc
    gem: --no-ri --no-rdoc

Install [Homebrew][homebrew] - "*The missing package manager for OS X*":

    ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"

Check your system for potential problems and fix them - if any (exits with a non-zero status if any problems are found). Repeat... until it tells you "*Your system is raring to brew.*" :-)

    brew doctor

Install [Vagrant][vagrant] - "*Create and configure lightweight, reproducible, and portable development environments.*":

    sudo gem install vagrant

Install [Veewee][veewee] - "*tool to easily build vagrant base boxes*":

    sudo gem install veewee
    
## Web Development

Creates a shell function 'server', starting an HTTP server from current working directory, optionally specifing the port:

    vi ~/.bashrc
    function server() {
      local port="${1:-8000}"
      open "http://localhost:${port}/"
      python -m SimpleHTTPServer "$port"
    }
    
    # called like so:
    server 3000

## Editors & (Markdown) Writing Tools

- [Textmate][textmate] — the missing editor for Mac OS X.
- [Sublime Text][sublimetext] -  a sophisticated text editor for code, markup and prose.
- [Marked][marked] - flexible Markdown preview.
- [Marked Bonus Pack][marked-bonus-pack] - scripts, commands and bundles.
 
### Work with files in *Sublime Text* from the command line

> Sublime Text 2 includes a command line tool, subl, to work with files on the
> command line. This can be used to open files and projects in Sublime Text 2, 
> as well working as an EDITOR for unix tools, such as git and subversion.
> [sublimetext.com OS X Command Line](http://www.sublimetext.com/docs/2/osx_command_line.html)

    mkdir ~/bin

    vi ~/.bashrc
    PATH=$PATH:~/bin # Add ~/bin to PATH

    source ~/.bashrc

    ln -s "/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl" ~/bin/subl

### Markdown Preview with *Marked* from *Sublime Text*

Download [Marked Bonus Pack][marked-bonus-pack] and copy the `Marked.sublime-build` file to `~/Library/Application Support/Sublime Text 2/Packages/User/`: pressing **[Command]-[B]** will open the current file in [Marked][marked] for preview.


## Utilities

### ClamXav Anti-Virus

- [ClamXav][clamxav] - the Free Anti-Virus Solution for Mac OS X

> ClamXav Sentry provides the ability to watch folders for changes to their contents.
> As soon as a file or folder is added to one of the watched folders, it is scanned 
> by ClamXav. If the new addition is clean, no further action is required on your part. 
> On the other hand, if it is infected, a warning message is displayed immediately 
> alerting you to the fact and allowing you to decide which course of action to take.


## Miscellaneous

- [Kalenderwoche in Mac-OS X anzeigen](http://www.macwelt.de/artikel/_Tipps/371756/kalenderwoche_in_mac_os_x_anzeigen/1)

[rubygems]: http://rubygems.org/ "RubyGems"
[homebrew]: http://mxcl.github.com/homebrew/ "Homebrew"
[vagrant]: http://vagrantup.com/ "Vagrant"
[veewee]: https://github.com/jedi4ever/veewee "Veewee"
[textmate]: http://macromates.com/ "Textmate"
[sublimetext]: http://www.sublimetext.com/ "Sublime Text"
[marked]: http://markedapp.com/ "Marked"
[marked-bonus-pack]: http://support.markedapp.com/kb/how-to-tips-and-tricks/marked-bonus-pack-scripts-commands-and-bundles "Marked Bonus Pack"
[clamxav]: http://www.clamxav.com/ "ClamXav"
