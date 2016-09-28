---
layout: default
---

<div id="container" class="container-fluid">
  <div class="row">

    {% include _page_header.html %}

    <section id="main_content">
      <div id="canfar-carousel" class="carousel slide"
           data-ride="carousel" data-keyboard="true">
        <!-- Indicators -->
        <ol class="carousel-indicators">
          <li data-target="#canfar-carousel" data-slide-to="0"
              class="active"></li>
          <li data-target="#canfar-carousel" data-slide-to="1"></li>
          <li data-target="#canfar-carousel" data-slide-to="2"></li>
        </ol>

        <!-- Wrapper for slides -->
        <div class="carousel-inner" role="listbox">
          {% for showcase in site.data.showcases %}
          <div class="item {% if forloop.index == 1 %}active{% endif %}" style="background-image: url('{{ showcase.img | prepend: site.baseurl }}');">
            <div class="carousel-caption">
              <h3>{{ showcase.title }}</h3>
              <p>{{ showcase.tagline }}</p>
            </div>
          </div>
          {% endfor %}
        </div>

        <!-- Controls -->
        <a class="left carousel-control" href="#canfar-carousel"
           role="button" data-slide="prev">
          <span class="glyphicon glyphicon-chevron-left"
                aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a class="right carousel-control" href="#canfar-carousel"
           role="button" data-slide="next">
          <span class="glyphicon glyphicon-chevron-right"
                aria-hidden="true"></span>
          <span class="sr-only">Next</span>
        </a>
      </div>

    </section>

    <section id="information_content">
      <div class="row">
        <div class="col-md-6 col-md-offset-6">
          <div class="col-md-4">
            <div class="col-md-10 col-md-offset-1">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h3 class="panel-title">Events</h3>
                </div>
                <div class="panel-body">
                  Event content
                </div>
              </div>
            </div>
          </div>
          <div class="col-md-4">
            <div class="col-md-10 col-md-offset-1">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h3 class="panel-title">Collaborations</h3>
                </div>
                <div class="panel-body">
                  Collaborations content
                </div>
              </div>
            </div>
          </div>
          <div class="col-md-4">
            <div class="col-md-10 col-md-offset-1">
              <div class="panel panel-primary">
                <div class="panel-heading">
                  <h3 class="panel-title">Future</h3>
                </div>
                <div class="panel-body">
                  Future content
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    {% include _page_footer.html %}

  </div>
</div>