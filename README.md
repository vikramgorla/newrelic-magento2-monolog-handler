# New Relic Magento 2 Monolog Handler
This is an extension of NewRelic PHP Monolog Enricher to Push Magento 2 Logs to New Relic Logs API.

This extension on its own just implements Handler Class, Processor Class is implemented by [vgorla/newrelic-magento2-monolog-processor](https://github.com/vikramgorla/newrelic-magento2-monolog-processor) which can be installed indepdently without Handler if you have any existing log forwarders to send logs to New Relic.
Processor extension is infact added as a dependany to this module to exploit logs in context functionality of New Relic logs.

### Installation

Using Composer :

```
$ composer require vgorla/newrelic-magento2-monolog-handler
```

Enable Distributed Tracing :

[Enable Distributed Tracing](https://docs.newrelic.com/docs/distributed-tracing/enable-configure/language-agents-enable-distributed-tracing/#php-config) in your New Relic Configuration file (normally newrelic.ini), enabling infinite tracing is not mandatory for in context logs to work.
```
newrelic.distributed_tracing_enabled = true
newrelic.span_events_enabled = true
```
Read more about New Relic logs in context here : 
[New Relic PHP: Configure logs in context](https://docs.newrelic.com/docs/logs/enable-log-management-new-relic/configure-logs-context/configure-logs-context-php/#php-monolog)