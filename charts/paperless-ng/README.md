# Paperless

This is a helm chart for [Paperless-ng](https://github.com/jonaswinkler/paperless-ng). The documentation can be found [here](https://paperless-ng.readthedocs.io/en/latest/).

**This chart is not maintained by the upstream project and any issues with the chart should be raised [here](https://github.com/k8s-at-home/charts/issues/new/choose).**

## TL;DR;

```shell
$ helm repo add k8s-at-home https://k8s-at-home.com/charts/
$ helm install k8s-at-home/paperless-ng
```

## Installing the Chart

To install the chart with the release name `my-release`:

```console
helm install --name my-release k8s-at-home/paperless-ng
```

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
helm delete my-release --purge
```
The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration
The chart's [values.yaml](https://github.com/k8s-at-home/charts/blob/master/charts/paperless-ng/values.yaml) file contains a set of suggested values for a minimal deployment. Further configuration options are found in the [common library](https://github.com/k8s-at-home/charts/blob/master/charts/common/values.yaml). All configuration for the Paperless application itself is through environment variables. Please refer to the links provided in chart's [values](https://github.com/k8s-at-home/charts/blob/master/charts/paperless-ng/values.yaml) file.


Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. For example,
```console
helm install paperless \
  --set env.TZ="America/New_York" \
    k8s-at-home/paperless-ng
```
Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart. For example,
```console
helm install paperless k8s-at-home/paperless-ng --values values.yaml
```
