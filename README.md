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
kubectl create ns guestbook
kapp -n guestbook deploy -a guestbook -f app/ -y
```

List the apps

```sh
kctrl app list -n kapp-packages
```

Get the guestbook app

```sh
kctrl app get -a guestbook -n kapp-packages
```

Describe the app with `kubectl`

```sh
kubectl describe app/guestbook -n kapp-packages
```

Inspect the app with `kapp`

```sh
kapp inspect -a guestbook -n guestbook
```

List the available packages

```sh
kctrl package available list -n kapp-packages
```

List the installed packages

```sh
kctrl package installed list -n kapp-packages
```
