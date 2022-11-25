# Puppet create Symlinks
```
sudo su -

cd /etc/puppetlabs/code/environments/production/manifests

ll
```
```
vi apps.pp
```
```
class symlink {

  # First create a symlink to /var/www/html

  file { '/opt/finance':

    ensure => 'link',

    target => '/var/www/html',

  }

   # Now create media.txt under /opt/finance

  file { '/opt/finance/media.txt':

    ensure => 'present',

  }

}

node 'stapp03.stratos.xfusioncorp.com' {

  include symlink

}
```
```
puppet parser validate games.pp

ssh banner@stapp03

sudo su -

ll /var/www/html/

puppet agent -tv

ll /var/www/html/

ll /opt/finance
```


