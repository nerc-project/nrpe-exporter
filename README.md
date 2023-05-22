# NRPE Metrics Exporter on OpenShift

This project deploys prometheus node-exporter configured to expose results of checks done by running of a collection of [NRPE][1] scripts.

Implementation is based on deployment of [ipmi-exporter][2] with many helpful details documented there.

[1]: <https://exchange.nagios.org/directory/Addons/Monitoring-Agents/NRPE--2D-Nagios-Remote-Plugin-Executor/details> (NRPE)

[2]: <https://github.com/OCP-on-NERC/ipmi-exporter> (ipmi-exporter)
