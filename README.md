# Nutanix Karbon Kubernetes login command line
This project is a command line to automate login to Nutanix Karbon Kubernetes based cluster

## How to install
```console
curl -o /usr/bin/karbon-login https://raw.githubusercontent.com/mourad-hamza/nutanix-karbon-k8s-login/main/karbon-login && chmod +x /usr/bin/karbon-login
```

## Usage:
```console
Usage karbon-login -k KARBON_API_URL -c KUBERNETES_CLUSTER_NAME [ -i INSECURE | -u USERNAME | -p PASSWORD ]
      karbon-login -h

This command is to automate login to Nutanix Karbon Kubernetes based cluster
it simply gets the config file from Nutanix Prism central Karbon server for a given Kubernetes cluster and stores it in the user home directory ~/.kube/config :

Options
 -k or --karbon-api-url  : Karbon API URL, like https://IP_ADDRESS:9440 or https://FQDN:9440
 -c or --k8s-cluster     : Kubernetes cluster name in Karbon clusters list
 -i or --insecure        : Disable SSL certificat check for Prism central URL
 -u or --username        : Prism central username
 -p or --password        : Prism central password
 -h or --help            : Display this help

Notes
 This command line can be used in an interactive or non-interactive mode
 this will depend on the login and password given in the arguments
```
