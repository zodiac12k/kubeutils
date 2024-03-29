# kubeutils
Useful kubernetes utilities

## kubecm

`kubecm` is called kubernetes config manager or kubernetes config merger.

### Why this utility is born?

If you download the kubeconfig via ibmcloud cli `ibmcloud ks cluster config CLUSTER_NAME`, you can export only one kubernetes config.

`kubectx` helps you switch among multiple clusters, but you cannot export multiple kubernetes configs easily for IBM kubernetes service.

So this utility helps you manage and merge KUBECONFIG downloaded from IBM kubernetes service.

### Before you begin

This utility can use only for Mac OS. It's not validated in other OS(Windows, Linux).

I recommend to install [kubectx](https://github.com/ahmetb/kubectx), [kube-ps1](https://github.com/jonmosco/kube-ps1), [k9s](https://github.com/derailed/k9s) to operate multi cluster easily.
```
$ brew install kubectx
$ brew install kube-ps1
$ brew install derailed/k9s/k9s
```

### Installation

for example:
```
sudo git clone https://github.com/zodiac12k/kubeutils /opt/kubeutils
sudo ln -s /opt/kubeutils/kubecm /usr/local/bin/kubecm
```

If you want to reload automatically KUBECONFIG when your terminal session open:
For zsh:
```
echo "source kubecm -r" >> ~/.zshrc
source ~/.zshrc
```
For bash:
```
echo "source kubecm -r" >> ~/.bashrc
source ~/.bashrc
```

### Usage
```
$ kubecm
/tmp/kube-config-dummy-6A01475C-86A8-4AAB-B5B3-5590BA018E1F.yml:/Users/aaa/.bluemix/plugins/container-service/clusters/bbb-admin/kube-config-ccc.yml:/Users/xxx/.bluemix/plugins/container-service/clusters/yyy-admin/kube-config-zzz.yml:

$ kubecm -r
Start reload KUBECONFIG
Finish reload KUBECONFIG
/tmp/kube-config-dummy-6A01475C-86A8-4AAB-B5B3-5590BA018E1F.yml:/Users/aaa/.bluemix/plugins/container-service/clusters/bbb-admin/kube-config-ccc.yml:/Users/xxx/.bluemix/plugins/container-service/clusters/yyy-admin/kube-config-zzz.yml:
```
