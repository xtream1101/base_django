Django Base
===========

The base app is used as a base template for all of your apps


Quick start
-----------
1. Add "base" to your INSTALLED_APPS setting like this:

    INSTALLED_APPS = (  
        ...  
        'base',  
    )

1. Include the inventory URLconf in your project urls.py like this:  
    `from django.views.generic import TemplateView`  
    `url(r'^$', TemplateView.as_view(template_name="base/index.html"), name='home'),`


Use  
---  

In your apps html template  
`{% extends 'base/base.html' %}`  
`{% block title %} App title here {% endblock %}`  
`{% block content %} app content {% endblock %}`  