# create github repo (name: helm-chart)

# setting github pages
source: gh-pages
path: root

# package helm file
helm package simple

# create helm index.yaml
helm repo index simple --url https://acgs771126.github.io/helm-chart/simple

# upload index.yaml and helm chart file
git add .
git commit -m 'update chart'
ggpush

# add helm repo
helm repo add andy-chart https://acgs771126.github.io/helm-chart/simple