# Schizelle Portfolio

## Distinction between Gallery types

- _gallery
  - See on the main page
  - Can be expanded via **View All**
- _headshots
  - Part of Gallery Drop down
- _shows
  - Part of Gallery Drop down
- _creative_projects
  - Part of Gallery Drop down

## To add a new subheading under Gallery

### References
- See `components/gallery-subpage`

### Instructions

- Navigate to `_data/navigation.yml` and add a new submenu with your required URL

```yml
- title: "Gallery"
    submenu:
    - title: "Headshots"
        url: "/headshots/"
```

- Create a `{URL}.html` in `collections/_pages`
  - For example `headshots.html`
  - Add this front matter to your `{URL}.html`
  - Make sure you specify the "from" keyword, this will be similar to what you write in `_config.yml`

```html
---
title: Headshots
content_blocks:
  - _bookshop_name: page-heading
    title: Headshots
    description: Professional headshots for film and tv
  - _bookshop_name: gallery-subpage
    from: headshots
---
```

- Create an `_{URL}` folder in the `collections` folder
  - See the `_headshots` folder created
  - Add your image-card files as markdown

- Go to `_config.yml`
  - Make sure to add your `_URL` folder created under the `collections` section as `URL`
  - NOTE: output: true is required for page to be rendered
```yml
collections
  # ...
  headshots:
    output: true
```
