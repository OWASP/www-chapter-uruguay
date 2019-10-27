<!-- Based on https://www.w3schools.com/howto/tryit.asp?filename=tryhow_js_slideshow_multiple -->
<div class="slideshow-container">
  {% for picture in include.data %}
    <div class="{{ include.name }}">
      <img src="{{ picture.url }}" class="img-responsive">
    </div>
  {% endfor %}
  
  <a class="prev" onclick="plusSlides(-1, {{ include.id }})">&#10094;</a>
  <a class="next" onclick="plusSlides(1, {{ include.id }})">&#10095;</a>
</div>
<br/>
