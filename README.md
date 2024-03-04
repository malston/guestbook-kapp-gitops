# guestbook-kapp-gitops

- app - contains the manifests to deploy the guestbook app using the manifests under packaging
- packaging - contains the manifests to install the guestbook app as a package

## Install kapp-controller

```sh
kapp deploy -a kc -f https://github.com/carvel-dev/kapp-controller/releases/download/v0.50.0/release.yml -y
```


harbor.markalston.net/guestbook/kbld-gb-frontend@sha256:145634de65632c68e40ddebec5a4ed94e28e77ac6b068c1d114a04ad9a7f3323