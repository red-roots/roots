+++
title = "Roots"
sort_by = "weight"
+++

# Roots

**Roots** is a simple and responsive Zola theme.

- Simple and intuitive structure
- Clean and elegant design
- Responsive and mobile device compatible
- Customize and extend friendly

# Installation

> **Zola** is a prerequisite. Please refer to the [Zola installation](https://www.getzola.org/documentation/getting-started/installation/) docs.

First download this theme to your `themes` directory:

```bash
$ cd themes
$ git clone https://github.com/huhu/roots.git
```

or add as a submodule
```bash
$ git submodule add https://github.com/huhu/roots  themes/roots
```

and then enable it in your `config.toml`:

```toml
theme = "roots"
```

# Structure

### Frontpage

You can customize your frontpage by overriding the `frontpage` block in the `templates/index.html`.

```html
{% extends "roots/templates/index.html" %}
{% block frontpage %}
    <div>
        Your cool frontpage html...
    </div>
{% endblock frontpage %}
```

### Page

Every markdown file located in `content` directory will become a **Page**. There also will display as
a navigate link on the top-right corner.
You can change the frontmatter's `weight` value to sort the order (ascending order).

```
+++
title = "Changelog"
description = "Changelog"
weight = 2
+++

```

### CSS variables

You can override theme variable by creating a file named `_variables.html` in your `templates` directory.

```html
<style>
    :root {
        /* Primary theme color */
        --primary-color: #FED43F;
        /* Primary theme text color */
        --primary-text-color: #543631;
        --primary-text-color-over: #000;
        /* Primary theme link color */
        --primary-link-color: #F9BB2D;
        /* Secondary color: the background body color */
        --secondary-color: #fcfaf6;
        --secondary-text-color: #303030;
        /* Highlight text color of table of content */
        --toc-highlight-text-color: #d46e13;
        --toc-background-color: white;
        --code-color: #4a4a4a;
        --code-background-color: white;
        --shadow-color: #ddd;
        /* Font used for headers (h1 & h2) */
        --header-font-family: "Fira Sans", sans-serif;
        /* Font used for text */
        --text-font-family: "Fira Sans", sans-serif;
    }
</style>
```

### Favicon
The same way as changing the `frontpage` block in the `templates/index.html`, you can change the **favicon**.

```html
{% extends "roots/templates/index.html" %}
{% block favicon %}
    <link rel="icon" type="image/png" href="/favicon.ico">
{% endblock favicon %}
```

### Fonts
If you changed the `--xy-font-family` variable in `_variables.html`, you have to load the mentioned fonts in the `templates/index.html`.


# Configuration

You can customize some builtin property in `config.toml` file:

```toml
[extra]
theme_logo_path = "roots.svg"
theme_extra_menu = [
    { title = "Github", link = "https://github.com/huhu/roots"}
]
```

# Showcases

Please see the [showcases page](/showcases).

# Acknowledgement

Thanks you to [Huhu](https://github.com/huhu/juice) for the strong inspiration.
