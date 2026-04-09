# Local Development Notes

For local Jekyll work, do not use the system Ruby at `/usr/bin/ruby`.

Use Homebrew Ruby instead:

```bash
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
```

Then run:

```bash
bundle exec jekyll build
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

Reason:

- System Ruby resolves to Bundler `1.17.2`, which does not satisfy `Gemfile.lock`.
- Homebrew Ruby resolves to Ruby `4.0.2` and Bundler `4.0.8`, which matches the project lockfile and builds successfully.
