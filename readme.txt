=== reCaptcha Protected Downloads ===
Contributors: elhardoum
Tags: content, shortcode, download, spam, anti-spam, link, media, file, captcha, google, recaptcha
Requires at least: 4.7.2
Tested up to: 4.7.2
Stable tag: 0.1
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html
Author URI: http://samelh.com/
Donate link: http://samelh.com/

Protect your downloads from bots and spiders with a shortcode and Google's no-captcha reCaptcha

== Description ==

<p>Upon copying the plugin folder to /wp-content/plugins/, you may activate it by going to your plugins page. Once activated, click on the plugin's settings and enter the public/private reCAPTCHA keys obtained from Google.</p>

<p>My version of this plugin will convert any .pdf links, in href, to the hash, and apply the reCAPTCHA prompt to these links. Upon first loading the page, a session will be created, lasting for 3 hours, look at SESSION_TIME_LIMIT in recaptcha-protected-downloads.php if you'd like to change this. Once a reCAPTCHA is first solved, the other links will be clickable without a need to solve another reCAPTCHA, until the session is expired.</p>

<strike><p>Use the shortcode <code>[recaptcha-protected-download]</code> to wrap any direct download link that you'd like reCaptcha to process.</p></strike>

<strike><p><code>[recaptcha-protected-download]https://example.com/download.zip[/recaptcha-protected-download]</code></p></strike>

<strong>Example</strong><strike>

<p>Here's my <code>hello world</code> post HTML:</p>

<pre>
<a href="https://www.irs.gov/pub/irs-pdf/fw4.pdf" target="_blank">IRS</a>
</pre>

<p>Which is parsed as follows:</p>

<pre>
<a href="#rcpdl=fc17b5220ce042f809ea732722215ee5" target="_blank">IRS</a>
</pre>

<strong>About</strong>

<p>First, much thanks to elhardoum, as this is based entirely on his original code: https://github.com/elhardoum/recaptcha-protected-downloads. I needed to apply reCAPTCHA to my links as this pluging originally does, but also needed the following:</P>

<ul>
<li>Apply reCAPTCHA to PDF links without the need for shortcodes.</li>
<li>Enforce reCAPTCHA once, start a session, and re-enforce reCAPTCHA upon session expiration.</li>
</ul>

Thank you!

== Installation ==

1. Visit 'Plugins > Add New'
2. Search for 'reCaptcha Protected Downloads'
3. Activate reCaptcha Protected Downloads from your Plugins page. You will have to activate it for the whole network.

Once you activate the plugin, you should now navigate to "Settings" > "reCaptcha Downlaods" (or "Options" > "reCaptcha Downlaods" for network activated plugin) and add your Google reCaptcha credentials (public and private keys) which you can obtain from https://www.google.com/recaptcha/admin

== Screenshots ==

1. reCaptcha popup after clicking download link

== Changelog ==

= 0.1.0 =
* Customized to include the following: 
- Apply reCAPTCHA to PDF links without the need for shortcodes.
- Enforce reCAPTCHA once, start a session, and re-enforce reCAPTCHA upon session expiration.

= 0.1 =
* Initial stable release.