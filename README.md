# Quang Truong's Website

## Installation
The site is plain Jekyll (no plugins), so you only need Ruby and the `jekyll` gem.

**Windows**
```
winget install RubyInstallerTeam.RubyWithDevKit.3.3
# open a new terminal, then:
ridk install   # choose option 3 (MSYS2 + MINGW toolchain)
gem install jekyll
gem install wdm   # optional: native file watching, silences the "add wdm to your Gemfile" warning
```

**macOS** (the system Ruby is too old; use Homebrew's)
```
brew install ruby
echo 'export PATH="$(brew --prefix ruby)/bin:$PATH"' >> ~/.zshrc && source ~/.zshrc
echo "export PATH=\"$(gem env gemdir)/bin:\$PATH\"" >> ~/.zshrc && source ~/.zshrc
gem install jekyll
```

**Linux** (Debian/Ubuntu)
```
sudo apt install ruby-full build-essential
echo 'export GEM_HOME="$HOME/gems"; export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc && source ~/.bashrc
gem install jekyll
```

If `jekyll serve` fails with `cannot load such file -- webrick`, run `gem install webrick`.

## Updates guide
Change one of the files in `_data`, unless you are changing the look of the website.

Test changes with:
```
jekyll serve
```
Then open http://localhost:4000. Press Ctrl+C to stop the server. On Windows this prints `Terminate batch job (Y/N)?`; answer `Y`.
