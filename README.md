# fahdi.github.io
My Github pages https://fahdi.github.io/

## Local Development

This is a Jekyll-based GitHub Pages website. To run it locally:

### Prerequisites
- Ruby (3.4+ recommended)
- Jekyll
- Bundler

### Installation

1. Install Ruby via Homebrew (macOS):
   ```bash
   brew install ruby
   ```

2. Add Homebrew Ruby to your PATH:
   ```bash
   export PATH="/opt/homebrew/opt/ruby/bin:/opt/homebrew/lib/ruby/gems/3.4.0/bin:$PATH"
   ```

3. Install Jekyll and Bundler:
   ```bash
   gem install jekyll bundler
   ```

### Running the Site

To start the development server:

```bash
# Set the Ruby path
export PATH="/opt/homebrew/opt/ruby/bin:/opt/homebrew/lib/ruby/gems/3.4.0/bin:$PATH"

# Start Jekyll server with livereload
jekyll serve --host 127.0.0.1 --port 4001 --livereload
```

The site will be available at http://localhost:4001 with automatic browser refresh when files change.

### Features

- **GitHub Integration**: Dynamically displays GitHub repositories
- **Blog Integration**: Links to external blog posts
- **Social Media Links**: Twitter, Facebook, Quora, LeetCode, etc.
- **Responsive Design**: Built with Jekyll's Minima theme
