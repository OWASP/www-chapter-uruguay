---
title: OWASP
layout:  null
tab: true
order: 1
tags: Uruguay
---

# OWASP
* Promueve el desarrollo de software seguro
* Orientada a la prestación de servicios orientados a la Web
* Se centra principalmente en el "back-end" mas que en cuestiones de diseño web
* Un foro abierto para el debate
* Un recurso gratuito para cualquier equipo de desarrollo de software

## ¿Qué ofrece OWASP?
<div id='all-projects' class='projects-list'>
    <h3>Listado de proyectos según <a id="projects-level" class='active'>Nivel</a> ó <a id="projects-type" class='inactive'>Tipo</a></h3>
    <div id="project-list-level" class='project-list'>
        {% assign fs_projects = site.data.owaspprojects | where:'level', '4' %}
        {% assign l_projects = site.data.owaspprojects | where:'level', '3' %}
        {% assign i_projects = site.data.owaspprojects | where:'level', '2' %}
        <h3>Proyectos Flagship <img src='https://owasp.org/assets/images/common/owasp_level_flagship.svg' width='45px' alt='Flagship'></h3>
        <ul>
        {% for project in fs_projects %}
        <li><a href="{{ project.url }}">{{ project.title }}</a></li>
        {% endfor %}
        </ul>
        <h3>Proyectos Laboratorio <img src='https://owasp.org/assets/images/common/owasp_level_labs.svg' width='45px' alt='Lab'></h3>
        <ul>
        {% for project in l_projects %}
        <li><a href="{{ project.url }}">{{ project.title }}</a></li>
        {% endfor %}
        </ul>
        <h3>Proyectos en Incubación <img src='https://owasp.org/assets/images/common/owasp_level_incubator.svg' width='45px' alt='Incubator'></h3>
        <ul>
        {% for project in i_projects %}
        <li><a href="{{ project.url }}">{{ project.title }}</a></li>
        {% endfor %}
        </ul>
    </div>
    <div id="project-list-type" style='display:none;'>
        {% assign tool_projects = site.data.owaspprojects | where:'type', 'tool' %}
        {% assign documentation_projects = site.data.owaspprojects | where:'type', 'documentation' %}
        {% assign code_projects = site.data.owaspprojects | where:'type', 'code' %}
        {% assign other_projects = site.data.owaspprojects | where:'type', 'other' %}
        <h2>Herramientas <i style="margin-left:12px;" class="fa fa-tools fa-lg"></i></h2>
        <ul>
        {% for project in tool_projects %}
        <li><a href="{{ project.url }}">{{ project.title }}</a></li>
        {% endfor %}
        </ul>
        <h2>Documentación <i style="margin-left:12px;" class="fa fa-file-alt fa-lg"></i></h2>
        <ul> 
        {% for project in documentation_projects %}
        <li><a href="{{ project.url }}">{{ project.title }}</a></li>
        {% endfor %}
        </ul>
        <h2>Código <i style="margin-left:12px;" class="fa fa-file-code fa-lg"></i></h2>
        <ul>
        {% for project in code_projects %}
        <li><a href="{{ project.url }}">{{ project.title }}</a></li>
        {% endfor %}
        </ul>
        <h2>Otros </h2>
        <ul>
        {% for project in other_projects %}
        <li><a href="{{ project.url }}">{{ project.title }}</a></li>
        {% endfor %}
        </ul>
    </div>
</div>
<script type="text/javascript">
    $(function(){
        $('#projects-type').click(function(){
            $('#project-list-level').hide();
            $('#project-list-type').show();
            $('#projects-level').removeClass('active');
            $('#projects-type').addClass('active');
            $('#projects-level').addClass('inactive');
            $('#projects-type').removeClass('inactive');
        });
        $('#projects-level').click(function(){
            $('#project-list-type').hide();
            $('#project-list-level').show();
            $('#projects-type').removeClass('active');
            $('#projects-level').addClass('active');
             $('#projects-level').removeClass('inactive');
            $('#projects-type').addClass('inactive');
        });
    });
</script>


## Capítulos Locales
* Comunidades interesadas en Seguridad de Aplicaciones

## Desarrollo de nuevos proyectos
* Posibilidad de utilizar las herramientas y colaboradores disponibles para generar nuevos proyectos

## Becas de Investigación
* OWASP otorga becas a investigadores de la seguridad en aplicaciones para desarrollar herramientas, guias, publicaciones, etc.
