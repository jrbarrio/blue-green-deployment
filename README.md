https://kubernetes.io/blog/2018/04/30/zero-downtime-deployment-kubernetes-jenkins/

helm install httpbin-blue service-chart -f values_blue.yaml
helm install httpbin-green service-chart -f values_green.yaml
helm install httpbin service-chart -f values.yaml