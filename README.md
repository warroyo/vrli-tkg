# VRLI for TKGs/m

this is all of the k8s resources needed to deploy fluentd configured for VRLI in TKG.

## Usage

1. update the li-k8s.yml and replace the instances of `<LOGINSIGHT-IP>` with your instance's IP or fqdn
2. `kubectl apply -f li-k8s.yml`