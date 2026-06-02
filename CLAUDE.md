# Local Development Notes

For local Jekyll work, use the installed Homebrew `ruby@3.3` keg instead of the system Ruby:

```bash
export PATH="/opt/homebrew/opt/ruby@3.3/bin:$PATH"
bundle exec jekyll build
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

Do not use `/opt/homebrew/opt/ruby/bin` on this machine; the unversioned Homebrew `ruby` formula is not installed here.

This project does not build correctly with `/usr/bin/ruby` because that environment uses Bundler `1.17.2`, while `Gemfile.lock` requires Bundler `4.0.8`. Homebrew `ruby@3.3` currently provides Ruby `3.3.11` and Bundler `4.0.8`.
