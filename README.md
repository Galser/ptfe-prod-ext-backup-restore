# ptfe-prod-ext-backup-restore
PTFE Prod External Services version with snapshot/backup/restore/use snapshot

Based on two repositories: https://github.com/Galser/ptfe-prod-ext and https://github.com/Galser/ptfe-prodmount-vc-cloud-backuprestore

# Purpose

This repo contains all the code and instructions on how to install a PTFE (Prod) version with a Valid Certificate in a cloud environment in external services mode. With later making/restoration of its state from a snapshot. 

# Requirements

This repository assumes general knowledge about Terraform, if not, please get yourself accustomed first by going through [getting started guide for Terraform](https://learn.hashicorp.com/terraform?track=getting-started#getting-started). We also going to use AWS EC2 as our infrastructure provider, DNS service of CloudFlare and SSL Certificates from LetsEncrypt.

To learn more about the mentioned above tools and technologies -  please check section [Technologies near the end of the README](#technologies)


# How-to

## Prepare authentication credentials
- Beforehand, you will need to have SSH RSA key available at the default location :
 - `~/.ssh/id_rsa` and `~/.ssh/id_rsa.pub`
 > This key is going to be used later to connect to the instance where TFE will be running.
 
- Prepare AWS auth credentials (You can create security credentials on [this page](https://console.aws.amazon.com/iam/home?#security_credential).) To export them via env variables, execute in the command line :
 ```
 export AWS_ACCESS_KEY_ID="YOUR ACCESS KEY"
 export AWS_SECRET_ACCESS_KEY="YOUR SECRET KEY"
 ```
- Prepare CloudFlare authentication for your domain DNS management - register and export as env variables API keys and tokens. Follow instructions from CloudFlare here: https://support.cloudflare.com/hc/en-us/articles/200167836-Managing-API-Tokens-and-Keys
 - Export generated token and API keys :
 ```bash
 export CLOUDFLARE_API_KEY=YOUR_API_KEY_HERE
 export CLOUDFLARE_API_TOKEN=YOUR_TOKEN_HERE
 export CLOUDFLARE_ZONE_API_TOKEN=YOUR_TOKEN_HERE
 export CLOUDFLARE_DNS_API_TOKEN=YOUR_TOKEN_HERE
 ```
 
## Deploy infrastructure
- Clone this repo (*use the tools of your choice*)
- Open the folder with cloned repo
- Define your domain name in [variables.tf](variables.tf), edit on 2-nd line, following block : 
 ```terraform
 variable "site_domain" {
   default = "guselietov.com"
 }
 ```
- Define your domain site (host) record in [variables.tf](variables.tf), edit on 6-s line, following block : 
 ```terraform
 variable "site_record" {
   default = "tfe-ext-dr-1"
 }
 ```

- From inside folder with cloned repo init Terraform by executing : 
```
terraform init
```
Example output can be found here : [terraform_init.md](terraform_init.md)

- Now let's spin up everything, by executing :
```
terraform apply -auto-approve
```
Example FULL output can be found here : [terraform_apply.md](terraform_apply.md)

Execution will take some time, and at the very end of the output you should see something similar to : 
```bash
Outputs:

backend_fqdn = tfe-ext-dr-1_backend.guselietov.com
cert_url = https://acme-v02.api.letsencrypt.org/acme/cert/03f8397c0693851dbf8ead6bad4db1d3757a
db_endpoint = terraform-20191118133250830800000002.cfzxhhyh79j5.eu-central-1.rds.amazonaws.com:5432
db_name = agtfeextdr1
db_password = 9dxMvRasfasD4GS_pZ
db_user = adimini
full_site_name = tfe-ext-dr-1.guselietov.com
loadbalancer_fqdn = ag-clb-ag-clb-tfe-ext-dr-1-1298816429.eu-central-1.elb.amazonaws.com
object_storage_id = tfe-ext-dr-1-ec590f4bd918e366
public_ip = 18.184.74.49
region = eu-central-1
```
- Please note that the successful `apply` should create 3 files with SSL certificate information in local folder : 
```bash
#ls -l site_ssl_*
-rwxr-xr-x  1 andrii  staff  1944 Nov 18 14:32 site_ssl_cert.pem
-rwxr-xr-x  1 andrii  staff  3594 Nov 18 14:32 site_ssl_cert_bundle.pem
-rwxr-xr-x  1 andrii  staff  1679 Nov 18 14:32 site_ssl_private_key.pem
```

We are going to use them later. 
## Install TFE

### Terminal-based portion of TFE installation

- Connect to VM : 
```bash
ssh ubuntu@tfe-ext-dr-1_backend.guselietov.com
``` 
> Note: Use the `public_ip` or `backend_fqdn` from the previous step

- Start the PTFE install: 
```curl https://install.terraform.io/ptfe/stable | sudo bash```
 - use Public IP-address from previous steps ( `18.184.74.49` in the example ) for the service question. You can just press [Enter],
 - Reply `N` to proxy question. Again - you can just press [Enter]
 Output example : 
 ```bash
   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  133k  100  133k    0     0  30975      0  0:00:04  0:00:04 --:--:-- 30975
Determining local address
The installer will use network interface 'ens5' (with IP address '10.0.1.67')
Determining service address
The installer will use service address '18.184.74.49' (discovered from EC2 metadata service)
The installer has automatically detected the service IP address of this machine as 18.184.74.49.
Do you want to:
[0] default: use 18.184.74.49
[1] enter new address...
...

 Operator installation successful

 To continue the installation, visit the following URL in your browser:

 http://18.184.74.49:8800

 ```
This concludes the terminal install portion. let's continue in Web UI.


### Web-based portion of TFE installation

## Make snapshot

## Kill TFE - Imitating full application disaster

### Restore from a snapshot




# TODO
- [ ] update README
- [ ] make snapshot
- [ ] kill TFE
- [ ] restore TFE from snapshot
- [ ] update README for restore part

# DONE
- [x] define objectives 
- [x] create (reuse) code for infrastructure
- [x] install TFE in Prod mode with external services


# Run logs

- terraform init : [terraform_init.md](terraform_init.md)
- terraform apply (infra creation)  : [terraform_apply.md](terraform_apply.md)
- TFE destruction (full disaster imitation) : [tfe_destruction.md](tfe_destruction.md)
- terraform destroy of infra : [terraform_destroy.md](terraform_destroy.md)



# Technologies

1. **To download the content of this repository** you will need **git command-line tools**(recommended) or **Git UI Client**. To install official command-line Git tools please [find here instructions](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) for various operating systems. 

2. **For managing infrastructure** we using Terraform - open-source infrastructure as a code software tool created by HashiCorp. It enables users to define and provision a data center infrastructure using a high-level configuration language known as Hashicorp Configuration Language, or optionally JSON. More you encouraged to [learn here](https://www.terraform.io).
 - Specifically, we going to use Terraform for creating infrastructure, and install Terraform Enterprise. TFE Overview: can be found here: https://www.terraform.io/docs/enterprise/index.html
 - Pre-Install checklist: https://www.terraform.io/docs/enterprise/before-installing/index.html

3. **This project for virtualization** uses **AWS EC2** - Amazon Elastic Compute Cloud (Amazon EC2 for short) - a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. You can read in details and create a free try-out account if you don't have one here : [Amazon EC2 main page](https://aws.amazon.com/ec2/) 

4. **Cloudflare**, - is an American web infrastructure and website security company, providing content delivery network services, DDoS mitigation, Internet security, and distributed domain name server services. More information can be found here: https://www.cloudflare.com/ 

5. **Let'sEncrypt** - Let's Encrypt is a non-profit certificate authority run by Internet Security Research Group that provides X.509 certificates for Transport Layer Security encryption at no charge. The certificate is valid for 90 days, during which renewal can take place at any time. You can find out more on their [official page](https://letsencrypt.org/)
