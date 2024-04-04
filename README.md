# EVE-NG in Azure

## Requirements

- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli) installed
- [Pulumi](https://www.pulumi.com/docs/install/) installed
- Python available on the main system

## Deployment

The example leverages a bare bones VM Pulumi deployment to host EVE-NG. Additional setup is required to have the host VM in azure act as a jumphost to nodes in the labs.

Ensure to configure a new Pulumi secret for the VM and make any additional changes in `Pulumi.dev.yaml`.

```shell
pulumi config set --secret passwd somepass
```

Once that is complete, deploy the environment.

```shell
pulumi up -y
```

Once the VM is deployed, follow the EVE-NG GCP deployment [instructions](https://www.eve-ng.net/index.php/documentation/installation/google-cloud-install/) on the EVE-NG guide.
