+++
title = "Search"
menu = "main"
weight = 30
+++

# Search

<link href="../pagefind/pagefind-ui.css" rel="stylesheet">
<script src="../pagefind/pagefind-ui.js"></script>
<div id="search"></div>
<script>
  window.addEventListener("DOMContentLoaded", () => {
    new PagefindUI({ element: "#search", showSubResults: true });
  });
</script>
<noscript>Search needs JavaScript. You can browse every post on the <a href="../blog/">blog</a>.</noscript>
