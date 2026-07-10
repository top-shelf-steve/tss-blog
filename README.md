# rocvoc

My blog, built with Jekyll and hosted free on GitHub Pages at
**https://top-shelf-steve.github.io/tss-blog/**

## How to write a post

1. Create a file in `_posts/` named `YYYY-MM-DD-some-title.md`
2. Start it with front matter:

   ```
   ---
   layout: post
   title: "Some Title"
   ---
   ```

3. Write markdown below the front matter.
4. `git add . && git commit -m "New post" && git push` — live in about a minute.

## Images

Drop the image file in `assets/images/`, then in your post:

```
![What the image shows]({{ "/assets/images/my-image.png" | relative_url }})
```

## Odds and ends

- Site title, tagline, and avatar are set in `_config.yml`
- Replace `assets/images/avatar.svg` with your own picture (update `avatar:` in `_config.yml` if the filename changes)
- Edit `about.md` to fill in the About page
- Moving to a custom domain later: add the domain under repo Settings → Pages, set `url:` in `_config.yml` to the domain, and change `baseurl:` to `""`
