On Ubuntu 16.04 using Ubuntu's Network Manager, kube-dns running in  minikube failed
when `--vm-driver=none` because `/etc/resolv.conf` was not setup to point to external
IP address.

This fix from [@jgoclawski](https://github.com/kubernetes/minikube/issues/2027#issuecomment-381574807)
seems to do the trick.

Modify the upstream list of dns servers to fit your needs.
