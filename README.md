ECP
=========

This role installs and configures the EBI Cloud Portal, which consist of an API and webapp.

Requirements
------------

None

Role Variables
--------------

The first 2 variable define which papertrail destination to log to - remember to turn on 'self-registration'.
* `papertrail_host`: *.papertrailapp.com* is automatically added). For example *logs4*.
* `papertrail_port`: For example *12345*.
* `jenkins_user`: regular jenkins username
* `jenkins_token`: api token (see <jenkins url>/me/configure)
* `artifacts_source`: *master* or *dev* 
* `api_hostname`: which hostname the API is using (*.tsi.ebi.ac.uk* is automatically added)
* `app_hostname`: which hostname the webapp is using (*.tsi.ebi.ac.uk* is automatically added)

Dependencies
------------

TBC (see [galaxy meta](meta/main.yml) for the latest thoughts on the subject)

Example Playbook
----------------

This is an example of how to use this role:

    - hosts: servers
      roles:
         - { role: ecp, api_hostname: dev.api.portal, app_hostname: dev.portal }

Licence
-------
Released under the [MIT license](https://opensource.org/licenses/MIT).

Author Information
------------------

Amélie Cornélis ameliec@ebi.ac.uk
