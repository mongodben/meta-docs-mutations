---
title: Image Lightboxes
updated: '2024-08-13T13:16:43.865Z'
url: https://mongodb.com/docs/meta/reference/lightbox/
---

# Image Lightboxes

Sometimes an image is too large to be legible in the normal page flow. While it is generally better to redesign the image, you may wish instead to allow the user to temporarily expand the image to its full size.

This is called a "lightbox", and you may provide the `lightbox` option to the Sphinx figure directive if the `mongodb` extension is activated in your `conf.py`.

```rst
.. figure:: /images/compass-array-query-op.png
   :alt: lightbox example
   :figwidth: 200px
   :lightbox:
```