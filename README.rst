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