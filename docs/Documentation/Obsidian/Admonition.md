---
tags: [documentation, Markdown]
author: [Yann Houry]
date: 23-02-2022
---

## Source
- https://github.com/valentine195/obsidian-admonition
- https://squidfunk.github.io/mkdocs-material/reference/admonitions/

````
```ad-note
title:                  # Admonition title.
collapse:               # Create a collapsible admonition.
icon:                   # Override the icon.
color:                  # Override the color.
```
````

Use [Fontawesome](https://fontawesome.com/icons) to override the icon

### Admonition types
- note
- abstract
- info
- tip
- success
- question
- warning
- failure
- danger
- bug
- example
- quote

## Examples
```ad-note
title: Notes
collapse: open
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla.
```

```ad-info
title: Info
collapse: open
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla.
```

```ad-warning
title: Attention
collapse: open
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla.
```

```ad-example
title: Exemple
collapse: open
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla.
```

```ad-quote
title: Citation
collapse: open
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla.
```

```ad-info
title: À lire
collapse: open
icon: book
color: 200, 200, 200
```