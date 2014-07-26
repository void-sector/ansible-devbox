ansible/role-mysql
==================

Provides mysql installation.

Configuration
-------------

You can configure the database and users to create like so (either in your 
playbook or group_vars):

mysql:
  clients:
  - 123.123.123.123
  - 321.321.321.321
  credentials:
  - {
      dbname: database01,
      username: username01,
      password: password01
    }
  - {
      dbname: database02,
      username: username02,
      password: password02
    }