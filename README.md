## Keycloak Chart

An example chart for deploying a Keycloak on Openshift



## Creating new release

```
git checkout release
helm package .
mv  keycloak-chart*.tgz release/
helm repo index --url https://jaland.github.io/keycloak-helm-chart/ .
git add --all
git commit -m "Release x.x.x"
```




## Testing chart

### Add helm repo
```
helm repo add keycloak https://jaland.github.io/keycloak-helm-chart/
helm repo list
```

### Deploy chart
```
helm repo update
helm install keycloak/keycloak-chart --name-template keycloak
```

1.0.0
