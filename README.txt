### github and aks authentication 

## adding service principal to github 

```
az  login 
groupId=$(az group show --name <resource-group-name> --query id --output tsv)
az ad sp create-for-rbac --scope $groupId --role Contributor --json-auth
--->> last command will generate json output which you have to save in github repo under secret section 
```
