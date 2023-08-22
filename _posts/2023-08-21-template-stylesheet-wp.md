---
layout: post
title: "template / stylesheet"
date: 2023-08-21 18:33:23 +0200
categories: wordpress
---

## Thème parent

```php
// Dans functions.php enfant
wp_enqueue_style( 'parent-style', get_template_directory_uri() . '/style.css' );
```

## Thème enfant

```php
// Dans functions.php enfant
wp_enqueue_style('theme-style', get_stylesheet_directory_uri() . '/assets/css/theme.scss', array(), filemtime(get_stylesheet_directory() . '/assets/css/theme.scss'));
```