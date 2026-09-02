# Researcher Website Template

Plain HTML/CSS/JS site, no build step, designed for GitHub Pages.

## Structure

```
index.html          About / homepage
cv.html              CV (PDF embed + HTML fallback)
projects.html        Project list
blog.html            Blog post list (auto-generated from posts-index.json)
post.html            Single post template (loads markdown by ?slug=)
posts/               Your .md blog posts go here
posts-index.json     Metadata for each post (title, date, tags, summary)
cv/cv.pdf            Your CV PDF (replace the placeholder)
assets/style.css     All styling
```

## Editing your info

- **index.html**: replace bracketed placeholders — name, tagline, bio, research interests, email/links.
- **cv.html**: replace placeholder entries (education, experience, publications, skills, awards).
  Drop your real CV PDF at `cv/cv.pdf` (same filename, or update the path in cv.html).
- **projects.html**: duplicate the `.card` block for each project.

## Adding a blog post

1. Write `posts/your-slug.md` in Markdown. Use `$...$` for inline LaTeX, `$$...$$` for block math.
2. Add an entry to `posts-index.json`:
   ```json
   {
     "slug": "your-slug",
     "title": "Post Title",
     "date": "2026-09-01",
     "tags": ["tag1", "tag2"],
     "summary": "One-line summary shown on the blog list."
   }
   ```
3. Commit and push. No build step — GitHub Pages serves it directly.

## Deploying to GitHub Pages

1. Create a new GitHub repo (e.g. `yourusername.github.io` for a root domain, or any name for a project site).
2. Push all these files to the repo's `main` branch.
3. In repo Settings → Pages, set source to `main` branch, root folder.
4. Site goes live at `https://yourusername.github.io/` (or `/reponame/` for a project site).

## Customizing style

All colors/spacing live in `assets/style.css` under `:root` at the top —
change `--accent` to swap the accent color, `--maxw` to change content width, etc.
