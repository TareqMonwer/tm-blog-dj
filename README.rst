==========
tm-blog-dj
==========

TM Blog Django is a Django app to conduct Web-based articles. 

Detailed documentation is in the "docs" directory.

Quick start
-----------

1. Add "tm_blog_dj" to your INSTALLED_APPS setting like this::

    INSTALLED_APPS = [
        ...
        'tm_blog_dj',
    ]

2. Include the polls URLconf in your project urls.py like this::

    path('blog/', include('tm_blog.urls')),

3. Run ``python manage.py migrate``.

4. Start the development server and visit http://127.0.0.1:8000/admin/
   to create a poll (you'll need the Admin app enabled).

5. Visit http://127.0.0.1:8000/blog/


IMPORTANT:
----------

This project makes use of these libraries listed:
+  `allauth` for authentication.
+ `crispy_forms` for forms.
+ `ckeditor` for rich-text-editor. This means, you need to use `ckeditor_uploader` in your INSTALLED_APPS, and 
include `ckeditor_uploader.urls` in you root `URLconf`.
You need to define ``CKEDITOR_UPLOAD_PATH = 'ck-uploads/'``, ``CKEDITOR_IMAGE_BACKEND = "pillow"`` & ``CKEDITOR_ALLOW_NONIMAGE_FILES = False`` in your settings file as well.
+ Media settings should be provided as well:
urlpattern + static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT) MEDIA_ROOT and MEDIA_URL should be defined in settings.py.
+ For additional features in ckeditor, use this snippet in settings.py:
```
# CKEDITOR
CKEDITOR_CONFIGS = {
    'default': {
        'toolbar': 'full',
        'extraPlugins': ['codesnippet', 'markdown'],
        'width': '100%',
    },
}
```