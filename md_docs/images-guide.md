---
title: Adding Images
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/images-guide/
---

# Adding Images

This guide is advisory, and its suggestions do not necessarily apply to every situation.

## Without Giza (Recommended)

### Adding an SVG

Whenever possible, you should publish diagrams in SVG form. This provides a crisp image at any screen resolution with a small file size.

First install mut, Inkscape, and svgo.

Place your SVG in `source/images/`. If you named your SVG `foo.svg`, then run the following from within that directory:

```sh
mut-images foo.svg
```

This will generate `foo.bakedsvg.svg`. This *baked* SVG file contains no text: to prevent users from needing to download any fonts, `mut-images` transforms all text elements into paths. It then uses `svgo` to minify the resulting SVG file.

Create a `source/images/foo.rst` file with contents such as the following:

```rst
.. figure:: /images/foo.bakedsvg.svg
   :alt: An example image.
   :figwidth: 500px
```

Check in and commit all three files.

### Adding a PNG

Not all images start their life as an SVG. The process is less refined for adding these files, but in general keep the resolution under two times the display width.

For example, if you want to display an image as 500px wide, the image itself should not be wider than 1000px.

The MongoDB Documentation Project does not currently have a best practice for handling very large (>1080p) files or photographic content.

It may make sense to use mozjpeg if you need lossy compression; imagemagick to resize images; and a Ninja file to put the pieces together.

The default `libpng` encoder does not create optimal PNG files, so install zopflipng. To compress a PNG, use the following template:

```sh
zopflipng -m <input.png> <output.png>
```

This may take several minutes, as the `-m` option requests a brute-force search for optimal compression parameters.

Place the output PNG in `source/images/`, and create a `source/images/foo.rst` file with contents such as the following:

```rst
.. figure:: /images/foo.png
   :alt: An example image.
   :figwidth: 500px
```

## With Giza

Some MongoDB documentation projects use Giza's image generation. This can be effective when you need images rendered at different sizes for different output formats.

It has the following disadvantages:

- Giza only accepts SVGs: you must embed raster files inside of an SVG,

- Giza invokes inkscape for each input file, and

- Reliability problems. There was one instance where giza generated some images sans any text.

Giza looks for the path listed in `system.files.data.files` within `config/build_conf.yaml` for a manifest containing image metadata.

The image metadata is a YAML list of documents such as the following:

```yaml
name: opsmanager-large
alt: "A highly available deployment uses horizontal scaling of the application database and backup    blockstore database, as well as multiple backup daemons."
output:
  - type: print
    tag: 'print'
    dpi: 300
    width: 2100
  - type: web
    dpi: 72
    width: 700
```

From this example, Giza will generate the following files in the build directory:

- `/source/images/opsmanager-large.rst`

- `/source/images/opsmanager-large.png`

- `/source/images/opsmanager-large-print.png`