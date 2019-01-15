#!/bin/bash
set -eo pipefail

# A RabbitMQ node is considered healthy if all the below are true:
# * the rabbit app finished booting & it's running
# * there are no alarms
# * there is at least 1 active listener

rabbitmqctl eval '
{ true, rabbit_app_booted_and_running } = { rabbit:is_booted(node()), rabbit_app_booted_and_running },
{ [], no_alarms } = { rabbit:alarms(), no_alarms },
[] /= rabbit_networking:active_listeners(),
rabbitmq_node_is_healthy.
' || exit 1
