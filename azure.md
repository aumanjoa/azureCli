get available locations
az account list-locations

erstellen einer resourcegruppe
az group create --name MyResourceGroup --location westeurope

erstellen einer ubuntu maschine

az vm create -n MyUbuntuVm -g MyResourceGroup --image UbuntuLTS --generate-ssh-keys
