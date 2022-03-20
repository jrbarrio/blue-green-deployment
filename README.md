https://kubernetes.io/blog/2018/04/30/zero-downtime-deployment-kubernetes-jenkins/

kubectl run httpbin --image=kennethreitz/httpbin --port=80 --dry-run -o yaml
kubectl port-forward pod/httpbin 8000:80

kubectl expose pod/httpbin --port --dry-run -o yaml
kubectl port-forward pod/httpbin 8000:80

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml