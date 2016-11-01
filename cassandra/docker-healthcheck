#!/bin/bash
set -eo pipefail

host="$(hostname --ip-address || echo '127.0.0.1')"

if cqlsh -u cassandra -p cassandra "$host" < /dev/null; then
	exit 0
fi

exit 1
