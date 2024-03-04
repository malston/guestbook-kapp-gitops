# guestbook-kapp-gitops

- app - contains the manifests to deploy the guestbook app using the manifests under packaging
- packaging - contains the manifests to install the guestbook app as a package

## Install kapp-controller

```sh
kapp deploy -a kc -f https://github.com/carvel-dev/kapp-controller/releases/latest/download/release.yml -y
```

## Deploy the app

We're going to deploy the app manually for now.

```sh
kapp -n default deploy -a guestbook -f app/ -y
```
