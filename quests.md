kubectl create deployment echo-web --image=gcr.io/qwiklabs-resources/echo-app:v1
kubectl expose deployment echo-web --type=LoadBalancer --port 80 --target-port 80
gcloud builds submit -t gcr.io/qwiklabs-resources/echo-app:v2 .
