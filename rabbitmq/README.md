RabbitMQ server
==========

## RabbitMQ

This playbook installs RabbitMQ on Ubuntu system from official rabbitmq repository.
Default included plugins: rabbitmq_management,rabbitmq_tracing

### Vars

* **rabbitmq_plugins**: Install rabbitmq plugins
    * Type: String
    * Default: rabbitmq_management,rabbitmq_tracing
