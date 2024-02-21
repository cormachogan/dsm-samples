# Data Services Manager 2.0 - Gateway API Examples
Sample YAML manifests for the API gateway on Data Services Manager 2.0 (VMware)

Two sets of examples are included, one infrastructure focused and the other data service focused.
Different personas (infra admin & dsm admin/user) determine which operations can be applied by the different persona.

Thus different kubeconfigs are required depending on whether an infrastructure operation or a DSM data service operation is being carried out.

The infrastructure admin kubeconfig can be found on the vSphere Client under vCenter Server > Configure > Data Services Manager > Infrastructure Policies.
The data service manager kubeconfig admin/user can be found on the DSM UI under the user profile drop-down.

Also note that the tokens associated with the kubeconfig regularly expire, so if you get a message similar to "error: You must be logged in to the server (Unauthorized)", you may have to download the updated kubeconfig which contains the updated token.

If you use the incorrect kubeconfig, e.g. the infra admin kubeconfig tries to create a MySQL database, it will fail with 'denied - role "INFRA_ADMIN" has no permission "C" on databases.dataservices.vmware.com/v1alpha1, Resource=mysqlclusters'. Similarly, if you try to create or modify an infrastructure policy as a DSM admin/user, it will fail with for: 'denied - role "DSM_ADMIN" has no permission "U" on infrastructure.dataservices.vmware.com/v1alpha1, Resource=infrastructurepolicies'.  Make sure you are using the correct kubeconfig, i.e. wither the Infra Admin kubeconfig from the vSphere Client or the DSM admin/user kubeconfig from the DSM UI.
