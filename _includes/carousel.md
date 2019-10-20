<div id="main-carousel" class="carousel slide" data-interval="false">
  <!-- Wrapper for slides -->
  <div class="carousel-inner" role="listbox">
    {% for picture in include.data %}
      <img src="{{ picture.url }}" alt="" style="padding-top:1rem" class="img-responsive">
    {% endfor %}
  </div>
</div>
<br>
