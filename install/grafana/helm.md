# Using Helm Repo to install grafana

# Add helm repo 

helm repo add grafana https://grafana.github.io/helm-charts

# Update helm repo
helm repo update

# Install helm
helm install grafana grafana/grafana

#  Expose Grafana Service
kubectl expose service grafana — type=NodePort — target-port=3000 — name=grafana-ext
