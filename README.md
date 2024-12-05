
https://cloud.redhat.com/openshift/install/pull-secret

helm create helm-command

helm template command ./helm-command

helm package helm-command

az login

az login acr --name oci://<nombre-del-registro>.azurecr.io

helm push <nombre-del-paquete>.tgz oci://<nombre-del-registro>.azurecr.io/helm

helm push mi-chart-1.0.0.tgz oci://mi-registro.azurecr.io/helm



az login acr --name akzure.azurecr.io

helm push helm-command-0.1.0.tgz oci://akzure.azurecr.io/helm