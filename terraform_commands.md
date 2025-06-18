**What is Terraform?**

Terraform is an infrastructure as code (IaC) tool developed by HashiCorp, which was initially open-source but recently switched to a BSL. It uses a declarative language called HashiCorp Configuration Language (HCL) to define infrastructure resources. Terraform supports a wide variety of cloud providers such as AWS, Microsoft Azure, Google Cloud, or Oracle Cloud Infrastructure, but it can also be used with Kubernetes, Helm, and many others. It is stateful, keeping track of the deployed infrastructure using a state file.


**What is Terraform CLI?**

The Terraform Command Line Interface (CLI), is a command-line tool that provides a simple way for users to interact with the infrastructure components defined in the Terraform configuration. It offers multiple commands, from initializing your terraform directory to planning, applying, and destroying infrastructure resources. With the Terraform CLI, you also have the ability to check outputs, do state-related operations, and even test different expressions.

_____________________________________________________________________________________________________________

``terraform init`` - Initializes terraform in current directory. Only once per directory is enough.

``terraform init -upgrade`` - To use the latest updated version of provider.

``terraform init -get-plugins=false`` - Initialize the working directory, do not download plugins.

``terraform init -lock=false`` - Initialize the working directory, don’t hold a state lock during backend migration.

``terraform init -input=false`` - Initialize the working directory, and disable interactive prompts.

``terraform init -migrate-state`` - Reconfigure a backend, and attempt to migrate any existing state.

``terraform init -verify-plugins=false`` - Initialize the working directory, do not verify plugins for Hashicorp signature.

``terraform init -reconfigure`` - Initialize the working directory with new state or account.

______________________________________________________________________________________________________________

``terraform get`` - Download and installs modules needed for the configuration. Note- this is usually not required as this is part of the ``terraform init`` command.

``terraform get -update`` - Check the versions of the already installed modules against the available modules and installs the newer versions if available.

``terraform validate`` - To check whether the configurations are valid in the directory and does not access any remote state or services.

``terraform validate -json`` - To see easier the number of errors and warnings that you have.

___________________________________________________________________________________________________________________

``terraform plan`` - Review the configuration and verify the resources that terraform is going to create or update. It will generate a execution plan showing you what actions will be taken without actually performing the planned actions.

``terraform plan -out=<path>`` - Save the plan file to a given path. Can then be passed to the ``terraform apply`` command.

``terraform plan -destroy`` - Create a plan to destroy all objects rather than the usual actions.

``terraform apply`` - Applies the terraform configuration and when it prompts, type 'Yes' to proceed creating or updating the resources further.

``terraform apply --auto-approve`` - Applies the terraform configuration without prompting for approval.

``terraform apply <planfilename>`` - Provide the file generated using the ``terraform plan -out`` command. If provided, Terraform will take the actions in the plan without any confirmation prompts.

``terraform apply -lock=false`` - Do not hold a state lock during the Terraform apply operation. Use with caution if other engineers might run concurrent commands against the same workspace.

``terraform apply -parallelism=<n>`` - Specify the number of operations run in parallel.

``terraform apply -var="environment=dev"`` - Pass in a variable value.

``terraform apply -var-file="varfile.tfvars"`` - Pass in variables contained in a file.

``terraform apply -target=”module.appgw.0"`` - Apply changes only to the targeted resource.

_________________________________________________________________________________________________________________________

``terraform destroy`` - Removes the resources that are created previously with the terraform configuration.

``terraform destroy -target=”module.appgw.0"`` - Destroy only the targeted resource.

``terraform destroy --auto-approve`` - Destroy the infrastructure without having to interactively type ‘yes’ to the plan. Useful in automation CI/CD pipelines.

_______________________________________________________________________________________________________________________________

``terraform refresh`` - Modify the state file with updated metadata containing information on the resources being managed in Terraform. Will not modify your infrastructure.

``terraform show`` - Show the state file in a human-readable format.

``terraform show <path to statefile>`` - If you want to read a specific state file, you can provide the path to it. If no path is provided, the current state file is shown.

``terraform state list`` - Lists out all the resources that are tracked in the current state file.

``terraform state mv`` - Move an item in the state, for example, this is useful when you need to tell Terraform that an item has been renamed. e.g. ``terraform state mv vm1.oldname vm1.newname``

``terraform state pull > state.tfstate`` - Get the current state and outputs it to a local file.

``terraform state push`` - Update remote state from the local state file.

``terraform state rm`` - Remove the specified instance from the state file. Useful when a resource has been manually deleted outside of Terraform.

``terraform state show <resourcename>`` - Show the specified resource in the state file.

___________________________________________________________________________________________________________________________________________________

``terraform -help`` - Get a list of available commands for execution with descriptions and can be used with any other subcommand to get more information.

``terraform fmt -help`` - Displays help option for the fmt command.

``terraform version`` - Show the current version of your Terraform and notifies you if there is a newer version available for download.

``terraform fmt`` - Format your Terraform configuration files using the HCL language standard.

``terraform fmt --recursive`` - Formats files inside its sub-directories as well.

``terraform fmt --diff`` - Displays differences between original configuration files and formatting changes.

_________________________________________________________________________________________________________________________________________________

``terraform workspace show`` — Show the name of the current workspace.

``terraform workspace list`` — List your workspaces.

``terraform workspace select <workspace name>`` — Select a specified workspace.

``terraform workspace new <workspace name>`` — Create a new workspace with a specified name.

``terraform workspace delete <workspace name>`` — Delete a specified workspace.

``terraform fmt --check`` - Useful in automation CI/CD pipelines, the check flag can be used to ensure the configuration files are formatted correctly, if not the exit status will be non-zero. If files are formatted correctly, the exit status will be zero.

_______________________________________________________________________________________________________________________________________________

``terraform output`` — List all the outputs currently held in your state file. These are displayed by default at the end of a terraform apply, this command can be useful if you want to view them independently.

``terraform output -state=<path to state file>`` — List the outputs held in the specified state file. -state option is ignored when the remote state is used.

``terraform output -json`` — List the outputs held in your state file in JSON format to make them machine-readable.

``terraform output vm1_public_ip`` — List a specific output held in your state file.
