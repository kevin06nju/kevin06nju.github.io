# Kevin's AI Learning Hub

A personal blog for sharing AI learning experiences, built with **Jekyll** and deployed on **GitHub Pages**.

**Live Site:** [https://kevin06nju.github.io](https://kevin06nju.github.io)

## Features

- **Topic-based organization** — Articles grouped into topic folders (`_posts/ai-basics/`, `_posts/llm/`, `_posts/tools/`)
- **Tag system** — Cross-cutting tags for flexible browsing
- **Category filtering** — JavaScript-powered tab filtering on homepage
- **Two-column card layout** — Gradient cover images per topic with hover animations
- **Sidebar** — Author card, recent posts, tag cloud
- **Responsive design** — Desktop sidebar collapses to grid on mobile
- **Dark code blocks** — Catppuccin-style syntax highlighting

## Tech Stack

- **Jekyll** — Static site generator
- **GitHub Pages** — Zero-config hosting and deployment
- **Kramdown + Rouge** — Markdown rendering and syntax highlighting
- **Vanilla CSS + JS** — No framework dependencies

## Project Structure

```
_config.yml              # Site config, topic definitions, author info
_layouts/
  default.html           # Base layout
  post.html              # Article page with gradient cover
  topic.html             # Topic detail page
_includes/
  header.html            # Sticky navigation
  footer.html            # Site footer
_posts/
  ai-basics/             # Topic: AI fundamentals
  llm/                   # Topic: Large Language Models
  tools/                 # Topic: Tools & Practice
topics/                  # Individual topic listing pages
assets/css/main.css      # All styles
index.html               # Homepage with cards + sidebar
topics.html              # All topics overview
tags.html                # Tag cloud + grouped posts
about.md                 # About page
```

## Writing a New Post

1. Create a file in the appropriate topic folder:
   ```
   _posts/<topic-slug>/YYYY-MM-DD-your-title.md
   ```

2. Add front matter:
   ```yaml
   ---
   title: "Your Post Title"
   date: 2026-04-10
   topic: "AI 基础"        # Must match a topic name in _config.yml
   tags: [tag1, tag2]
   ---
   ```

3. Write content in Markdown, then push to GitHub.

## Adding a New Topic

1. Add topic definition in `_config.yml` under `topics`:
   ```yaml
   new-topic:
     name: "Topic Name"
     description: "Short description"
     icon: "🔥"
     gradient: "linear-gradient(135deg, #color1 0%, #color2 100%)"
   ```

2. Create the topic folder: `_posts/new-topic/`

3. Create a topic page at `topics/new-topic.md`:
   ```yaml
   ---
   layout: topic
   title: "Topic Name"
   permalink: /topics/new-topic/
   topic_name: "Topic Name"
   description: "Short description"
   icon: "🔥"
   ---
   ```

## License

Content and code in this repository are for personal use. Feel free to reference the structure for your own blog.
