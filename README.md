# Helm chart myapp-chart
Helm chart for my [Golang sample app](https://github.com/tiagotele/golangsample).

## Expose repository as helm chart
```bash
$ helm package $YOUR_CHART_PATH/ # build the tgz file and copy it here
$ helm repo index . # create or update the index.yaml for repo
$ git add .
$ git commit -m 'New chart version'
```
> Thanks to [Kaveh Mousavi Zamani](https://github.com/kmzfs/helm-repo-in-github/blob/master/README.md#adding-a-new-version-or-chart-to-this-repo)

## Installing
```bash
helm3 repo add sample 'https://raw.githubusercontent.com/tiagotele/myapp-chart/master/'
helm3 search repo myapp-chart
helm3 install myapp myapp-chart
```

