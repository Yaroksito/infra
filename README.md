# infra

What is is?

This repo explains how to schedule Kubernetes infrastructure workloads on infra nodes by using lables taints and tolerations.
Specifically, it describes how to place ODF, Cluster-Logging, Monitoring stack and router all togethers on the infra nodes.
It consists of a step by step procedure (see solution.yaml) along with the relevant yaml files.

Why?

1. In order to isolate infrastructure workloads and allow application to be schedule independently on worker nodes
2. In case of using OpenShift, placing infrastructure workloads in infra nodes saves subscription costs as well as isolation.

Refrences:
1. Infrastructure nodes in OpenShift 4 
https://access.redhat.com/solutions/5034771
2. How to add toleration for the "non-ocs" taints to the OpenShift Data Foundation pods?
https://access.redhat.com/articles/6408481
3. Moving the logging stack to infra/storage nodes
https://docs.openshift.com/container-platform/4.10/monitoring/configuring-the-monitoring-stack.html#moving-monitoring-components-to-different-nodes_configuring-the-monitoring-stack
https://docs.openshift.com/container-platform/4.10/logging/config/cluster-logging-moving-nodes.html
5. Configure elasticsearch-im cronjobs with toleration for infra/storage taints
https://access.redhat.com/solutions/6983629
7. Configure ODF deployments, CM, CR and subscription to tolerate infra taints
https://access.redhat.com/articles/6408481
9. toleration for "non-ocs" taints OpenShift Data Foundation pods
https://bugzilla.redhat.com/show_bug.cgi?id=2122980
https://bugzilla.redhat.com/show_bug.cgi?id=2121842
