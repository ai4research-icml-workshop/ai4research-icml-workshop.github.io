# Local Development Notes

For local Jekyll work, use Homebrew Ruby instead of the system Ruby:

```bash
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
bundle exec jekyll build
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

This project does not build correctly with `/usr/bin/ruby` because that environment uses Bundler `1.17.2`, while `Gemfile.lock` requires Bundler `4.0.8`.
