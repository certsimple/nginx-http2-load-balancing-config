## An nginx config for 2017

nginx has [excellent official documentation](https://www.nginx.com/resources/wiki/start/) but putting all the logic together can take a while. Here's an `nginx.conf` with:

 - HTTP/2
 - IPv6
 - Load balancing between multiple app servers
 - A sorry page (shown if all the app servers go down)
 - Static content served on a separate server
 - HTML5 SSE support
 - Correct proxy headers for working GeoIP
 - The various www vs non-www, HTTP vs HTTPS combinations redirected to a single HTTPS site

See the [full documentation at CertSimple](https://certsimple.com/blog/nginx-http2-load-balancing-config), including diagrams and explanations for why particular values were chosen.

## Pull requests welcome

If you have useful changes or additions you're welcome to send pull requests. Try and use include files in `conf.d` where possible!