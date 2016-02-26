# chef-mailhog

[![CK Version](http://img.shields.io/cookbook/v/mailhog.svg)](https://supermarket.getchef.com/cookbooks/mailhog)

This cookbook installs [MailHog](https://github.com/mailhog/MailHog).

This fork includes a change to fix the error from Vagrant Chef Zero shown below.

```
template[/etc/sv/mailhog/log/run] (/var/chef/cache/cookbooks/runit/libraries/provider_runit_service.rb line 143) had an error:
Chef::Exceptions::FileNotFound: Cookbook 'mailhog' (0.1.0) does not contain a file at any of these locations:
```

Usage
-----

Include the mailhog recipe to install MailHog on your system:
```chef
include_recipe "mailhog"
```

MailHog service is installed and managed via `runit`.

Requirements
------------

### Cookbooks:

* runit

### Platforms:

* Ubuntu
* Debian
* RHEL
* CentOS
* Fedora

License
-------

Copyright (c) 2015 Sergey Storchay, http://r8.com.ua

Licensed under MIT:
http://raw.github.com/r8/chef-mailhog/master/LICENSE
