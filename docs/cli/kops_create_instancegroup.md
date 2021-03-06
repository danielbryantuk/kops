## kops create instancegroup

Create an instancegroup.

### Synopsis


Create an instancegroup configuration.  kops has the concept of "instance groups", which are a group of similar virutal machines. On AWS, they map to an AutoScalingGroup. An ig work either as a Kubernetes master or a node.

```
kops create instancegroup
```

### Examples

```
  # Create an instancegroup for the k8s-cluster.example.com cluster.
  kops create ig --name=k8s-cluster.example.com node-example \
  --role node --subnet my-subnet-name
```

### Options

```
      --role string          Type of instance group to create (Node,Master,Bastion) (default "Node")
      --subnet stringSlice   Subnets in which to create instance group
```

### Options inherited from parent commands

```
      --alsologtostderr                  log to standard error as well as files
      --config string                    config file (default is $HOME/.kops.yaml)
      --log_backtrace_at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log_dir string                   If non-empty, write log files in this directory
      --logtostderr                      log to standard error instead of files (default false)
      --name string                      Name of cluster
      --state string                     Location of state storage
      --stderrthreshold severity         logs at or above this threshold go to stderr (default 2)
  -v, --v Level                          log level for V logs
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO
* [kops create](kops_create.md)	 - Create a resource by command line, filename or stdin.

