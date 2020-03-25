## 6/ Configuring Symfony (and Environments)
https://symfony.com/doc/3.4/configuration.html

+ Every Symfony application consists of a collection of bundles that add useful tools (services) to your project. 

```YAML
app/config/config.yml
imports:
    - { resource: parameters.yml }
    - { resource: security.yml }
    - { resource: services.yml }
    - { resource: easy_admin.yml }
    - { resource: "@MccpSalesBundle/Resources/config/config.yml"}