# IBM Maximo Application Suite

## Maximo Application Suite 8.6 Deployment on Red Hat OpenShift Kubernetes Services (ROKS) in IBM Cloud

Este tutorial se encuentra bajo desarrollo y puede cambiar en cualquier momento.

### Pre-Requisitos
### Provision the OpenShift hardware
### Deploy Cloud Pak for Data 3.5 (CP4D) vía IBM Catalog
### Update: Catalog method is no longer available in IBM Cloud. Deploy the lite assembly manually.


## Pre-Requisitos

Los prerequisitos para la implementación de Maximo Application Suite son:

* Una instancia remota de un servidor virtual como ambiente de trabajo (preferible linux)
* Un Cluster de OpenShift en IBM Cloud
* Licencia y archivo de instalación de Maximo Application Suite
* [Visual Studio Code](https://code.visualstudio.com/docs/?dv=osx) ejecutandose localmente en tú laptop con la extensión [Microsoft's Remote SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh)
* Una cuenta de ibm cloud. Si tú no tienes un IBM ID puedes obtener uno aquí. Click en el botón Login to MY IBM y entonces click en el link Create an IBM ID.

### Ambiente de Trabajo

#### Install Command Line Interfaces

Install CLIs for IBM Cloud CLI, Helm and Openshift. Open and terminal window and type the following commands.

1. IBM Cloud CLI

```txt
curl -sL https://ibm.biz/idt-installer | bash
```

2. Helm Command line Tool

```txt
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3 && chmod 700 get_helm.sh && bash ./get_helm.sh
```

3. OpenShift Command line Tool

```txt
curl -sLo /tmp/oc.tar.gz https://mirror.openshift.com/pub/openshift-v4/x86_64/clients/oc/4.6/linux/oc.tar.gz && sudo tar xzvf /tmp/oc.tar.gz -C /usr/local/bin/ && rm -rf /tmp/oc.tar.gz
```

#### Validate Install CLIs

Validate the installed utilities: Open and terminal window and type the following commands.

1. IBM Cloud CLI

ibmcloud -v

2. Helm CLI

helm version -c

3. Kubernetes CLI

kubectl version --client=true

4. OpenShift CLI

oc version --client

5. Docker CLI

docker --help
