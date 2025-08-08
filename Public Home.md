---
title: Hello, World!
tags:
  - Public
creationDate: 2025-08-08
modifiedDate: 2025-08-08
published: 2025-08-08
access: Public
---

Hey, I'm Paul Kenny. This is my <a href="./pages/Digital%20Garden.html">digital garden</a>. My smelly, messy digital garden.

<p>
Here's the Everything Graph. Pages are green dots and tags are blue dots. If you drag one of the dots around it helps "resolve" the graph:

<div id="graph-container"></div>
<script>
    const jsonFilePath = "index.json";
    const script = document.createElement('script');
    script.src = "js/d3-pkspkms-graph-no-tag-hierarchy.js";
    script.onload = () => {
        if (typeof initD3Graph === 'function') {
            initD3Graph(jsonFilePath, 'graph-container');
        }
    };
    document.body.appendChild(script);
</script>

<hr>

Here's some pages that may be of interest:

<ul>
    <li><a href="./pages/Blogs%20I%20Like.html">Blogs I Like</a></li>
    <li><a href="./pages/Programs%20I%20Like.html">Programs I Like</a></li>
    <li><a href="./cooler-index.html">Experimental 3D graph</a></li>
</ul>

<h2>All Pages</h2>

$partial("templates/pages.html")$
