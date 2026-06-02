# Local Development Notes

For local Jekyll work, do not use the system Ruby at `/usr/bin/ruby`.

Use the installed Homebrew `ruby@3.3` keg instead:

```bash
export PATH="/opt/homebrew/opt/ruby@3.3/bin:$PATH"
```

Do not use `/opt/homebrew/opt/ruby/bin` on this machine; the unversioned Homebrew `ruby` formula is not installed here.

Then run:

```bash
bundle exec jekyll build
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

Reason:

- System Ruby resolves to Bundler `1.17.2`, which does not satisfy `Gemfile.lock`.
- Homebrew `ruby@3.3` resolves to Ruby `3.3.11` and Bundler `4.0.8`, which matches the project lockfile and builds successfully.
