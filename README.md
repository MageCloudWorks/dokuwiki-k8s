# dokuwiki-k8s
Dokuwiki Kubernetes Deployment 

## Deploy in kubernetes
```
kubectl apply -f dokuwiki.yaml
```
## Install Dokuwiki
### Get latest version of Dokuwiki
Check for latest version https://github.com/splitbrain/dokuwiki/tags

### Install into Kubenetes Persistent Volume
```
kubectl exec -it deployment/dokuwiki -- bash -c 'curl -L https://github.com/splitbrain/dokuwiki/archive/refs/tags/release_stable_2020-07-29.tar.gz | tar xzv --strip-components=1'
kubectl exec -it deployment/dokuwiki -- bash -c 'chown -R www-data:www-data /var/www/html/*'
```
