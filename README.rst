ASP .NET on Apache with Mod Mono - Free .NET hosting
====================================================

`Mono`_ has an open source implementation of ASP.NET 4.5, ASP.NET MVC
and ASP.NET AJAX that can be used to host ASP .NET web applications on
Linux. This provides a great free alternative to Microsoft's .NET 
stack. Apache is used to pass off requests for ASP.NET pages to the
embedded Mono application server.

This appliance includes all the standard features in `TurnKey Core`_,
and on top of that:

- Apache ASP .NET hosting using `mod\_mono`_, a module that allows
  Apache to serve ASP .NET applications.
   
   - mod_mono and associated packages and dependencies are installed
     direct from `Xamarin apt repo`_.
   - mono-server4 is configured to use /var/www as the webroot
   - Includes a MySQL .NET Connector.

   **Security note**: Updates to Xamarin packages may require supervision
   so they **ARE NOT** configured to install automatically. See below for
   updating.

- Interactive Mono CSharp shell.
- TurnKey Web Control panel with links to useful references and
  resources, and ASP .NET example pages.
- SSL support out of the box.
- Postfix MTA (bound to localhost) to allow sending of email (e.g.,
  password recovery).
- Webmin modules for configuring Apache2, MySQL and Postfix.

Supervised Manual Mono Updates
------------------------------

To upgrade to the latest version of mod_mono, etc from the command line::

    apt-get update
    apt-get install libapache2-mod-mono mono-apache-server4 asp.net-examples

Credentials *(passwords set at first boot)*
-------------------------------------------

-  Webmin, SSH, MySQL: username **root**


.. _Mono: http://www.mono-project.com/ASP.NET
.. _TurnKey Core: https://www.turnkeylinux.org/core
.. _mod\_mono: http://www.mono-project.com/Mod_mono
.. _Xamarin apt repo: https://www.mono-project.com/download/stable/#download-lin-debian
