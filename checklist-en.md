## Frontend Checklist
  * [ ] Spell-check copy
  * [ ] Set favicon
  * [ ] Customize the default error views: https://docs.djangoproject.com/en/2.0/howto/deployment/checklist/#customize-the-default-error-views
  * [ ] Run Observatory: https://observatory.mozilla.org/
  * [ ] Check Google Page Speed: https://developers.google.com/speed/pagespeed/
  * [ ] Run Google Webmaster Tools: https://www.google.com/webmasters/tools/home
  * [ ] Guarantee Mobile-Friendly: https://search.google.com/test/mobile-friendly
  * [ ] Guarantee correct viewport `<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">`: https://getbootstrap.com/docs/4.0/getting-started/introduction/#starter-template
  * [ ] Make robots.txt
  * [ ] Make a sitemap.xml using Django

## DNS checklist
  * [ ] Check records
  * [ ] Check TTL, set low when launch, set high after everything is fine
  * [ ] Move API to different subdomain (like `api.example.org`), this allows a different server for frontend
  * [ ] Enforce or remove www subdomain (and set `PREPEND_WWW` in Django if necessary)

## Server Checklist
  * [ ] Check if latest Heroku stack is being used
  * [ ] Check if latest server OS version is being used
  * [ ] Check if latest server Python version is being used
  * [ ] Configure Redis maxmemory and eviction policy (likely `noeviction`)
  * [ ] Configure RabbitMQ: https://www.rabbitmq.com/production-checklist.html
  * [ ] Configure SSL for everything
  * [ ] Test SSL health: https://www.ssllabs.com/ssltest/index.html
  * [ ] Configure SSL certificates autorenewal
  * [ ] Set a Heroku "Standard" database or higher
  * [ ] Tune PostgreSQL settings: http://pgtune.leopard.in.ua/
  * [ ] Configure database backups generation scripts
  * [ ] Configure entire database server disk backup
  * [ ] Guarantee Celery and other services aren't running as sudo
  * [ ] Configure application firewall for application servers
  * [ ] Limit file size for uploads
  * [ ] Validate uploads media types: http://blog.hayleyanderson.us/2015/07/18/validating-file-types-in-django/
  * [ ] Configure throttling

## Django Checklist
  * [ ] Run `python manage.py check --deploy` in production
  * [ ] Anonymize the URLs for Admin, Celery Flower, etc.
  * [ ] Check redirections, especially if it's a new platform replacing an old one
  * [ ] Properly set `ALLOWED_HOSTS`
  * [ ] Guarantee `DEBUG = False`
  * [ ] Change `SECRET_KEY`
  * [ ] Set `APPEND_SLASH = True`
  * [ ] Set `CSRF_COOKIE_SECURE = True`
  * [ ] Set `SESSION_COOKIE_SECURE = True`
  * [ ] Check `SECURE_PROXY_SSL_HEADER`, see: https://docs.djangoproject.com/en/2.0/ref/settings/#std:setting-SECURE_PROXY_SSL_HEADER
  * [ ] Set `SECURE_SSL_REDIRECT = True`
  * [ ] Check if `XFrameOptionsMiddleware` is being used: https://docs.djangoproject.com/en/2.0/ref/clickjacking/#clickjacking-prevention
  * [ ] Set HTTP Strict Transport Security: https://docs.djangoproject.com/en/2.0/ref/middleware/#http-strict-transport-security
  * [ ] Set `SECURE_CONTENT_TYPE_NOSNIFF = True`
  * [ ] Set `SECURE_BROWSER_XSS_FILTER = True`
  * [ ] If using subdomains, set `SESSION_COOKIE_DOMAIN`: https://docs.djangoproject.com/en/2.0/topics/http/sessions/#session-security
  * [ ] Set and test `ADMINS` for 500 errors emails
  * [ ] Set and test `MANAGERS` for 404 errors emails
  * [ ] Check CORS settings, use https://github.com/ottoyiu/django-cors-headers
  * [ ] Consider `ATOMIC_REQUESTS` for more DB integrity: https://docs.djangoproject.com/en/2.0/topics/db/transactions/#tying-transactions-to-http-requests
  * [ ] Save metadata of every email sent, use http://anymail.readthedocs.io/en/stable/sending/signals/
  * [ ] Check if `DEFAULT_FROM_EMAIL` is set to a friendly replyable email
  * [ ] Check if email templates are correct
  * [ ] Set `upload_to` argument for all `FileField` and `ImageField`
  * [ ] Use environment variables, not hardcoded settings

## Third-party Checklist
  * [ ] Add all accesses of third-party tools to LastPass
  * [ ] Configure Papertrail, or other logging service
  * [ ] Configure Sentry for backend, including Celery
  * [ ] Configure Sentry for frontend
  * [ ] Configure Mailgun, or other transactional email service
  * [ ] Configure Cloudflare cache for frontend assets
  * [ ] Configure Uptime Robot
  * [ ] Setup Google Tag Manager
  * [ ] Update OAuth callback/deauthorize URLs in all third-party services
  * [ ] Rotate OAuth keys of all third-party services
  * [ ] Change passwords of all third-party services
  * [ ] Check if buckets/blob storages of AWS/Azure are private
  * [ ] Check the SaaS CTO Security Checklist: https://www.sqreen.io/checklists/saas-cto-security-checklist