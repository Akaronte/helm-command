
https://cloud.redhat.com/openshift/install/pull-secret

helm create helm-command

helm template command ./helm-command

helm package helm-command

az login

az login acr --name oci://akzure.azurecr.io

helm push <nombre-del-paquete>.tgz oci://<nombre-del-registro>.azurecr.io/helm

helm push mi-chart-1.0.0.tgz oci://akzure.azurecr.io/helm


export HELM_EXPERIMENTAL_OCI=1
az login acr --name akzure.azurecr.io

helm push helm-command-0.1.0.tgz oci://akzure.azurecr.io/helm

helm repo add akzure https://akzure.azurecr.io/helm/v1/repo

helm repo add akzure oci://akzure.azurecr.io/helm/v1/repo

oci://akzure.azurecr.io/helm


az acr repository show --name $ACR_NAME --repository helm/hello-world

az acr repository show --name akzure --repository helm/helm-command


az acr manifest list-metadata --registry akzure --name helm/helm-command

helm install myhelmtest oci://akzure.azurecr.io/helm/hellm-command --version 0.1.0


oc secrets link serviceaccount/default regcred --for=pull,mount -n mytestcommand