See INSTALL.txt for installation instructions.

See docs/html/index.html and docstrings for documentation.

If you have a git working tree rather than a release, you'll only have
the markdown source, e.g. mechanize/index.txt; release.py is used to
build the HTML docs.


<h1>Changes</h1>

<ul>
  <li>browser bootstrap</li>
  <li>cookie jar bootstrap</li>
</ul>

<h1>Motivation</h1>
<p>I have been a long time web crawling fan and have often used this library to crawl around the web.
I've found that I always end up repeating the same sort of bootstrapping for some of the super handy
objects that this library supplies.
</p>

<h1>Example</h1>
<p><b>Old</b></p>
<code>from mechanize import Browser</code>
<br>
<code>br = Browser()</code>
<br>
<code>br.set_handle_equiv(True)</code><br>
<code>br.set_handle_http(True)</code><br>
<code>...</code><br>
<code>from cookielib import LWPCookieJar</code><br>
<code>cookiejar = LWPCookieJar()</code><br>
<code>br.set_cookiejar(cookiejar)</code><br>
<code>br. ....</code><br>
<br>
<p><b>New</b></p>
<code>from mechanize import Browser</code>
<br>
<code>br = Browser()</code>
<br>
<code>br.bootstrap()</code>


<p>Go crawl the web without worrying about any stupid robots.txt nonsense with your emulated, bootstrapped and user-agent mocking browser</p>
