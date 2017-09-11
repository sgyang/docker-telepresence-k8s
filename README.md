# Silent version of telepresence-k8s image

Just ignore the stdout outputs of telepresence-k8s.

[Telepresence](https://www.telepresence.io) is very useful and I love it.
But it is little bit annoying for me if telepresence-k8s emits tons of outputs of stdout when I use Kubernetes on GKE and run it on that, since GKE collects all of the outputs and automatically sends them to Stackdriver Logging which I usually watch and check even if the environment is just for development.

## How to use

Just set environment variable: `TELEPRESENCE_REGISTRY=sgyang`, that's it. See https://github.com/datawire/telepresence/blob/0.65/cli/telepresence#L47.

```
$ TELEPRESENCE_REGISTRY=sgyang teleplesence --method vpn-tcp
```
