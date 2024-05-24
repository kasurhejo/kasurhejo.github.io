---
layout: default1
disqus: false
archive: false
post_class: post-template
---

<!-- Begin Article
================================================== -->
<div class="container">
    <div class="row">

        <!-- Post Share -->
        <div class="col-md-2 pl-0">
            {% include share.html %}
        </div>

        <!-- Post -->
        {% assign author = site.authors[page.author] %}

        <div class="col-md-9 flex-first flex-md-unordered">
            <div class="mainheading">

           
                   
             <a id="show_id" onclick="document.getElementById('spoiler_id').style.display=''; document.getElementById('show_id').style.display='none';"></a><span id="spoiler_id" style="display: none;"><a class="link" onclick="document.getElementById('spoiler_id').style.display='none'; document.getElementById('show_id').style.display='';"></a>
<div style="background-color: rgba(0, 0, 0, 0); margin: 1px;">
<div class="smallfont"><i><span style="font-size: 16px; font-weight: bold; margin-right: 3px;"></span></i><input onclick="if (this.parentNode.parentNode.getElementsByTagName('div')[1].getElementsByTagName('div')[0].style.display != '') { this.parentNode.parentNode.getElementsByTagName('div')[1].getElementsByTagName('div')[0].style.display = ''; this.innerText = ''; this.value = ''; } else { this.parentNode.parentNode.getElementsByTagName('div')[1].getElementsByTagName('div')[0].style.display = 'none'; this.innerText = ''; this.value = ''; }" style="background-color: #00000000; font-size: 16px; width: auto;" type="button" value="" />
</div>
<div class="alt2" style="background-color: rgba(255, 255, 255, 0); margin: 0px; padding: 0px;">
<div style="display: none;" loading="lazy">














                <!-- Post Title -->
                <h1 class="posttitle">{{ page.title }}</h1>
</div></div></div></span>   

            </div>

     
     <a id="show_id" onclick="document.getElementById('spoiler_id').style.display=''; document.getElementById('show_id').style.display='none';"></a><span id="spoiler_id" style="display: none;"><a class="link" onclick="document.getElementById('spoiler_id').style.display='none'; document.getElementById('show_id').style.display='';"></a>
<div style="background-color: rgba(0, 0, 0, 0); margin: 1px;">
<div class="smallfont"><i><span style="font-size: 16px; font-weight: bold; margin-right: 3px;"></span></i><input onclick="if (this.parentNode.parentNode.getElementsByTagName('div')[1].getElementsByTagName('div')[0].style.display != '') { this.parentNode.parentNode.getElementsByTagName('div')[1].getElementsByTagName('div')[0].style.display = ''; this.innerText = ''; this.value = ''; } else { this.parentNode.parentNode.getElementsByTagName('div')[1].getElementsByTagName('div')[0].style.display = 'none'; this.innerText = ''; this.value = ''; }" style="background-color: #00000000; font-size: 16px; width: auto;" type="button" value="" />
</div>
<div class="alt2" style="background-color: rgba(255, 255, 255, 0); margin: 0px; padding: 0px;">
<div style="display: none;" loading="lazy">












  
            
            
            <!-- Post Featured Image -->
            {% if page.image %}

            {% if site.lazyimages == "enabled" %}
            <img class="featured-image img-fluid lazyimg" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAMAAAACCAQAAAA3fa6RAAAADklEQVR42mNkAANGCAUAACMAA2w/AMgAAAAASUVORK5CYII=" data-src="{% if page.image contains "://" %}{{ page.image }}{% else %}{{ site.baseurl }}/{{ page.image }}{% endif %}" alt="{{ page.title }}">
            {% else %}
            <img class="featured-image img-fluid" src="{% if page.image contains "://" %}{{ page.image }}{% else %}{{ site.baseurl }}/{{ page.image }}{% endif %}" alt="{{ page.title }}">
            {% endif %}

            {% endif %}
            <!-- End Featured Image -->
</div></div></div></span>
            
            <!-- Post Content -->
            <div class="article-post">
                <!-- Toc if any -->
                {% if page.toc %}
                    {% if page.beforetoc %}
                        <p><em>{{page.beforetoc}}</em></p>
                    {% endif %}
                    <div class="toc mt-4 mb-4 lead">
                        <h3 class="font-weight-bold">Summary</h3>
                        {% include toc.html html=content %}
                    </div>
                {% endif %}
                <!-- End Toc -->
               
         
    
        






{{content}}


                
                
            </div>


            <!-- Rating -->
            {% if page.rating %}
            <div class="rating mb-4 d-flex align-items-center">
                <strong class="mr-1">Rating:</strong> {% include star_rating.html %}
            </div>
            {% endif %}

            <!-- Post Date -->
            <p>
            <small>
                <span class="post-date"><time class="post-date" datetime="{{ page.date | date:"%Y-%m-%d" }}">{{ page.date | date_to_string }}</time></span>           
                {% if page.last_modified_at %}
                (Updated: <time datetime="{{ page.last_modified_at | date_to_xmlschema }}" itemprop="dateModified">{{ page.last_modified_at | date: "%b %-d, %Y" }}</time>)
                {% endif %}
                </small>
            </p>

      

      
        </div>
        <!-- End Post -->

    </div>
</div>
<!-- End Article
================================================== -->
 
