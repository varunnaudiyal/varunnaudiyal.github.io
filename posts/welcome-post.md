# Welcome

This is a sample post to show how the blog system works. Write posts in plain **Markdown**,
and this template will render them automatically — no build step required.

## Markdown features

- Lists, **bold**, *italics*, `inline code`
- Code blocks:

```python
def hello():
    print("Hello, research world!")
```

- Links and images work as usual: [example link](https://example.com)

## LaTeX support

Inline math works like this: the energy-mass relation is $E = mc^2$.

Block-level equations work too:

$$
\nabla \cdot \mathbf{E} = \frac{\rho}{\varepsilon_0}
$$

You can write more complex expressions, e.g. a Gaussian integral:

$$
\int_{-\infty}^{\infty} e^{-x^2} \, dx = \sqrt{\pi}
$$

## How to add a new post

1. Write a new `.md` file in the `posts/` folder, e.g. `posts/2026-09-my-topic.md`.
2. Add an entry to `posts-index.json` with a matching `slug` (the filename without `.md`),
   a `title`, `date`, optional `tags`, and a short `summary`.
3. Commit and push — GitHub Pages updates automatically, no build step needed.

That's it!
