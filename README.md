# ion_auth-adldap2-codeigniter
Active Directory authentication for Codeigniter on Ion Auth basis

This piece of software can be used with Codeigniter 3 to authenticate against
Active Directory domain controllers (or Samba4 domain controllers).

The software is intended to be used on intranets.

## Installation

- ensure that you are using PHP 7.x
- install Codeigniter 3
- install Ion-Auth
- install adldap2 using composer:  `composer require adldap2/adldap2`
- configure codeigniter and ion auth
- review and configure the adauth config file
- initiate migration

### Codeigniter configuration.

You can set up ion auth in application third_party directory as well.
In order to use it please add the below in your config/autoload.php file

<code>
$autoload['packages'] = array(APPPATH . 'third_party/ion_auth');
</code>

## What is included

- Bootstrap 3.3.7    http://getbootstrap.com/
- Font Awsome 4.7.0  http://fontawesome.io/

## How it works

The Adauth controller is basically a "butchered" version of Ion Auth's Auth controller
It will try to authenticate you against the local database first and if it is
unsuccessful then it will try to authenticate with the domain controller.
If the athentication against the domain controller was successful it will create
the user locally. Otherwise it works the same way as Ion Auth.

## Credits:
- [Codeigniter](https://codeigniter.com/)
- [Ion Auth](http://benedmunds.com/ion_auth/)
- [Adldap2](https://github.com/Adldap2/Adldap2)
- [Bootstrap 3.3.7](https://getbootstrap.com/docs/3.3/)
- [Font Awesome by Dave Gandy - http://fontawesome.io](http://fontawesome.io/)
- [jQuery](https://jquery.com/)
- [DataTables](https://www.datatables.net/)


> This is my first attempt at sharing something that i've written for myself :)
> Feel free to point out issues or contribute changes.