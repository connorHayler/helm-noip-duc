# NoIp Duc Helm Chart

Repository hosting a helm chart for NoIp Duc

## Get started

Add the repository to helm

```
helm repo add connorHayler https://connorHayler.github.io/helm-noip-duc
```

Install the chart

```
helm install noip-duc connorHayler/noip-duc --set config.auth.username=$USERNAME,config.auth.password=$PASSWORD --namespace $NAMESPACE
```

\$USERNAME, \$PASSWORD, and \$NAMESPACE all should be either substituted out for your values or set as vars for this to read in

## Configuration

All environment variables are available to be used via this helm chart. These will need appending to the set arg in the scheme key1=val1,key2=val2
NOIP_HOSTNAMES is by default set to `all.ddnskey.com` so if you aren't using groups you don't need to set this
These are the keys to set for the corresponding env var
```
config.hostnames = NOIP_HOSTNAMES
config.checkInterval = NOIP_CHECK_INTERVAL
config.daemon.group = NOIP_DAEMON_GROUP
config.daemon.pidFile = NOIP_DAEMON_PID_FILE
config.daemon.user = NOIP_DAEMON_USER
config.execOnChange = NOIP_EXEC_ON_CHANGE
config.httpTimeout = NOIP_HTTP_TIMEOUT
config.method = NOIP_IP_METHOD
config.logLevel = NOIP_LOG_LEVEL
```