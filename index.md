---
title: Aeon Community Collection
permalink: index.html
---
<html>
<head>
<title>Aeon Community Collection</title>
<link rel="stylesheet" href="https://unpkg.com/flexboxgrid2@7.2.1/flexboxgrid2.css">
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css" integrity="sha384-B4dIYHKNBt8Bc12p+WXckhzcICo0wtJAoU8YZTY5qE0Id1GSseTk6S+L3BlXeVIU" crossorigin="anonymous">
<style>
:root {
  --color1: #5fbcd3;
  --color2: #2c89a0;
  --color3: #164450;
  --color4: #444444;
  --color5: #ffffff;
  --color6: #f2f2f2;
}
body {
  margin: 0;
  background-color: var(--color6);
  color: var(--color4);
  font-family: 'Myriad Pro', Calibri, Helvetica, Arial, sans-serif;
}
a {
  color: var(--color2);
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
h2 > a {
  color: var(--color4);
  text-decoration: none;
}
h2 > a:hover {
  color: var(--color2);
  text-decoration: none;
}
h1, h2, h3 {
  font-family: 'Lucida Grande', 'Calibri', Helvetica, Arial, sans-serif;
}
h2 {
  border-bottom-color: var(--color4);
  border-bottom-style: solid;
  border-bottom-width: 2px;
  cursor: pointer;
}
h3 {
  padding-left: 10px;
}
ul {
  padding-left: 30px;
}
input[type=checkbox] {
  display: none;
}
.panel {
  height: auto;
  opacity: 1;
  transition: 1s;
  overflow: hidden;
}
input[type=checkbox]:checked+label+.panel {
  z-index: -1;
  height: 0px;
  opacity: 0;
  transition: 1s;
}
.text-left {
  text-align: left;
}
footer {
  width: 100%;
  height: 50px;
  background-color: var(--color4);
  margin: 60px 0px 0px 0px;
}
</style>
<!--
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.4/jquery.min.js" type="text/javascript"></script>
-->
</head>
<body>

<header>

</header>

<main>
  <div class="container">
    <div class="row center-xs">
      <div class="col-xs-12 col-lg-10 col-xl-8 text-left">
        <h1>Welcome</h1>
        <p>This site will contain some How-To's and Wherefores of the Aeon digital currency.</p>

        <input type="checkbox" name="accordion" id="get-started" checked>
        <label for="get-started"><h2>Get Started</h2></label>
        <div class="panel">
          {% capture get-started %}{% include get-started.md %}{% endcapture %}
          {{ get-started | markdownify }}
        </div>

        <input type="checkbox" name="accordion" id="using" checked>
        <label for="using"><h2>Using</h2></label>
        <div class="panel">
          {% capture using %}{% include using.md %}{% endcapture %}
          {{ using | markdownify }}
        </div>

        <input type="checkbox" name="accordion" id="mining" checked>
        <label for="mining"><h2>Mining</h2></label>
        <div class="panel">
          {% capture mining %}{% include mining.md %}{% endcapture %}
          {{ mining | markdownify }}
        </div>

        <input type="checkbox" name="accordion" id="accepting" checked>
        <label for="accepting"><h2>Accepting</h2></label>
        <div class="panel">
          {% capture accepting %}{% include accepting.md %}{% endcapture %}
          {{ accepting | markdownify }}
        </div>

        <input type="checkbox" name="accordion" id="contributing" checked>
        <label for="contributing"><h2>Contributing</h2></label>
        <div class="panel">
          {% capture contributing %}{% include contributing.md %}{% endcapture %}
          {{ contributing | markdownify }}
        </div>

        <input type="checkbox" name="accordion" id="developer-guides" checked>
        <label for="developer-guides"><h2>Developer Guides</h2></label>
        <div class="panel">
          {% capture developer-guides %}{% include developer-guides.md %}{% endcapture %}
          {{ developer-guides | markdownify }}
        </div>

        <input type="checkbox" name="accordion" id="recent-news" checked>
        <label for="recent-news"><h2>Recent News</h2></label>
        <div class="panel">
          {% capture recent-news %}{% include recent-news.md %}{% endcapture %}
          {{ recent-news | markdownify }}
        </div>

        <input type="checkbox" name="accordion" id="community" checked>
        <label for="community"><h2>Community</h2></label>
        <div class="panel">
          {% capture community %}{% include community.md %}{% endcapture %}
          {{ community | markdownify }}
        </div>
      </div>
    </div>
  </div>
</main>

<footer>
</footer>

</body>
</html>
