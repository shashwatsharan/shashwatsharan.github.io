---
layout: default
title: Gallery
---

{% for album in site.data.gallery %}
<section class="album">
  <h2>{{ album.title }}</h2>
  <p class="album-meta">{{ album.place }} · {{ album.date }}</p>
  <div class="justified">
    {% for p in album.photos %}
    {% assign tpath = "/assets/img/gallery/thumbs/" | append: p.file %}
    {% assign thumb = site.static_files | where: "path", tpath | first %}
    <a href="/assets/img/gallery/{{ p.file }}" class="photo" style="--ar: {{ p.ar | default: 1.5 }}"{% unless p.ar %} data-auto-ar{% endunless %} data-caption="{{ p.caption | escape }}" data-album="{{ forloop.parentloop.index }}">
      <img src="{% if thumb %}{{ tpath }}{% else %}/assets/img/gallery/{{ p.file }}{% endif %}" alt="{{ p.caption | escape }}" loading="lazy">
    </a>
    {% endfor %}
  </div>
  {% if album.description %}<p class="album-desc">{{ album.description }}</p>{% endif %}
</section>
{% endfor %}

<div class="lightbox" hidden>
  <button class="lb-close" aria-label="Close">&times;</button>
  <button class="lb-prev" aria-label="Previous photo">&#8249;</button>
  <figure class="lb-figure">
    <img class="lb-img" alt="">
    <figcaption class="lb-caption"></figcaption>
  </figure>
  <button class="lb-next" aria-label="Next photo">&#8250;</button>
</div>

<script>
(function () {
  var links = Array.prototype.slice.call(document.querySelectorAll('.album .photo'));
  // photos added without an ar value get their shape from the image itself
  document.querySelectorAll('.photo[data-auto-ar] img').forEach(function (im) {
    function fit() { if (im.naturalWidth) im.parentNode.style.setProperty('--ar', im.naturalWidth / im.naturalHeight); }
    if (im.complete) fit(); else im.addEventListener('load', fit);
  });
  var lb = document.querySelector('.lightbox'), img = lb.querySelector('.lb-img'),
      cap = lb.querySelector('.lb-caption'), group = [], i = 0, x0 = null;
  function show() {
    var a = group[i];
    img.src = a.href; img.alt = a.dataset.caption; cap.textContent = a.dataset.caption;
    var many = group.length > 1;
    lb.querySelector('.lb-prev').hidden = !many; lb.querySelector('.lb-next').hidden = !many;
  }
  function open(a) {
    group = links.filter(function (l) { return l.dataset.album === a.dataset.album; });
    i = group.indexOf(a); show(); lb.hidden = false; document.body.style.overflow = 'hidden';
  }
  function close() { lb.hidden = true; img.src = ''; document.body.style.overflow = ''; }
  function step(d) { i = (i + d + group.length) % group.length; show(); }
  links.forEach(function (a) {
    a.addEventListener('click', function (e) { e.preventDefault(); open(a); });
  });
  lb.querySelector('.lb-close').onclick = close;
  lb.querySelector('.lb-prev').onclick = function (e) { e.stopPropagation(); step(-1); };
  lb.querySelector('.lb-next').onclick = function (e) { e.stopPropagation(); step(1); };
  lb.addEventListener('click', function (e) { if (e.target === lb || e.target.classList.contains('lb-figure')) close(); });
  document.addEventListener('keydown', function (e) {
    if (lb.hidden) return;
    if (e.key === 'Escape') close();
    if (e.key === 'ArrowLeft') step(-1);
    if (e.key === 'ArrowRight') step(1);
  });
  lb.addEventListener('touchstart', function (e) { x0 = e.touches[0].clientX; }, { passive: true });
  lb.addEventListener('touchend', function (e) {
    if (x0 === null) return;
    var dx = e.changedTouches[0].clientX - x0; x0 = null;
    if (Math.abs(dx) > 50) step(dx < 0 ? 1 : -1);
  });
})();
</script>
