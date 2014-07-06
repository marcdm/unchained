Unchained - (experimental fork)
=========

Experiments with common helper functions to help Django break free. 
Get the real version of  Unchained at Aychedee's repo here : 
https://github.com/aychedee/unchained

Install
=======
To install (the real thing), use this command :

    pip install git+https://github.com/aychedee/unchained.git


Usage
=====


Sending html emails properly
----------------------------

    from unchained import send_html_email

    send_html_email(
        'A Subject',
        'template_stub',
        'sender@mail.com'
        ['a@b.c', 'b@c.a']
    )

This relies on having two files in your templates directory. One called
`template_stub.txt` and the other called `template_stub.html`


Storing json as json in Postgres
--------------------------------

A JSON field type for your models that will accept Python strings, lists, or
dicts and convert them back to the appropriate type on the way out.

    from django.db import models
    from unchained.fields import import JSONField

    class AModel(models.Model):
        data = JSONField()

