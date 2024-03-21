# Example of usage Azure DevOps with Environments and agent installed on VMs
Several scripts that create VM, Install DevOps agent and finally promote VM to be Domain Controller.
Useful as example of usage Azure DevOps.

Please notice that in 03-InstallADDS.yaml and 99-TestDevops.yaml we are using:
```bash
tags: ${{parameters.tag}}
```

We can not use just variable like
```bash
tags: $(tag)
```

probably due to the error in Azure DevOps (MS is going to fix it).

It is fix for:
```bash
No resource were found in the environment with ID 4 matching the specified criteria: ResourceId , ResourceName , ResourceType VirtualMachine, Tags
```
