k -n external-services get certificateRequest -o wide
k -n external-services describe certificateRequest tls-whoami-ingress-http-1

kubectl -n external-services get certificates
kubectl -n external-services describe certificate tls-whoami-ingress-http

kubectl -n external-services get order -o wide
kubectl -n external-services describe order tls-whoami-ingress-http-1-2640678775

kubectl  -n cert-manager get pods 
kubectl -n cert-manager logs cert-manager-bbc84b684-gs4k2


k delete -f 02-whoami-ingress.yml 
k apply -f 02-whoami.yml 
k get ClusterIssuer -o wide
k describe clusterissuer letsencrypt-staging
kubectl -n whoami get certificateRequest -o wide
kubectl -n whoami describe certificateRequest tls-whoami-ingress-http-1
kubectl -n whoami describe order tls-whoami-ingress-http-1-2640678775
k get -n whoami challenges
k describe -n whoami challenge tls-whoami-ingress-http-1-2640678775-1107622269



 1952  cd github/k3s-ansible-traefik-rancher
 1953  cd test/
 1954  k delete -f 02-whoami-ingress.yml 
 1955  k apply -f 02-whoami-ingress.yml 
 1956  k delete -f 02-whoami-ingress.yml 
 1957  k apply -f 02-whoami-ingress.yml 
 1958  kubectl -n whoami get certificateRequest -o wide
 1959  kubectl -n whoami get issuer -o wide
 1960  kubectl -n whoami get certificateRequest -o wide
 1961  kubectl -n whoami describe certificateRequest tls-whoami-ingress-http-1
 1965  kubectl -n whoami get certificateRequest -o wide
 1966  kubectl -n whoami describe certificateRequest tls-whoami-ingress-http-1
 1967  kubectl -n whoami describe order whoami/tls-whoami-ingress-http-1-2640678775
 1970  kubectl -n whoami get order tls-whoami-ingress-http-1-2640678775
 1971  kubectl -n whoami get order tls-whoami-ingress-http-1-2640678775  -ojsonpath='{.status.authorizations[x].url}'
 1972  kubectl -n whoami get order tls-whoami-ingress-http-1-2640678775  -ojsonpath='{.status.authorizations[0].url}'
 1973  k get challenges
 1975  k describe challenge whoami/tls-whoami-ingress-http-1-2640678775-1107622269
 1976  k describe challenge -n whoami tls-whoami-ingress-http-1-2640678775-1107622269
 1977  k delete -f 02-whoami-ingress.yml 
 1978  k apply -f 02-whoami-ingress.yml 
 1979  k describe challenge -n whoami tls-whoami-ingress-http-1-2640678775-1107622269
 1980  k get -n whoami challenges
 1981  kubectl -n whoami get order -o wide
 1982  kubectl -n whoami get certificateRequest -o wide
 1983  k delete -f 02-whoami-ingress.yml 
 1984  cd github/k3s-ansible-traefik-rancher/test/
 1985  k delete -f 02-whoami-ingress.yml 
 1986  k apply -f 02-whoami-ingress.yml 
 1987  history