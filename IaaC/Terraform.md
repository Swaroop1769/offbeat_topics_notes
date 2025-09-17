terraform HCL 

terraform init
terraform plan
terraform apply
terraform destroy

resource resource_type resource name {

key = "value"
key2 = "value1"
}

terraform show  ## prints the current state of the infrastructure

or

terraform show -json ### prints in json format

${random_pet.pet_name.id} 

depends on []


terraform plan -refresh=false
terraform apply -var ----

terraform validate  ##to check if configuration is valid or not


terraform fmt ## format command it adjust the main.tf into readable format useful!!!!


terraform providers  ##to view the list of all providers

terraform providers mirror /root/terraform/new_local_file   ##mirrors the providers into new file

terraform output ## prints all the outputs
or 
terraform output name ### we can retrive a specific output value if we specify the name we need

terraform refresh ##used to refresh the terraform to sync with the real infrastructure  ###for any manual update in terraform file we can give this command


terraform graph  ###used for visual representation of dependencies and a terraform configuration or execution plan
### apt update
### apt install graphviz -y ### if we run this we can get the proper visualization

once the graphviz is installed give the below command

terraform graph | dot -Tsvg > graph.svg



Tofu validate
Tofu fmt  --> files that are changed in configuration directory are displayed

Tofu show --> prints out the current state of infra as seen by open tofu

Or 
Tofu show -json

Tofu providers
Tofu output   or tofu output <variable_name>
Tofu refresh --> is used to sync tofu with real world infra, Also, it won't modify any infra but just updates the understanding of infra by the means of state file


Tofu graph --> to create visual representation of dependencies in an open tofu configuration or an execution plan. This command can be ran as soon as config file is ready. Even b4 tofu init we can use this command
Can also be visualized graphically using graph Wiz tool.






