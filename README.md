# VRLI for TKGs/m

this is all of the k8s resources needed to deploy fluentd configured for VRLI in TKG. this also adds a new field to all logs for cluster name

## Usage

1. update the li-k8s.yml or vrlic-k8s(for loginishgt cloud) and replace the instances of `<LOGINSIGHT-IP>` with your instance's IP or fqdn
2. if using vrlic also update the `<api_token>`
3. replace `<CLUSTER-NAME>` with your k8s cluster name, this will be added to all logs as the `kubernetes_cluster_name`
4. `kubectl apply -f li-k8s.yml`


## Note on Cluster Name

this field can have any name that you want. however it makes most sense to tie this to the name that other tooling such as TO use for cluster name that way it can be correlated.  for example to TO and TMC integration the cluster name might look like `tbs2.pa-warroyo.aws-hosted.tmc`