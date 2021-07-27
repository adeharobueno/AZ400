Run ansible in cloud shell of azure

```
ansible-playbook --version
```

Create a yaml to execute with ansible (rg.yml)

```yaml
   #---
    - hosts: localhost
      connection: local
      tasks:
        - name: Create resource group
          azure_rm_resourcegroup:
            name: ansible-rg
            location: eastus
           	subscription_id: 327b62c4-2ec4-4585-8e9f-bba4bf50a042
```

Run with ansible the above playbook

```
ansible-playbook rg.yml
```

previusly use the next command

```
az account list --output table
az account set --subscription 327b62c4-2ec4-4585-8e9f-bba4bf50a042
```

