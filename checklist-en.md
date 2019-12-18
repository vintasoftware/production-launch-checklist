## Content
 * [ ] Spell-check copy
 * [ ] Check links are correct
 * [ ] Check the website is retina compatible
 * [ ] Set favicon
 * [ ] Customize the default error views
 * [ ] Check you have dumb 500 error pages, the least logic in it minimizes the risk of infinite break redirects
 * [ ] Test target browsers compatibility
 * [ ] Guarantee the application is mobile-friendly: http://bit.ly/ggl-mobile-friendly-tool 

## Accessibility
 * [ ] Check accessibility on Wave: http://bit.ly/wave-web-tool

## SEO & Analytics
 * [ ] Configure Google Tag Manager: http://bit.ly/tag-manager-tool
 * [ ] Run Google Webmasters Tools: http://bit.ly/ggl-webmasters-tools 
 * [ ] Make a robots.txt
 * [ ] Make a sitemap.xml
 * [ ] Check pages have descriptive and unique titles
 * [ ] Check meta descriptions are unique

## Performance
 * [ ] Check HTML, CSS and JS files are minified
 * [ ] Guarantee correct viewport `<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">`: http://bit.ly/boot-starter-template 
 * [ ] Check performance on Google Page Speed: http://bit.ly/ggl-page-speed-tool
 * [ ] Check performance on GTmetrix: http://bit.ly/gtmetrix-tool
 * [ ] Scan your site on webhint: http://bit.ly/webhint-tool

## Transactional Emails
 * [ ] Check if email templates are correct
 * [ ] Configure SendGrid, Mailgun, or another transactional email service
 * [ ] Set an automatic BCC for admins
 * [ ] Save metadata of every email sent

 ## Monitoring
 * [ ] Check no sensitive data is being logged
 * [ ] Check if logs are prefixed according to task/feature
 * [ ] Configure Papertrail or another logging service
 * [ ] Set Papertrail alerts and integrate with Slack and email  
 * [ ] Configure Sentry or another error tracking service
 * [ ] Configure Uptime monitoring
 * [ ] Configure New Relic or another application monitoring service

## Security
 * [ ] Check the SaaS CTO Security Checklist: http://bit.ly/sqreen-security-checklist
 * [ ] Run Observatory: http://bit.ly/mozilla-observatory  
 * [ ] Add all accesses of third-party tools to LastPass, or other password manager service
 * [ ] Update OAuth callback/deauthorize URLs in all third-party services
 * [ ] Rotate OAuth keys of all third-party services
 * [ ] Change passwords of all third-party services
 * [ ] Check if buckets/blob storages of AWS/Azure are private
 * [ ] Setup AWS S3 buckets encryption
 * [ ] Check interactive shells are read-only

## DNS
 * [ ] Check records
 * [ ] Check TTL, set low when launching, set high after everything is fine
 * [ ] Configure a custom domain
 * [ ] Move API to a different subdomain (like `api.example.org`), this allows a different server for frontend
 * [ ] Enforce or remove www subdomain

## Server
 * [ ] Check if latest server stack is being used
 * [ ] Check if latest server OS version is being used
 * [ ] Check if latest server Python version is being used
 * [ ] Configure Redis maxmemory and eviction policy (likely `volatile-ttl`)
 * [ ] Configure RabbitMQ: http://bit.ly/rabbitmq-production-checklist 
 * [ ] Configure SSL for everything
 * [ ] Test SSL health: http://bit.ly/ssl-server-test 
 * [ ] Configure SSL certificates autorenewal
 * [ ] Tune PostgreSQL settings: http://bit.ly/pgtune-tool
 * [ ] Configure database backups generation scripts
 * [ ] Configure entire database server disk backup
 * [ ] Guarantee Celery and other services aren't running as sudo
 * [ ] Configure application firewall for application servers
 * [ ] Limit file size for uploads
 * [ ] Validate uploads media types
 * [ ] Configure throttling
 * [ ] Configure autoscaling
 * [ ] Enable HTTP/2
 * [ ] Check if all services are able to handle autoscaling upper limits. (Eg.: will your Redis be able to handle connections if X servers are provisioned)
 * [ ] Configure DNS/caching 
	 * [ ] Enable Brotli Compression
	 * [ ] Check and enable the speed features that don't interfere with your application
 * [ ] Enable other speed/WAF features
