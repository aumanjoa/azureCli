get available locations
```bash
az account list-locations
```

erstellen einer resourcegruppe
```bash
az group create --name MyResourceGroup --location westeurope
```
erstellen einer ubuntu maschine
```bash
az vm create -n MyUbuntuVm -g MyResourceGroup --image UbuntuLTS --generate-ssh-keys
```

list all resources

```bash
az resource list
```

list all vms

```bash
az vm list --output table
```