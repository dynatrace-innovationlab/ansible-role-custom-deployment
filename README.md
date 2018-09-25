# Ansible Role: Dynatrace Deployment

This role allows to send custom deployment information to Dynatrace.

### Usage (Example):

```yaml
dynatrace_deployment:
  tenant_url: 'https://your-tenant-url.com'
  api_token: 'your-api-token'
  attach_rules:
    tagRule: 
      meTypes: 'SERVICE'
      tags: 'ansible-deployment'
  deploymentVersion: '2.0'
  deploymentName: 'my name'
```

## Tests

Find tests and examples in the `/tests` folder.

<!--

## Run tests

Put Dynatrace module in a library folder and a `playbook` file in the parent folder.
Then start the sample `playbook` from the bash. This will automatically load the modules from the `library` folder.
Add ```-v``` or ```-vvv``` for verbose debugging output.

```
$ ansible-playbook test-deployment.yml
```

-->


