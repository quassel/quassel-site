---
tags:
- security
title: A Bleeding Heart
---
Hi all,

as you should have heard by now, a <a href="http://heartbleed.com/">major security vulnerability</a> was discovered in OpenSSL. This does affect Quassel as well, as by default the connection between a Quassel client and core is encrypted using SSL (or, rather, TLS); in particular, it affects you if you run a core that supports SSL and is exposed to the public internet (clients, both monolithic and stand-alone, are not affected because they don't offer an SSL-encrypted service).
<ul>
<li>If you host a Quassel core, make sure to upgrade your OpenSSL to at least version 1.0.1g (or whatever your distro deems to be a fixed one), then restart the core. Create a new private key and certificate and replace the quasselCert.pem file in your config directory <a href="http://bugs.quassel-irc.org/projects/quassel-irc/wiki/Client-Core_SSL_support">as described here</a> and restart your core again. Since the vulnerability is in the OpenSSL library and not in Quassel itself, there is no need to update Quassel <b>unless one of the following bullet points applies:</b></li>
<li>If you run one of the static cores offered on our site, make sure to <a href="/downloads">download</a> the newest version; we uploaded a 0.10.0 core built against a fixed OpenSSL version on April 8th 2014, 19:14 UTC. Any older version is vulnerable, as an insecure OpenSSL version was bundled. After replacing the core, follow the previous step to regenerate your key and certificate.</li>
<li>If you use our install package for Windows™, and run the core from this package, make sure to <a href="/downloads">download</a> the newest version. We uploaded a fixed package on April 9th 2014, 20:47 UTC. Any older version is vulnerable. First bullet point applies as well.</li>
<li>Our MacOSX packages don't bundle OpenSSL; they use the system-supplied version instead. No need to install a newer Quassel core, but first bullet point applies.</li>
</ul>

After replacing the certificate and restarting your core, you should also change the passwords, as they may have leaked due to the vulnerability.

That's it. Have fun securing your systems; I know I had... NOT.

~ Sput
