## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

```

  helm repo add oip-charts https://openinnovationprogram.github.io/helm-charts/
```

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo oip-charts` to see the charts.


### Update helm repo
`helm repo update oip-charts`

then check update 
`helm search repo`


### Example ###
To install the airbyte temporal chart:

```
    helm install temporal oip-charts/temporal
```

To uninstall the chart:

```
    helm delete temporal
```



## Build & update charts 

If you want to build and update chart that are in this directory. 

1. go to chart directory
2. after updating version in Chart.yaml run `helm package .`
3. mv tgz to root 
4. run `helm repo index .`
5. push to gh-pages branch to publish the new chart version