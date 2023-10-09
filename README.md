# vul-plugin-kubectl
A [Vul](https://github.com/khulnasoft-lab/vul) plugin that scans the images of a kubernetes resource

## Install

```
$ vul plugin install github.com/khulnasoft-lab/vul-plugin-kubectl
$ vul kubectl -h
Usage: vul kubectl [-h,--help] TYPE NAME [VUL OPTION]
 A Vul plugin that scans the images of a kubernetes resource.

Options:
  -h, --help    Show usage.

Examples:
  # Scan a Pod
  vul kubectl pod mypod

  # Scan a Deployment
  vul kubectl deployment mydeployment -n mynamespace

  # Scan a Job and filter by severity
  vul kubectl job myjob -n mynamespace -- --severity CRITICAL
```

## Usage
Vul's options need to be passed after `--`.

```
# Scan a Pod
$ vul kubectl pod mypod

# Scan a Deployment
$ vul kubectl deployment mydeployment -n mynamespace

# Scan a Job and filter by severity
$ vul kubectl job myjob -n mynamespace -- --severity CRITICAL
```
