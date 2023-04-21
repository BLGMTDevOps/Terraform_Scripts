
#  **<span style="color:green">Mithun Technologies, Marathahalli ,Bengaluru.</span>**
### **<span style="color:green">Contacts: +91-9980923226, +91-8296242028<br> WebSite : <http://mithuntechnologies.co.in/></span>**
### **Email: devopstrainingblr@gmail.com, devopstrainingblr@outlook.com**



## Terraform Installation And Setup In AWS EC2 Redhat Instnace.
##### Prerequisite
+ AWS Acccount.
+ Create Redhat EC2 Instnace.
+ Create IAM Role With Required Polocies.
   + VPCFullAccess
   + EC2FullAcces
   + S3FullAccess  ..etc
+ Attach IAM Role to EC2 Instance.

### Install Terraform

``` sh
$ sudo yum install wget unzip -y
$ wget https://releases.hashicorp.com/terraform/0.12.26/terraform_0.12.26_linux_amd64.zip
$ sudo unzip terraform_0.12.26_linux_amd64.zip -d /usr/local/bin/
# Export terraform binary path temporally
$ export PATH=$PATH:/usr/local/bin
# Add path permanently for current user.By Exporting path in .bashrc file at end of file.
$ vi .bashrc
   export PATH="$PATH:/usr/local/bin"
# Source .bashrc to reflect for current session
$ source ~/.bashrc   
```
#### Clone terraform scripts
``` sh
$ git clone https://github.com/MithunTechnologiesDevOps/Terraform_Scripts.git
$ cd Terraform_Scripts
```
#### <span style="color:orange">Update Your Key Name in variables.tf file before executing terraform script.</span>
## Infrastructure As A Code
#### Create Infrastructure(VPC,Subnets,Route Tables,EC2 Instnaces ..etc) As A Code Using Terraform Scripts
``` sh
# Initialise to install plugins
$ terraform init VPC/
# Validate teffaform scripts
$ terraform validate VPC/
# Plan terraform scripts which will list resources which is going  be created.
$ terraform plan VPC/
# Apply to create resources
$ terraform apply --auto-approve VPC/
```

##  Destroy Infrastructure  
```sh
$ terraform destroy --auto-approve VPC/
```
