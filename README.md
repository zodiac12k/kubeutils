# kubeutils
Useful kubernetes utilities

## kubecm

### Before you begin

This utility use only for Mac OS.
Not validated in other OS(Windows, Linux).

You must install `yq` to use this utility.
```
$ brew install yq
```

I recommend to install `kubectx`, `kube-ps1`, `k9s` to operate multi cluster easily.
```
$ brew install kubectx
$ brew install kube-ps1
$ brew install k9s
```

### Installation

for example:
```
sudo git clone https://github.com/zodiac12k/kubeutils /opt/kubeutils
sudo ln -s /opt/kubeutils/kubecm /usr/local/bin/kubecm
```

### Usage
```
$ kubecm
/tmp/kube-config-dummy-6A01475C-86A8-4AAB-B5B3-5590BA018E1F.yml:/Users/aaa.bluemix/plugins/container-service/clusters/bbb-admin/kube-config-ccc.yml:/Users/xxx/.bluemix/plugins/container-service/clusters/yyy-admin/kube-config-zzz.yml:

$ kubecm -r
Start reload KUBECONFIG
Finish reload KUBECONFIG
/tmp/kube-config-dummy-6A01475C-86A8-4AAB-B5B3-5590BA018E1F.yml:/Users/aaa.bluemix/plugins/container-service/clusters/bbb-admin/kube-config-ccc.yml:/Users/xxx/.bluemix/plugins/container-service/clusters/yyy-admin/kube-config-zzz.yml:
```
