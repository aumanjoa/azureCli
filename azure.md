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

dealocate (shutdown for no pay)
```bash
az vm deallocate --name MyUbuntuVm --resource-group MYRESOURCEGROUP
```

create vsts agent in container instance
```bash
az group create --name vstsagent --location westeurope

az container create -g vstsagent --name vstsagent --image microsoft/vsts-agent:ubuntu-16.04-standard -e VSTS_ACCOUNT=joausandbox VSTS_TOKEN=vfmvlhwbeqq2ilbvinhxl5nfpb7u5a246y64i33q4nmuywmeu63q VSTS_AGENT='$(hostname)-agent' VSTS_POOL=mypool
```
