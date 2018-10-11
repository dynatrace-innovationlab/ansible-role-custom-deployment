# Ansible Role: Dynatrace Deployment

This role allows to send custom deployment information to Dynatrace.

### Usage (Example):

```yaml
- hosts: localhost
  vars:
    tenant_url: 'https://XXXXXX.live.dynatrace.com'
    api_token: 'XXXXX'


  tasks:
  - include_role:
      name: dynatrace_deployment
    vars: 
      deploymentVersion: '1.1'
      attach_rules: 
        tagRule: 
          meTypes: 'SERVICE'
          tags: 'ansible-deployment'

  - include_role:
      name: dynatrace_deployment
    vars: 
      deploymentVersion: '1.2'
      attach_rules: 
        entity_ids: 'SERVICE-ID'
```
