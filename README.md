Role Name
=========

A role to install `Apache Tomcat`.

Requirements
------------

`Apache Tomcat` requires `Java`. if `Java` is installed on the hosts, specify it's location via `java_home` environment variable. Otherwise, `chubock.java` role which this role declares a dependency on will install `java` at `java_home` location. for more information about `chubock.java` visit [ansible-role-java](https://github.com/chubock/ansible-role-java). 

Role Variables
--------------

following variables are defined at defaults/main.yml:

    java_home: /opt/java/default
    apache_tomcat_url: https://ftp.fau.de/apache/tomcat/tomcat-9/v9.0.41/bin/apache-tomcat-9.0.41-windows-x64.zip
    catalina_home: /opt/tomcat/apache-tomcat-8.5.57
    apache_tomcat_service_template: apache-tomcat.service.j2

you can use your own template for `systemd` service with `apache_tomcat_service_template`.

Dependencies
------------

This role is dependent on `chubock.java`. for more information visit [ansible-role-java](https://github.com/chubock/ansible-role-java).

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: tomcat
      roles:
         - { role: chubock.apache-tomcat, java_home: /opt/java/default }

License
-------

Apache-2

Author Information
------------------

I'm a Software Developer with more than 5 years of experience in software industry. you can contact me via my email: chubock@gmail.com and my linkedin account: https://www.linkedin.com/in/chubock/
