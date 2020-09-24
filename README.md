## Keycloak Chart

An example chart for deploying a Keycloak on Openshift



## Creating new release

```
git checkout release
helm package .
mv  keyclaok-chart*.tgz release/
helm repo index --url https://jaland.github.io/keyclaok-helm-chart/ .
git add --all
git commit -m "Release x.x.x"
```




## Testing chart

### Add helm repo
```
helm repo add keyclaok https://jaland.github.io/keyclaok-helm-chart/
helm repo list
```

### Deploy chart
```
helm repo update
helm install keyclaok/keyclaok-chart --name-template keyclaok
```