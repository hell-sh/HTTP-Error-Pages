# HTTP-Error-Pages

Fancy error pages for your web server.

- [400](https://errors.hell.sh/400.html)
- [401](https://errors.hell.sh/401.html)
- [403](https://errors.hell.sh/403.html)
- [404](https://errors.hell.sh/404.html)
- [408](https://errors.hell.sh/408.html)
- [410](https://errors.hell.sh/410.html)

## Apache Installation

You can simply run this command:

	wget -qO- https://installation.hell.sh/apache-http-error-pages | bash

or clone HTTP-Error-Pages into `/etc/apache2/http-error-pages`, and then add this to your `apache2.conf`:

	Alias /http-error-pages /etc/apache2/http-error-pages
	ErrorDocument 400 /http-error-pages/400.html
	ErrorDocument 401 /http-error-pages/401.html
	ErrorDocument 403 /http-error-pages/403.html
	ErrorDocument 404 /http-error-pages/404.html
	ErrorDocument 408 /http-error-pages/408.html
	ErrorDocument 410 /http-error-pages/410.html
	<Directory /etc/apache2/http-error-pages>
		AllowOverride None
		Require all granted
	</Directory>
