# Infrastructure for VSTS Agent VM

## Deploy it

```sh
$ az group create \
  --name fhir-build-agent-rg \
  --location eastus

# Here, you'll be prompted for a VSTS PAT (personal access token)
$ az group deployment create \
  --name fhir-build-agent-deployment \
  --resource-group fhir-build-agent-rg \
  --template-file template.json \
  --parameters parameters.json
  
```

