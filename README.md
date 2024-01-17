# dsm-samples
Sample YAML manifest for Data Services Manager (VMware)

Two sets of examples are included, one infrastructure focused and the other data service focused.
Different personas (infra admin/dsm admin) determine which operations can be applied by the different persona.

Thus different kubeconfigs are required depending on whether an infrastructure operation or a DSM data service operation is being carried out.

The infrastructure admin kubeconfig can be found on the vSphere Client under vCenter Server > Configure > Data Services Manager > Infrastructure Policies.
The data service manager kubeconfig admin/user can be found on the DSM UI under the user profile drop-down.
