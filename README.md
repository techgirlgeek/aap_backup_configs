# Backup AAP configs using OCP Operator for AAP

The code originated from the following blog post and has been adapted for Ansible Automation Platform (AAP) 2.6 and OpenShift Container Platform (OCP) 4.18.33: https://medium.com/@tamber/optimizing-cloud-native-operations-series-part-8-aap-configuration-as-a-code-caac-backup-2ba89c26f197

Files directory has two playbooks.

1. playbook-AAP-test.yaml - For testing as a template directly in AAP
2. playbook.yaml - To be deployed as part of the Helm chart

This code is written as a Helm chart to be applied to an OCP cluster, in the same namespace as your AAP operator.

## Prerequisites

- Helm installed on deployment host
- OCP version >= 4.18.33
- AAP operator version >= 2.6

## Deployment

### Initial deployment

The following assumes helm chart is installed in a directory called aap_backup

```bash
helm install aap-backup ./aap-backup/
```

### Make changes to deployment

```bash
helm upgrade aap-backup ./aap-backup/
```
