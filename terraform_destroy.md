# Infra destroy

```bash
[0m[1mmodule.sslcert_letsencrypt.tls_private_key.private_key: Refreshing state... [id=a27a7f05abaf1e14c32e88ca3d97b6916169edce][0m
[0m[1mmodule.dns_cloudflare.data.cloudflare_zones.site_zone: Refreshing state...[0m
[0m[1mmodule.sslcert_letsencrypt.acme_registration.reg: Refreshing state... [id=https://acme-v02.api.letsencrypt.org/acme/acct/72025870][0m
[0m[1mmodule.objectstorage_aws.random_id.bucket: Refreshing state... [id=7FkPS9kY42Y][0m
[0m[1mmodule.db_aws.random_password.password: Refreshing state... [id=none][0m
[0m[1mmodule.db_aws.null_resource.timed-pw-out: Refreshing state... [id=6420129020507274029][0m
[0m[1mmodule.sslcert_letsencrypt.acme_certificate.certificate: Refreshing state... [id=https://acme-v02.api.letsencrypt.org/acme/cert/03f8397c0693851dbf8ead6bad4db1d3757a][0m
[0m[1mmodule.sslcert_letsencrypt.local_file.ssl_private_key_file: Refreshing state... [id=618f6dd031a1424b103be71d4e438f76e6efb4ea][0m
[0m[1mmodule.sslcert_letsencrypt.local_file.ssl_cert_file: Refreshing state... [id=ba64c6f4b5dad041f329602e09d47b1bdaf8d02f][0m
[0m[1mmodule.sslcert_letsencrypt.local_file.ssl_cert_bundle_file: Refreshing state... [id=4882919556e0ed69bdbe0f6ef4d38ef5ee870f05][0m
[0m[1mmodule.vpc_aws.data.aws_availability_zones.available: Refreshing state...[0m
[0m[1mmodule.sshkey_aws.aws_key_pair.sshkey: Refreshing state... [id=tfe-ext-dr-1][0m
[0m[1mmodule.vpc_aws.aws_vpc.ag_tfe: Refreshing state... [id=vpc-078b83e18678dbc8e][0m
[0m[1mmodule.objectstorage_aws.aws_s3_bucket.tfebucket: Refreshing state... [id=tfe-ext-dr-1-ec590f4bd918e366][0m
[0m[1mmodule.vpc_aws.aws_subnet.ag_tfe_Subnet: Refreshing state... [id=subnet-00fe0b043ebd95afe][0m
[0m[1mmodule.vpc_aws.aws_subnet.rds[0]: Refreshing state... [id=subnet-0b33618b0758403b9][0m
[0m[1mmodule.vpc_aws.aws_subnet.rds[2]: Refreshing state... [id=subnet-0b7becf732702638d][0m
[0m[1mmodule.vpc_aws.aws_subnet.rds[1]: Refreshing state... [id=subnet-0d03df45737943a7b][0m
[0m[1mmodule.vpc_aws.aws_security_group.ag_tfe_Security_Group_elb: Refreshing state... [id=sg-05116856615e4a32f][0m
[0m[1mmodule.vpc_aws.aws_route_table.ag_tfe_route_table: Refreshing state... [id=rtb-00ef6db6e42a25112][0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Refreshing state... [id=igw-0a50f3779bbb0ed48][0m
[0m[1mmodule.vpc_aws.aws_security_group.ag_tfe_Security_Group_db: Refreshing state... [id=sg-09bd7b30129de4964][0m
[0m[1mmodule.vpc_aws.aws_security_group.ag_tfe_Security_Group: Refreshing state... [id=sg-0a1b2ba13f83f6ba1][0m
[0m[1mmodule.vpc_aws.aws_route_table_association.ag_tfe_association: Refreshing state... [id=rtbassoc-017444ee20aa74572][0m
[0m[1mmodule.vpc_aws.aws_route.ag_tfe_internet_access: Refreshing state... [id=r-rtb-00ef6db6e42a251121080289494][0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Refreshing state... [id=i-095d6319db47efab8][0m
[0m[1mmodule.db_aws.aws_db_subnet_group.tfe: Refreshing state... [id=agtfeextdr1-rds-subnet-group][0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Refreshing state... [id=terraform-20191118133250830800000002][0m
[0m[1mmodule.bootstrap_pg_rds_aws.null_resource.pg-rds-bootstrap: Refreshing state... [id=8289507824799680102][0m
[0m[1mmodule.dns_cloudflare.cloudflare_record.site_backend: Refreshing state... [id=c0a89c909d2ac1f904c9dc0087259109][0m
[0m[1mmodule.lb_aws.aws_elb.ptfe_lb: Refreshing state... [id=ag-clb-ag-clb-tfe-ext-dr-1][0m
[0m[1mmodule.dns_cloudflare.cloudflare_record.site_lb: Refreshing state... [id=94128084dbc97da7cc4d80bf40d7f8ed][0m

An execution plan has been generated and is shown below.
Resource actions are indicated with the following symbols:
  [31m-[0m destroy
[0m
Terraform will perform the following actions:

[1m  # module.bootstrap_pg_rds_aws.null_resource.pg-rds-bootstrap[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "null_resource" "pg-rds-bootstrap" {
      [31m-[0m [0m[1m[0mid[0m[0m       = "8289507824799680102" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtriggers[0m[0m = {
          [31m-[0m [0m"rds" = "terraform-20191118133250830800000002"
        } [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.compute_aws.aws_instance.ptfe[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_instance" "ptfe" {
      [31m-[0m [0m[1m[0mami[0m[0m                          = "ami-08a162fe1419adb2a" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0marn[0m[0m                          = "arn:aws:ec2:eu-central-1:729476260648:instance/i-095d6319db47efab8" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0massociate_public_ip_address[0m[0m  = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mavailability_zone[0m[0m            = "eu-central-1a" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mcpu_core_count[0m[0m               = 1 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mcpu_threads_per_core[0m[0m         = 2 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdisable_api_termination[0m[0m      = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mebs_optimized[0m[0m                = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mget_password_data[0m[0m            = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                           = "i-095d6319db47efab8" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0minstance_state[0m[0m               = "running" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0minstance_type[0m[0m                = "m5.large" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mipv6_address_count[0m[0m           = 0 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mipv6_addresses[0m[0m               = [] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mkey_name[0m[0m                     = "tfe-ext-dr-1" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmonitoring[0m[0m                   = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mprimary_network_interface_id[0m[0m = "eni-074add191abe7aed4" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mprivate_dns[0m[0m                  = "ip-10-0-1-67.eu-central-1.compute.internal" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mprivate_ip[0m[0m                   = "10.0.1.67" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mpublic_dns[0m[0m                   = "ec2-18-184-74-49.eu-central-1.compute.amazonaws.com" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mpublic_ip[0m[0m                    = "18.184.74.49" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msecurity_groups[0m[0m              = [] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msource_dest_check[0m[0m            = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msubnet_id[0m[0m                    = "subnet-00fe0b043ebd95afe" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m                         = {
          [31m-[0m [0m"Name"      = "ag-tfe-ext-dr-1-andrii"
          [31m-[0m [0m"andriitag" = "true"
        } [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtenancy[0m[0m                      = "default" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvolume_tags[0m[0m                  = {
          [31m-[0m [0m"Name"      = "ag-tfe-ext-dr-1-andrii"
          [31m-[0m [0m"andriitag" = "true"
        } [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvpc_security_group_ids[0m[0m       = [
          [31m-[0m [0m"sg-0a1b2ba13f83f6ba1",
        ] [90m->[0m [0m[90mnull[0m[0m

      [31m-[0m [0mroot_block_device {
          [31m-[0m [0m[1m[0mdelete_on_termination[0m[0m = true [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mencrypted[0m[0m             = false [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0miops[0m[0m                  = 150 [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mvolume_id[0m[0m             = "vol-0a57f874a9e4b2aca" [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mvolume_size[0m[0m           = 50 [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mvolume_type[0m[0m           = "gp2" [90m->[0m [0m[90mnull[0m[0m
        }
    }

[1m  # module.db_aws.aws_db_instance.tfe_db[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_db_instance" "tfe_db" {
      [31m-[0m [0m[1m[0maddress[0m[0m                               = "terraform-20191118133250830800000002.cfzxhhyh79j5.eu-central-1.rds.amazonaws.com" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mallocated_storage[0m[0m                     = 50 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0marn[0m[0m                                   = "arn:aws:rds:eu-central-1:729476260648:db:terraform-20191118133250830800000002" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mauto_minor_version_upgrade[0m[0m            = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mavailability_zone[0m[0m                     = "eu-central-1a" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mbackup_retention_period[0m[0m               = 0 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mbackup_window[0m[0m                         = "23:29-23:59" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mca_cert_identifier[0m[0m                    = "rds-ca-2015" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mcopy_tags_to_snapshot[0m[0m                 = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdb_subnet_group_name[0m[0m                  = "agtfeextdr1-rds-subnet-group" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdeletion_protection[0m[0m                   = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0menabled_cloudwatch_logs_exports[0m[0m       = [] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mendpoint[0m[0m                              = "terraform-20191118133250830800000002.cfzxhhyh79j5.eu-central-1.rds.amazonaws.com:5432" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mengine[0m[0m                                = "postgres" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mengine_version[0m[0m                        = "9.6.15" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mfinal_snapshot_identifier[0m[0m             = "agtfeextdr1-final-snap" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mhosted_zone_id[0m[0m                        = "Z1RLNUO7B9Q6NB" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0miam_database_authentication_enabled[0m[0m   = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                                    = "terraform-20191118133250830800000002" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0midentifier[0m[0m                            = "terraform-20191118133250830800000002" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0minstance_class[0m[0m                        = "db.m4.large" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0miops[0m[0m                                  = 0 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mlicense_model[0m[0m                         = "postgresql-license" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmaintenance_window[0m[0m                    = "tue:02:12-tue:02:42" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmax_allocated_storage[0m[0m                 = 0 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmonitoring_interval[0m[0m                   = 0 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmulti_az[0m[0m                              = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mname[0m[0m                                  = "agtfeextdr1" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0moption_group_name[0m[0m                     = "default:postgres-9-6" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mparameter_group_name[0m[0m                  = "default.postgres9.6" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mpassword[0m[0m                              = (sensitive value)
      [31m-[0m [0m[1m[0mperformance_insights_enabled[0m[0m          = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mperformance_insights_retention_period[0m[0m = 0 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mport[0m[0m                                  = 5432 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mpublicly_accessible[0m[0m                   = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mreplicas[0m[0m                              = [] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mresource_id[0m[0m                           = "db-JASZN6334F2GJ3N4DOUUITKSH4" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msecurity_group_names[0m[0m                  = [] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mskip_final_snapshot[0m[0m                   = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mstatus[0m[0m                                = "available" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mstorage_encrypted[0m[0m                     = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mstorage_type[0m[0m                          = "gp2" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m                                  = {
          [31m-[0m [0m"Name"      = "ag-tfe-ext-dr-1"
          [31m-[0m [0m"andriitag" = "true"
        } [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0musername[0m[0m                              = "adimini" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvpc_security_group_ids[0m[0m                = [
          [31m-[0m [0m"sg-09bd7b30129de4964",
        ] [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.db_aws.aws_db_subnet_group.tfe[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_db_subnet_group" "tfe" {
      [31m-[0m [0m[1m[0marn[0m[0m         = "arn:aws:rds:eu-central-1:729476260648:subgrp:agtfeextdr1-rds-subnet-group" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdescription[0m[0m = "Terraform RDS subnet group" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m          = "agtfeextdr1-rds-subnet-group" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mname[0m[0m        = "agtfeextdr1-rds-subnet-group" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msubnet_ids[0m[0m  = [
          [31m-[0m [0m"subnet-0b33618b0758403b9",
          [31m-[0m [0m"subnet-0b7becf732702638d",
          [31m-[0m [0m"subnet-0d03df45737943a7b",
        ] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m        = {
          [31m-[0m [0m"Name"      = "ag-tfe-ext-dr-1"
          [31m-[0m [0m"andriitag" = "true"
        } [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.db_aws.null_resource.timed-pw-out[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "null_resource" "timed-pw-out" {
      [31m-[0m [0m[1m[0mid[0m[0m       = "6420129020507274029" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtriggers[0m[0m = {
          [31m-[0m [0m"timey" = "2019-11-18T13:32:44Z"
        } [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.db_aws.random_password.password[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "random_password" "password" {
      [31m-[0m [0m[1m[0mid[0m[0m               = "none" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mlength[0m[0m           = 16 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mlower[0m[0m            = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmin_lower[0m[0m        = 0 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmin_numeric[0m[0m      = 0 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmin_special[0m[0m      = 0 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmin_upper[0m[0m        = 0 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mnumber[0m[0m           = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0moverride_special[0m[0m = "_-" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mresult[0m[0m           = (sensitive value)
      [31m-[0m [0m[1m[0mspecial[0m[0m          = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mupper[0m[0m            = true [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.dns_cloudflare.cloudflare_record.site_backend[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "cloudflare_record" "site_backend" {
      [31m-[0m [0m[1m[0mcreated_on[0m[0m  = "2019-11-18T13:33:36.657802Z" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdata[0m[0m        = {} [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mhostname[0m[0m    = "tfe-ext-dr-1_backend.guselietov.com" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m          = "c0a89c909d2ac1f904c9dc0087259109" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmetadata[0m[0m    = {
          [31m-[0m [0m"auto_added"             = "false"
          [31m-[0m [0m"managed_by_apps"        = "false"
          [31m-[0m [0m"managed_by_argo_tunnel" = "false"
        } [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmodified_on[0m[0m = "2019-11-18T13:33:36.657802Z" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mname[0m[0m        = "tfe-ext-dr-1_backend" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mpriority[0m[0m    = 0 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mproxiable[0m[0m   = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mproxied[0m[0m     = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mttl[0m[0m         = 600 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtype[0m[0m        = "A" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvalue[0m[0m       = "18.184.74.49" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mzone_id[0m[0m     = "2032750a75777e59b3bf6c73333ee2b0" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.dns_cloudflare.cloudflare_record.site_lb[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "cloudflare_record" "site_lb" {
      [31m-[0m [0m[1m[0mcreated_on[0m[0m  = "2019-11-18T13:33:39.739715Z" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdata[0m[0m        = {} [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mhostname[0m[0m    = "tfe-ext-dr-1.guselietov.com" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m          = "94128084dbc97da7cc4d80bf40d7f8ed" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmetadata[0m[0m    = {
          [31m-[0m [0m"auto_added"             = "false"
          [31m-[0m [0m"managed_by_apps"        = "false"
          [31m-[0m [0m"managed_by_argo_tunnel" = "false"
        } [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmodified_on[0m[0m = "2019-11-18T13:33:39.739715Z" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mname[0m[0m        = "tfe-ext-dr-1" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mpriority[0m[0m    = 0 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mproxiable[0m[0m   = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mproxied[0m[0m     = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mttl[0m[0m         = 600 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtype[0m[0m        = "CNAME" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvalue[0m[0m       = "ag-clb-ag-clb-tfe-ext-dr-1-1298816429.eu-central-1.elb.amazonaws.com" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mzone_id[0m[0m     = "2032750a75777e59b3bf6c73333ee2b0" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.lb_aws.aws_elb.ptfe_lb[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_elb" "ptfe_lb" {
      [31m-[0m [0m[1m[0marn[0m[0m                         = "arn:aws:elasticloadbalancing:eu-central-1:729476260648:loadbalancer/ag-clb-ag-clb-tfe-ext-dr-1" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mavailability_zones[0m[0m          = [
          [31m-[0m [0m"eu-central-1a",
        ] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mconnection_draining[0m[0m         = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mconnection_draining_timeout[0m[0m = 400 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mcross_zone_load_balancing[0m[0m   = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdns_name[0m[0m                    = "ag-clb-ag-clb-tfe-ext-dr-1-1298816429.eu-central-1.elb.amazonaws.com" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                          = "ag-clb-ag-clb-tfe-ext-dr-1" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0midle_timeout[0m[0m                = 400 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0minstances[0m[0m                   = [
          [31m-[0m [0m"i-095d6319db47efab8",
        ] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0minternal[0m[0m                    = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mname[0m[0m                        = "ag-clb-ag-clb-tfe-ext-dr-1" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msecurity_groups[0m[0m             = [
          [31m-[0m [0m"sg-05116856615e4a32f",
        ] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msource_security_group[0m[0m       = "729476260648/ag_ptfe_pm-sg-elb" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msource_security_group_id[0m[0m    = "sg-05116856615e4a32f" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msubnets[0m[0m                     = [
          [31m-[0m [0m"subnet-00fe0b043ebd95afe",
        ] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m                        = {
          [31m-[0m [0m"Name"      = "ag-clb-tfe-ext-dr-1"
          [31m-[0m [0m"andriitag" = "true"
        } [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mzone_id[0m[0m                     = "Z215JYRZR1TBD5" [90m->[0m [0m[90mnull[0m[0m

      [31m-[0m [0mhealth_check {
          [31m-[0m [0m[1m[0mhealthy_threshold[0m[0m   = 3 [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0minterval[0m[0m            = 30 [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mtarget[0m[0m              = "TCP:8800" [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mtimeout[0m[0m             = 10 [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0munhealthy_threshold[0m[0m = 10 [90m->[0m [0m[90mnull[0m[0m
        }

      [31m-[0m [0mlistener {
          [31m-[0m [0m[1m[0minstance_port[0m[0m     = 443 [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0minstance_protocol[0m[0m = "tcp" [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mlb_port[0m[0m           = 443 [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mlb_protocol[0m[0m       = "tcp" [90m->[0m [0m[90mnull[0m[0m
        }
      [31m-[0m [0mlistener {
          [31m-[0m [0m[1m[0minstance_port[0m[0m     = 8800 [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0minstance_protocol[0m[0m = "tcp" [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mlb_port[0m[0m           = 8800 [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mlb_protocol[0m[0m       = "tcp" [90m->[0m [0m[90mnull[0m[0m
        }
    }

[1m  # module.objectstorage_aws.aws_s3_bucket.tfebucket[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_s3_bucket" "tfebucket" {
      [31m-[0m [0m[1m[0macl[0m[0m                         = "private" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0marn[0m[0m                         = "arn:aws:s3:::tfe-ext-dr-1-ec590f4bd918e366" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mbucket[0m[0m                      = "tfe-ext-dr-1-ec590f4bd918e366" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mbucket_domain_name[0m[0m          = "tfe-ext-dr-1-ec590f4bd918e366.s3.amazonaws.com" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mbucket_regional_domain_name[0m[0m = "tfe-ext-dr-1-ec590f4bd918e366.s3.eu-central-1.amazonaws.com" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mforce_destroy[0m[0m               = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mhosted_zone_id[0m[0m              = "Z21DNDUVLTQW6Q" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                          = "tfe-ext-dr-1-ec590f4bd918e366" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mregion[0m[0m                      = "eu-central-1" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mrequest_payer[0m[0m               = "BucketOwner" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m                        = {
          [31m-[0m [0m"Name"      = "tfe-ext-dr-1"
          [31m-[0m [0m"andriitag" = "true"
        } [90m->[0m [0m[90mnull[0m[0m

      [31m-[0m [0mlifecycle_rule {
          [31m-[0m [0m[1m[0mabort_incomplete_multipart_upload_days[0m[0m = 0 [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0menabled[0m[0m                                = true [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mid[0m[0m                                     = "tf-s3-lifecycle-20191118133248365500000001" [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mtags[0m[0m                                   = {} [90m->[0m [0m[90mnull[0m[0m

          [31m-[0m [0mtransition {
              [31m-[0m [0m[1m[0mdays[0m[0m          = 30 [90m->[0m [0m[90mnull[0m[0m
              [31m-[0m [0m[1m[0mstorage_class[0m[0m = "STANDARD_IA" [90m->[0m [0m[90mnull[0m[0m
            }
          [31m-[0m [0mtransition {
              [31m-[0m [0m[1m[0mdays[0m[0m          = 60 [90m->[0m [0m[90mnull[0m[0m
              [31m-[0m [0m[1m[0mstorage_class[0m[0m = "GLACIER" [90m->[0m [0m[90mnull[0m[0m
            }
        }

      [31m-[0m [0mversioning {
          [31m-[0m [0m[1m[0menabled[0m[0m    = true [90m->[0m [0m[90mnull[0m[0m
          [31m-[0m [0m[1m[0mmfa_delete[0m[0m = false [90m->[0m [0m[90mnull[0m[0m
        }
    }

[1m  # module.objectstorage_aws.random_id.bucket[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "random_id" "bucket" {
      [31m-[0m [0m[1m[0mb64[0m[0m         = "7FkPS9kY42Y" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mb64_std[0m[0m     = "7FkPS9kY42Y=" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mb64_url[0m[0m     = "7FkPS9kY42Y" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mbyte_length[0m[0m = 8 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdec[0m[0m         = "17030660284317492070" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mhex[0m[0m         = "ec590f4bd918e366" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m          = "7FkPS9kY42Y" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mkeepers[0m[0m     = {
          [31m-[0m [0m"ami_id" = "tfe-ext-dr-1"
        } [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.sshkey_aws.aws_key_pair.sshkey[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_key_pair" "sshkey" {
      [31m-[0m [0m[1m[0mfingerprint[0m[0m = "01:ca:46:0b:ea:ba:4e:28:0e:c9:b4:9e:2d:f3:29:66" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m          = "tfe-ext-dr-1" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mkey_name[0m[0m    = "tfe-ext-dr-1" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mpublic_key[0m[0m  = "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC704xhVAxg9Bhq0jIbABWVjKl2DW7apvfFj3UtvActT9a9w1Xt5Fa2jEFuzMXceFtpDjgq5j8E8vsrICu8Wpeqwuo2SR2aAjEjBDfJzOM3kmF9wuWdpacDhVm1luPJiqqM4wLAPufht5vhdlqD8QtW/q84MMHbbkXNjdvgqsIcvDWcCRLQDa1Du3ElF9V+/n182ihIDfQCUtQS0zc9lIcUemZMSLRhxAWA9BZYCu8wnUuLBE/fv8apC0NxOayklSBEj7Pk/HxJnYxTeskqGs5MkzHydObPZSnAtX4Hfe1KlmsAVwt6Sj2bG2AYpt9G0jF7Oq9sYQ6nBTMAxENIsmhB andrii@guselietovs-mbp.home" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.sslcert_letsencrypt.acme_certificate.certificate[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "acme_certificate" "certificate" {
      [31m-[0m [0m[1m[0maccount_key_pem[0m[0m    = (sensitive value)
      [31m-[0m [0m[1m[0mcertificate_domain[0m[0m = "tfe-ext-dr-1.guselietov.com" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mcertificate_p12[0m[0m    = (sensitive value)
      [31m-[0m [0m[1m[0mcertificate_pem[0m[0m    = "-----BEGIN CERTIFICATE-----\nMIIFbjCCBFagAwIBAgISA/g5fAaThR2/jq1rrU2x03V6MA0GCSqGSIb3DQEBCwUA\nMEoxCzAJBgNVBAYTAlVTMRYwFAYDVQQKEw1MZXQncyBFbmNyeXB0MSMwIQYDVQQD\nExpMZXQncyBFbmNyeXB0IEF1dGhvcml0eSBYMzAeFw0xOTExMTgxMjMyNThaFw0y\nMDAyMTYxMjMyNThaMCYxJDAiBgNVBAMTG3RmZS1leHQtZHItMS5ndXNlbGlldG92\nLmNvbTCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEBAJIRBkKPPcUT3hLT\nqnPBeUJxB0ID/vmN788wGkwLAXqLJOo5yaz72wvpP/8e2F3FisVVuA6fMd3/b2EX\n0KUQ0jSiQoQtEyorHLEfdfr/H+y+yFKf67amZLKES1BQvrmcb9frjbiiQDz4W5uk\nCWPEUkBQVdZlYKvgGSVSym8sHFwlJ7CFuHfaRtPVM0ZhLtofeMPHptD01Kcf+OaQ\nQHLgCYpbTjW7uX++dJkqe2NJjF8+jlcoqpcO70PnZ9H8cUCS8+RpUWa3tORR20Kw\nZ1pwiu8L74G/z7yCdWyMnKIWYshNbnkgwt3LiZR2ve55wGd40GZe9mqjmh20+ts0\np9/Z0XMCAwEAAaOCAnAwggJsMA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggr\nBgEFBQcDAQYIKwYBBQUHAwIwDAYDVR0TAQH/BAIwADAdBgNVHQ4EFgQUUXwT/JfF\nHJUD3LVOzqelX+Ls4SIwHwYDVR0jBBgwFoAUqEpqYwR93brm0Tm3pkVl7/Oo7KEw\nbwYIKwYBBQUHAQEEYzBhMC4GCCsGAQUFBzABhiJodHRwOi8vb2NzcC5pbnQteDMu\nbGV0c2VuY3J5cHQub3JnMC8GCCsGAQUFBzAChiNodHRwOi8vY2VydC5pbnQteDMu\nbGV0c2VuY3J5cHQub3JnLzAmBgNVHREEHzAdght0ZmUtZXh0LWRyLTEuZ3VzZWxp\nZXRvdi5jb20wTAYDVR0gBEUwQzAIBgZngQwBAgEwNwYLKwYBBAGC3xMBAQEwKDAm\nBggrBgEFBQcCARYaaHR0cDovL2Nwcy5sZXRzZW5jcnlwdC5vcmcwggEEBgorBgEE\nAdZ5AgQCBIH1BIHyAPAAdgBep3P531bA57U2SH3QSeAyepGaDIShEhKEGHWWgXFF\nWAAAAW5+t2arAAAEAwBHMEUCIFMQHqWcFQ3gfKF4ZrRw5pWnnACtpcqo++6suzDS\nL2s3AiEAmtXMYyjKwPdXAsjJKBZXd1FJvmgMl57tMURLbImyczQAdgAHt1wb5X1o\n//Gwxh0jFce65ld8V5S3au68YToaadOiHAAAAW5+t2b7AAAEAwBHMEUCIAGJWqv+\nct3DTE14/xLPUqpk6T4zPqxQ2JGo7pKsYAt2AiEAu3MKOV0A96TFc5B4+rAQnIo7\nVDCDCwNKgjj87vnR7tkwDQYJKoZIhvcNAQELBQADggEBAIHS/HYh2QC1NEFtTy9K\nElVAOi08jD4nFygA1SgTVosdT8o4pRbNrFjCWCzppnA7XnYJqgQ1ZkVoEyddrRr7\n7o8wkvS4J9tz3HBZKN+SUajcT9c/VN4AgP6+Ma7KLZgHRkR9uiTz5Q0K7AVgeqP6\nElTvbiWCHQrkRiCMWoL72qvATTNknvPG0Z+vgOuQMDMdkFyX5UyWM0L5CtEMpduJ\nnQ3HoxpZpN2lrpkUkw6Ri58rvV7O/WYnzhiXXJY+2teB39UDEgoan7Cd1s3o6XNv\nwswL8khMnBJGNts7fD2hLQmC6QX/zxZyFDNW+pb313pWcDJg+H9kIN1PIJ4VvJFL\nNig=\n-----END CERTIFICATE-----\n" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mcertificate_url[0m[0m    = "https://acme-v02.api.letsencrypt.org/acme/cert/03f8397c0693851dbf8ead6bad4db1d3757a" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mcommon_name[0m[0m        = "tfe-ext-dr-1.guselietov.com" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                 = "https://acme-v02.api.letsencrypt.org/acme/cert/03f8397c0693851dbf8ead6bad4db1d3757a" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0missuer_pem[0m[0m         = "-----BEGIN CERTIFICATE-----\nMIIEkjCCA3qgAwIBAgIQCgFBQgAAAVOFc2oLheynCDANBgkqhkiG9w0BAQsFADA/\nMSQwIgYDVQQKExtEaWdpdGFsIFNpZ25hdHVyZSBUcnVzdCBDby4xFzAVBgNVBAMT\nDkRTVCBSb290IENBIFgzMB4XDTE2MDMxNzE2NDA0NloXDTIxMDMxNzE2NDA0Nlow\nSjELMAkGA1UEBhMCVVMxFjAUBgNVBAoTDUxldCdzIEVuY3J5cHQxIzAhBgNVBAMT\nGkxldCdzIEVuY3J5cHQgQXV0aG9yaXR5IFgzMIIBIjANBgkqhkiG9w0BAQEFAAOC\nAQ8AMIIBCgKCAQEAnNMM8FrlLke3cl03g7NoYzDq1zUmGSXhvb418XCSL7e4S0EF\nq6meNQhY7LEqxGiHC6PjdeTm86dicbp5gWAf15Gan/PQeGdxyGkOlZHP/uaZ6WA8\nSMx+yk13EiSdRxta67nsHjcAHJyse6cF6s5K671B5TaYucv9bTyWaN8jKkKQDIZ0\nZ8h/pZq4UmEUEz9l6YKHy9v6Dlb2honzhT+Xhq+w3Brvaw2VFn3EK6BlspkENnWA\na6xK8xuQSXgvopZPKiAlKQTGdMDQMc2PMTiVFrqoM7hD8bEfwzB/onkxEz0tNvjj\n/PIzark5McWvxI0NHWQWM6r6hCm21AvA2H3DkwIDAQABo4IBfTCCAXkwEgYDVR0T\nAQH/BAgwBgEB/wIBADAOBgNVHQ8BAf8EBAMCAYYwfwYIKwYBBQUHAQEEczBxMDIG\nCCsGAQUFBzABhiZodHRwOi8vaXNyZy50cnVzdGlkLm9jc3AuaWRlbnRydXN0LmNv\nbTA7BggrBgEFBQcwAoYvaHR0cDovL2FwcHMuaWRlbnRydXN0LmNvbS9yb290cy9k\nc3Ryb290Y2F4My5wN2MwHwYDVR0jBBgwFoAUxKexpHsscfrb4UuQdf/EFWCFiRAw\nVAYDVR0gBE0wSzAIBgZngQwBAgEwPwYLKwYBBAGC3xMBAQEwMDAuBggrBgEFBQcC\nARYiaHR0cDovL2Nwcy5yb290LXgxLmxldHNlbmNyeXB0Lm9yZzA8BgNVHR8ENTAz\nMDGgL6AthitodHRwOi8vY3JsLmlkZW50cnVzdC5jb20vRFNUUk9PVENBWDNDUkwu\nY3JsMB0GA1UdDgQWBBSoSmpjBH3duubRObemRWXv86jsoTANBgkqhkiG9w0BAQsF\nAAOCAQEA3TPXEfNjWDjdGBX7CVW+dla5cEilaUcne8IkCJLxWh9KEik3JHRRHGJo\nuM2VcGfl96S8TihRzZvoroed6ti6WqEBmtzw3Wodatg+VyOeph4EYpr/1wXKtx8/\nwApIvJSwtmVi4MFU5aMqrSDE6ea73Mj2tcMyo5jMd6jmeWUHK8so/joWUoHOUgwu\nX4Po1QYz+3dszkDqMp4fklxBwXRsW10KXzPMTZ+sOPAveyxindmjkW8lGy+QsRlG\nPfZ+G6Z6h7mjem0Y+iWlkYcV4PIWL1iwBi8saCbGS5jN2p8M+X+Q7UNKEkROb3N6\nKOqkqm57TH2H3eDJAkSnh6/DNFu0Qg==\n-----END CERTIFICATE-----\n" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mkey_type[0m[0m           = "2048" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmin_days_remaining[0m[0m = 30 [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmust_staple[0m[0m        = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mprivate_key_pem[0m[0m    = (sensitive value)

      [31m-[0m [0mdns_challenge {
          [31m-[0m [0m[1m[0mconfig[0m[0m   = (sensitive value)
          [31m-[0m [0m[1m[0mprovider[0m[0m = "cloudflare" [90m->[0m [0m[90mnull[0m[0m
        }
    }

[1m  # module.sslcert_letsencrypt.acme_registration.reg[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "acme_registration" "reg" {
      [31m-[0m [0m[1m[0maccount_key_pem[0m[0m  = (sensitive value)
      [31m-[0m [0m[1m[0memail_address[0m[0m    = "andrii@guselietov.com" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m               = "https://acme-v02.api.letsencrypt.org/acme/acct/72025870" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mregistration_url[0m[0m = "https://acme-v02.api.letsencrypt.org/acme/acct/72025870" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.sslcert_letsencrypt.local_file.ssl_cert_bundle_file[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "local_file" "ssl_cert_bundle_file" {
      [31m-[0m [0m[1m[0mdirectory_permission[0m[0m = "0777" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mfile_permission[0m[0m      = "0777" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mfilename[0m[0m             = "./site_ssl_cert_bundle.pem" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                   = "4882919556e0ed69bdbe0f6ef4d38ef5ee870f05" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msensitive_content[0m[0m    = (sensitive value)
    }

[1m  # module.sslcert_letsencrypt.local_file.ssl_cert_file[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "local_file" "ssl_cert_file" {
      [31m-[0m [0m[1m[0mdirectory_permission[0m[0m = "0777" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mfile_permission[0m[0m      = "0777" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mfilename[0m[0m             = "./site_ssl_cert.pem" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                   = "ba64c6f4b5dad041f329602e09d47b1bdaf8d02f" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msensitive_content[0m[0m    = (sensitive value)
    }

[1m  # module.sslcert_letsencrypt.local_file.ssl_private_key_file[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "local_file" "ssl_private_key_file" {
      [31m-[0m [0m[1m[0mdirectory_permission[0m[0m = "0777" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mfile_permission[0m[0m      = "0777" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mfilename[0m[0m             = "./site_ssl_private_key.pem" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                   = "618f6dd031a1424b103be71d4e438f76e6efb4ea" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msensitive_content[0m[0m    = (sensitive value)
    }

[1m  # module.sslcert_letsencrypt.tls_private_key.private_key[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "tls_private_key" "private_key" {
      [31m-[0m [0m[1m[0malgorithm[0m[0m                  = "RSA" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mecdsa_curve[0m[0m                = "P224" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                         = "a27a7f05abaf1e14c32e88ca3d97b6916169edce" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mprivate_key_pem[0m[0m            = (sensitive value)
      [31m-[0m [0m[1m[0mpublic_key_fingerprint_md5[0m[0m = "a6:fd:52:d7:68:5d:f6:cf:38:8c:ff:91:39:6b:6f:f2" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mpublic_key_openssh[0m[0m         = "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDlmMjgFbsyrkniwsOfZcpTuq93hP6H5k8gDqcS4pi+78xinf3wTRZzR3zhG7iY7PAqs3o+EPO6Z1fFFhCnyL1+zsmz9E36qOU/qE3IVwAm3rpVMAavKp1EaMoax2c7a51L1WTYTk29+uXrOC5rS/y3XaMh0FiQPxW3XuRMsYqOcBPNuBxg23CAys3ek5R5Vn4vR9LVEInPFOcsrK77RyOsH5JMOeq9ytjcAz3ES9W/auIl3UEMyGezrcPU6C9j9lzQb7wUrx2EF10n89o8yyAUB+vg3z3VozfFXlu7QC3gLSCKnsNvFkPBhGDXbvTcfmIQX1ZMz7gNSYkBvcoHh86z\n" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mpublic_key_pem[0m[0m             = "-----BEGIN PUBLIC KEY-----\nMIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA5ZjI4BW7Mq5J4sLDn2XK\nU7qvd4T+h+ZPIA6nEuKYvu/MYp398E0Wc0d84Ru4mOzwKrN6PhDzumdXxRYQp8i9\nfs7Js/RN+qjlP6hNyFcAJt66VTAGryqdRGjKGsdnO2udS9Vk2E5Nvfrl6zgua0v8\nt12jIdBYkD8Vt17kTLGKjnATzbgcYNtwgMrN3pOUeVZ+L0fS1RCJzxTnLKyu+0cj\nrB+STDnqvcrY3AM9xEvVv2riJd1BDMhns63D1OgvY/Zc0G+8FK8dhBddJ/PaPMsg\nFAfr4N891aM3xV5bu0At4C0gip7DbxZDwYRg12703H5iEF9WTM+4DUmJAb3KB4fO\nswIDAQAB\n-----END PUBLIC KEY-----\n" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mrsa_bits[0m[0m                   = 2048 [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.vpc_aws.aws_internet_gateway.ag_tfe_GW[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_internet_gateway" "ag_tfe_GW" {
      [31m-[0m [0m[1m[0mid[0m[0m       = "igw-0a50f3779bbb0ed48" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mowner_id[0m[0m = "729476260648" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m     = {
          [31m-[0m [0m"Name" = "ag_ptfe_pm_internet_gateway"
        } [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvpc_id[0m[0m   = "vpc-078b83e18678dbc8e" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.vpc_aws.aws_route.ag_tfe_internet_access[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_route" "ag_tfe_internet_access" {
      [31m-[0m [0m[1m[0mdestination_cidr_block[0m[0m = "0.0.0.0/0" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mgateway_id[0m[0m             = "igw-0a50f3779bbb0ed48" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                     = "r-rtb-00ef6db6e42a251121080289494" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0morigin[0m[0m                 = "CreateRoute" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mroute_table_id[0m[0m         = "rtb-00ef6db6e42a25112" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mstate[0m[0m                  = "active" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.vpc_aws.aws_route_table.ag_tfe_route_table[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_route_table" "ag_tfe_route_table" {
      [31m-[0m [0m[1m[0mid[0m[0m               = "rtb-00ef6db6e42a25112" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mowner_id[0m[0m         = "729476260648" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mpropagating_vgws[0m[0m = [] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mroute[0m[0m            = [
          [31m-[0m [0m{
              [31m-[0m [0mcidr_block                = "0.0.0.0/0"
              [31m-[0m [0megress_only_gateway_id    = ""
              [31m-[0m [0mgateway_id                = "igw-0a50f3779bbb0ed48"
              [31m-[0m [0minstance_id               = ""
              [31m-[0m [0mipv6_cidr_block           = ""
              [31m-[0m [0mnat_gateway_id            = ""
              [31m-[0m [0mnetwork_interface_id      = ""
              [31m-[0m [0mtransit_gateway_id        = ""
              [31m-[0m [0mvpc_peering_connection_id = ""
            },
        ] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m             = {
          [31m-[0m [0m"Name" = "ag_ptfe_pm_route_table"
        } [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvpc_id[0m[0m           = "vpc-078b83e18678dbc8e" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.vpc_aws.aws_route_table_association.ag_tfe_association[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_route_table_association" "ag_tfe_association" {
      [31m-[0m [0m[1m[0mid[0m[0m             = "rtbassoc-017444ee20aa74572" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mroute_table_id[0m[0m = "rtb-00ef6db6e42a25112" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0msubnet_id[0m[0m      = "subnet-00fe0b043ebd95afe" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.vpc_aws.aws_security_group.ag_tfe_Security_Group[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_security_group" "ag_tfe_Security_Group" {
      [31m-[0m [0m[1m[0marn[0m[0m                    = "arn:aws:ec2:eu-central-1:729476260648:security-group/sg-0a1b2ba13f83f6ba1" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdescription[0m[0m            = "ag_ptfe_pm Security Group" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0megress[0m[0m                 = [
          [31m-[0m [0m{
              [31m-[0m [0mcidr_blocks      = [
                  [31m-[0m [0m"0.0.0.0/0",
                ]
              [31m-[0m [0mdescription      = ""
              [31m-[0m [0mfrom_port        = 1024
              [31m-[0m [0mipv6_cidr_blocks = []
              [31m-[0m [0mprefix_list_ids  = []
              [31m-[0m [0mprotocol         = "tcp"
              [31m-[0m [0msecurity_groups  = []
              [31m-[0m [0mself             = false
              [31m-[0m [0mto_port          = 65535
            },
          [31m-[0m [0m{
              [31m-[0m [0mcidr_blocks      = [
                  [31m-[0m [0m"0.0.0.0/0",
                ]
              [31m-[0m [0mdescription      = ""
              [31m-[0m [0mfrom_port        = 443
              [31m-[0m [0mipv6_cidr_blocks = []
              [31m-[0m [0mprefix_list_ids  = []
              [31m-[0m [0mprotocol         = "tcp"
              [31m-[0m [0msecurity_groups  = []
              [31m-[0m [0mself             = false
              [31m-[0m [0mto_port          = 443
            },
          [31m-[0m [0m{
              [31m-[0m [0mcidr_blocks      = [
                  [31m-[0m [0m"0.0.0.0/0",
                ]
              [31m-[0m [0mdescription      = ""
              [31m-[0m [0mfrom_port        = 80
              [31m-[0m [0mipv6_cidr_blocks = []
              [31m-[0m [0mprefix_list_ids  = []
              [31m-[0m [0mprotocol         = "tcp"
              [31m-[0m [0msecurity_groups  = []
              [31m-[0m [0mself             = false
              [31m-[0m [0mto_port          = 80
            },
        ] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                     = "sg-0a1b2ba13f83f6ba1" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mingress[0m[0m                = [
          [31m-[0m [0m{
              [31m-[0m [0mcidr_blocks      = [
                  [31m-[0m [0m"0.0.0.0/0",
                ]
              [31m-[0m [0mdescription      = ""
              [31m-[0m [0mfrom_port        = 22
              [31m-[0m [0mipv6_cidr_blocks = []
              [31m-[0m [0mprefix_list_ids  = []
              [31m-[0m [0mprotocol         = "tcp"
              [31m-[0m [0msecurity_groups  = []
              [31m-[0m [0mself             = false
              [31m-[0m [0mto_port          = 22
            },
          [31m-[0m [0m{
              [31m-[0m [0mcidr_blocks      = [
                  [31m-[0m [0m"0.0.0.0/0",
                ]
              [31m-[0m [0mdescription      = ""
              [31m-[0m [0mfrom_port        = 443
              [31m-[0m [0mipv6_cidr_blocks = []
              [31m-[0m [0mprefix_list_ids  = []
              [31m-[0m [0mprotocol         = "tcp"
              [31m-[0m [0msecurity_groups  = []
              [31m-[0m [0mself             = false
              [31m-[0m [0mto_port          = 443
            },
          [31m-[0m [0m{
              [31m-[0m [0mcidr_blocks      = [
                  [31m-[0m [0m"0.0.0.0/0",
                ]
              [31m-[0m [0mdescription      = ""
              [31m-[0m [0mfrom_port        = 8800
              [31m-[0m [0mipv6_cidr_blocks = []
              [31m-[0m [0mprefix_list_ids  = []
              [31m-[0m [0mprotocol         = "tcp"
              [31m-[0m [0msecurity_groups  = []
              [31m-[0m [0mself             = false
              [31m-[0m [0mto_port          = 8800
            },
        ] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mname[0m[0m                   = "ag_ptfe_pm Security Group" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mowner_id[0m[0m               = "729476260648" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mrevoke_rules_on_delete[0m[0m = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m                   = {
          [31m-[0m [0m"Name" = "ag_ptfe_pm_security_group"
        } [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvpc_id[0m[0m                 = "vpc-078b83e18678dbc8e" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.vpc_aws.aws_security_group.ag_tfe_Security_Group_db[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_security_group" "ag_tfe_Security_Group_db" {
      [31m-[0m [0m[1m[0marn[0m[0m                    = "arn:aws:ec2:eu-central-1:729476260648:security-group/sg-09bd7b30129de4964" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdescription[0m[0m            = "ag_ptfe_pm-sg-db" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0megress[0m[0m                 = [] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                     = "sg-09bd7b30129de4964" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mingress[0m[0m                = [
          [31m-[0m [0m{
              [31m-[0m [0mcidr_blocks      = [
                  [31m-[0m [0m"0.0.0.0/0",
                ]
              [31m-[0m [0mdescription      = ""
              [31m-[0m [0mfrom_port        = 5432
              [31m-[0m [0mipv6_cidr_blocks = []
              [31m-[0m [0mprefix_list_ids  = []
              [31m-[0m [0mprotocol         = "tcp"
              [31m-[0m [0msecurity_groups  = []
              [31m-[0m [0mself             = false
              [31m-[0m [0mto_port          = 5432
            },
        ] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mname[0m[0m                   = "ag_ptfe_pm-sg-db" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mowner_id[0m[0m               = "729476260648" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mrevoke_rules_on_delete[0m[0m = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m                   = {
          [31m-[0m [0m"Name" = "ag_ptfe_pm_security_group"
        } [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvpc_id[0m[0m                 = "vpc-078b83e18678dbc8e" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.vpc_aws.aws_security_group.ag_tfe_Security_Group_elb[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_security_group" "ag_tfe_Security_Group_elb" {
      [31m-[0m [0m[1m[0marn[0m[0m                    = "arn:aws:ec2:eu-central-1:729476260648:security-group/sg-05116856615e4a32f" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdescription[0m[0m            = "ag_ptfe_pm ELB Security Group" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0megress[0m[0m                 = [
          [31m-[0m [0m{
              [31m-[0m [0mcidr_blocks      = [
                  [31m-[0m [0m"0.0.0.0/0",
                ]
              [31m-[0m [0mdescription      = ""
              [31m-[0m [0mfrom_port        = 0
              [31m-[0m [0mipv6_cidr_blocks = []
              [31m-[0m [0mprefix_list_ids  = []
              [31m-[0m [0mprotocol         = "-1"
              [31m-[0m [0msecurity_groups  = []
              [31m-[0m [0mself             = false
              [31m-[0m [0mto_port          = 0
            },
        ] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                     = "sg-05116856615e4a32f" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mingress[0m[0m                = [
          [31m-[0m [0m{
              [31m-[0m [0mcidr_blocks      = [
                  [31m-[0m [0m"0.0.0.0/0",
                ]
              [31m-[0m [0mdescription      = ""
              [31m-[0m [0mfrom_port        = 443
              [31m-[0m [0mipv6_cidr_blocks = []
              [31m-[0m [0mprefix_list_ids  = []
              [31m-[0m [0mprotocol         = "tcp"
              [31m-[0m [0msecurity_groups  = []
              [31m-[0m [0mself             = false
              [31m-[0m [0mto_port          = 443
            },
          [31m-[0m [0m{
              [31m-[0m [0mcidr_blocks      = [
                  [31m-[0m [0m"0.0.0.0/0",
                ]
              [31m-[0m [0mdescription      = ""
              [31m-[0m [0mfrom_port        = 8800
              [31m-[0m [0mipv6_cidr_blocks = []
              [31m-[0m [0mprefix_list_ids  = []
              [31m-[0m [0mprotocol         = "tcp"
              [31m-[0m [0msecurity_groups  = []
              [31m-[0m [0mself             = false
              [31m-[0m [0mto_port          = 8800
            },
        ] [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mname[0m[0m                   = "ag_ptfe_pm-sg-elb" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mowner_id[0m[0m               = "729476260648" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mrevoke_rules_on_delete[0m[0m = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m                   = {} [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvpc_id[0m[0m                 = "vpc-078b83e18678dbc8e" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.vpc_aws.aws_subnet.ag_tfe_Subnet[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_subnet" "ag_tfe_Subnet" {
      [31m-[0m [0m[1m[0marn[0m[0m                             = "arn:aws:ec2:eu-central-1:729476260648:subnet/subnet-00fe0b043ebd95afe" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0massign_ipv6_address_on_creation[0m[0m = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mavailability_zone[0m[0m               = "eu-central-1a" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mavailability_zone_id[0m[0m            = "euc1-az2" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mcidr_block[0m[0m                      = "10.0.1.0/24" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                              = "subnet-00fe0b043ebd95afe" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmap_public_ip_on_launch[0m[0m         = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mowner_id[0m[0m                        = "729476260648" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m                            = {
          [31m-[0m [0m"Name" = "ag_ptfe_pm_subnet"
        } [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvpc_id[0m[0m                          = "vpc-078b83e18678dbc8e" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.vpc_aws.aws_subnet.rds[0][0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_subnet" "rds" {
      [31m-[0m [0m[1m[0marn[0m[0m                             = "arn:aws:ec2:eu-central-1:729476260648:subnet/subnet-0b33618b0758403b9" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0massign_ipv6_address_on_creation[0m[0m = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mavailability_zone[0m[0m               = "eu-central-1a" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mavailability_zone_id[0m[0m            = "euc1-az2" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mcidr_block[0m[0m                      = "10.0.3.0/24" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                              = "subnet-0b33618b0758403b9" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmap_public_ip_on_launch[0m[0m         = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mowner_id[0m[0m                        = "729476260648" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m                            = {} [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvpc_id[0m[0m                          = "vpc-078b83e18678dbc8e" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.vpc_aws.aws_subnet.rds[1][0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_subnet" "rds" {
      [31m-[0m [0m[1m[0marn[0m[0m                             = "arn:aws:ec2:eu-central-1:729476260648:subnet/subnet-0d03df45737943a7b" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0massign_ipv6_address_on_creation[0m[0m = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mavailability_zone[0m[0m               = "eu-central-1b" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mavailability_zone_id[0m[0m            = "euc1-az3" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mcidr_block[0m[0m                      = "10.0.4.0/24" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                              = "subnet-0d03df45737943a7b" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmap_public_ip_on_launch[0m[0m         = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mowner_id[0m[0m                        = "729476260648" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m                            = {} [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvpc_id[0m[0m                          = "vpc-078b83e18678dbc8e" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.vpc_aws.aws_subnet.rds[2][0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_subnet" "rds" {
      [31m-[0m [0m[1m[0marn[0m[0m                             = "arn:aws:ec2:eu-central-1:729476260648:subnet/subnet-0b7becf732702638d" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0massign_ipv6_address_on_creation[0m[0m = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mavailability_zone[0m[0m               = "eu-central-1c" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mavailability_zone_id[0m[0m            = "euc1-az1" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mcidr_block[0m[0m                      = "10.0.5.0/24" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                              = "subnet-0b7becf732702638d" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmap_public_ip_on_launch[0m[0m         = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mowner_id[0m[0m                        = "729476260648" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m                            = {} [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mvpc_id[0m[0m                          = "vpc-078b83e18678dbc8e" [90m->[0m [0m[90mnull[0m[0m
    }

[1m  # module.vpc_aws.aws_vpc.ag_tfe[0m will be [1m[31mdestroyed[0m[0m
[0m[31m  -[0m [0mresource "aws_vpc" "ag_tfe" {
      [31m-[0m [0m[1m[0marn[0m[0m                              = "arn:aws:ec2:eu-central-1:729476260648:vpc/vpc-078b83e18678dbc8e" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0massign_generated_ipv6_cidr_block[0m[0m = false [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mcidr_block[0m[0m                       = "10.0.0.0/16" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdefault_network_acl_id[0m[0m           = "acl-078d4d1af573f9a4c" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdefault_route_table_id[0m[0m           = "rtb-065c65201758bae6a" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdefault_security_group_id[0m[0m        = "sg-0f7d4c68726b7b411" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mdhcp_options_id[0m[0m                  = "dopt-4f934827" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0menable_dns_hostnames[0m[0m             = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0menable_dns_support[0m[0m               = true [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mid[0m[0m                               = "vpc-078b83e18678dbc8e" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0minstance_tenancy[0m[0m                 = "default" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mmain_route_table_id[0m[0m              = "rtb-065c65201758bae6a" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mowner_id[0m[0m                         = "729476260648" [90m->[0m [0m[90mnull[0m[0m
      [31m-[0m [0m[1m[0mtags[0m[0m                             = {
          [31m-[0m [0m"Name" = "ag_ptfe_pm"
        } [90m->[0m [0m[90mnull[0m[0m
    }

[0m[1mPlan:[0m 0 to add, 0 to change, 30 to destroy.[0m

[0m[1mDo you really want to destroy all resources?[0m
  Terraform will destroy all your managed infrastructure, as shown above.
  There is no undo. Only 'yes' will be accepted to confirm.

  [1mEnter a value:[0m [0m
[0m[1mmodule.db_aws.null_resource.timed-pw-out: Destroying... [id=6420129020507274029][0m[0m
[0m[1mmodule.bootstrap_pg_rds_aws.null_resource.pg-rds-bootstrap: Destroying... [id=8289507824799680102][0m[0m
[0m[1mmodule.db_aws.null_resource.timed-pw-out: Destruction complete after 0s[0m[0m
[0m[1mmodule.sslcert_letsencrypt.local_file.ssl_cert_file: Destroying... [id=ba64c6f4b5dad041f329602e09d47b1bdaf8d02f][0m[0m
[0m[1mmodule.sslcert_letsencrypt.local_file.ssl_private_key_file: Destroying... [id=618f6dd031a1424b103be71d4e438f76e6efb4ea][0m[0m
[0m[1mmodule.bootstrap_pg_rds_aws.null_resource.pg-rds-bootstrap: Destruction complete after 0s[0m[0m
[0m[1mmodule.sslcert_letsencrypt.local_file.ssl_cert_file: Destruction complete after 0s[0m[0m
[0m[1mmodule.sslcert_letsencrypt.local_file.ssl_private_key_file: Destruction complete after 0s[0m[0m
[0m[1mmodule.sslcert_letsencrypt.local_file.ssl_cert_bundle_file: Destroying... [id=4882919556e0ed69bdbe0f6ef4d38ef5ee870f05][0m[0m
[0m[1mmodule.sslcert_letsencrypt.local_file.ssl_cert_bundle_file: Destruction complete after 0s[0m[0m
[0m[1mmodule.dns_cloudflare.cloudflare_record.site_lb: Destroying... [id=94128084dbc97da7cc4d80bf40d7f8ed][0m[0m
[0m[1mmodule.dns_cloudflare.cloudflare_record.site_backend: Destroying... [id=c0a89c909d2ac1f904c9dc0087259109][0m[0m
[0m[1mmodule.sslcert_letsencrypt.acme_certificate.certificate: Destroying... [id=https://acme-v02.api.letsencrypt.org/acme/cert/03f8397c0693851dbf8ead6bad4db1d3757a][0m[0m
[0m[1mmodule.dns_cloudflare.cloudflare_record.site_backend: Destruction complete after 1s[0m[0m
[0m[1mmodule.dns_cloudflare.cloudflare_record.site_lb: Destruction complete after 1s[0m[0m
[0m[1mmodule.vpc_aws.aws_route.ag_tfe_internet_access: Destroying... [id=r-rtb-00ef6db6e42a251121080289494][0m[0m
[0m[1mmodule.vpc_aws.aws_route_table_association.ag_tfe_association: Destroying... [id=rtbassoc-017444ee20aa74572][0m[0m
[0m[1mmodule.lb_aws.aws_elb.ptfe_lb: Destroying... [id=ag-clb-ag-clb-tfe-ext-dr-1][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Destroying... [id=terraform-20191118133250830800000002][0m[0m
[0m[1mmodule.objectstorage_aws.aws_s3_bucket.tfebucket: Destroying... [id=tfe-ext-dr-1-ec590f4bd918e366][0m[0m
[0m[1mmodule.vpc_aws.aws_route_table_association.ag_tfe_association: Destruction complete after 0s[0m[0m
[0m[1mmodule.vpc_aws.aws_route.ag_tfe_internet_access: Destruction complete after 0s[0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Destroying... [id=igw-0a50f3779bbb0ed48][0m[0m
[0m[1mmodule.vpc_aws.aws_route_table.ag_tfe_route_table: Destroying... [id=rtb-00ef6db6e42a25112][0m[0m
[0m[1mmodule.sslcert_letsencrypt.acme_certificate.certificate: Destruction complete after 2s[0m[0m
[0m[1mmodule.sslcert_letsencrypt.acme_registration.reg: Destroying... [id=https://acme-v02.api.letsencrypt.org/acme/acct/72025870][0m[0m
[0m[1mmodule.objectstorage_aws.aws_s3_bucket.tfebucket: Destruction complete after 0s[0m[0m
[0m[1mmodule.objectstorage_aws.random_id.bucket: Destroying... [id=7FkPS9kY42Y][0m[0m
[0m[1mmodule.objectstorage_aws.random_id.bucket: Destruction complete after 0s[0m[0m
[0m[1mmodule.vpc_aws.aws_route_table.ag_tfe_route_table: Destruction complete after 0s[0m[0m
[0m[1mmodule.lb_aws.aws_elb.ptfe_lb: Destruction complete after 0s[0m[0m
[0m[1mmodule.vpc_aws.aws_security_group.ag_tfe_Security_Group_elb: Destroying... [id=sg-05116856615e4a32f][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Destroying... [id=i-095d6319db47efab8][0m[0m
[0m[1mmodule.sslcert_letsencrypt.acme_registration.reg: Destruction complete after 1s[0m[0m
[0m[1mmodule.sslcert_letsencrypt.tls_private_key.private_key: Destroying... [id=a27a7f05abaf1e14c32e88ca3d97b6916169edce][0m[0m
[0m[1mmodule.sslcert_letsencrypt.tls_private_key.private_key: Destruction complete after 0s[0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 10s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 10s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 10s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_security_group.ag_tfe_Security_Group_elb: Still destroying... [id=sg-05116856615e4a32f, 10s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 20s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 20s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_security_group.ag_tfe_Security_Group_elb: Still destroying... [id=sg-05116856615e4a32f, 20s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 20s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_security_group.ag_tfe_Security_Group_elb: Destruction complete after 28s[0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 30s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 30s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 30s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 40s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 40s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 40s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 50s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 50s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 50s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 1m0s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 1m0s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 1m0s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 1m10s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 1m10s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 1m10s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 1m20s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 1m20s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 1m20s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 1m30s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 1m30s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 1m30s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 1m40s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 1m40s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 1m40s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 1m50s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 1m50s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 1m50s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 2m0s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 2m0s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 2m0s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 2m10s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 2m10s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 2m10s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 2m20s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 2m20s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 2m20s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 2m30s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 2m30s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 2m30s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 2m40s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 2m40s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 2m40s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 2m50s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 2m50s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 2m50s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 3m0s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 3m0s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 3m0s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 3m10s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 3m10s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 3m10s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 3m20s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 3m20s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 3m20s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 3m30s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Still destroying... [id=igw-0a50f3779bbb0ed48, 3m30s elapsed][0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Still destroying... [id=i-095d6319db47efab8, 3m30s elapsed][0m[0m
[0m[1mmodule.vpc_aws.aws_internet_gateway.ag_tfe_GW: Destruction complete after 3m31s[0m[0m
[0m[1mmodule.compute_aws.aws_instance.ptfe: Destruction complete after 3m33s[0m[0m
[0m[1mmodule.sshkey_aws.aws_key_pair.sshkey: Destroying... [id=tfe-ext-dr-1][0m[0m
[0m[1mmodule.vpc_aws.aws_subnet.ag_tfe_Subnet: Destroying... [id=subnet-00fe0b043ebd95afe][0m[0m
[0m[1mmodule.vpc_aws.aws_security_group.ag_tfe_Security_Group: Destroying... [id=sg-0a1b2ba13f83f6ba1][0m[0m
[0m[1mmodule.sshkey_aws.aws_key_pair.sshkey: Destruction complete after 0s[0m[0m
[0m[1mmodule.vpc_aws.aws_security_group.ag_tfe_Security_Group: Destruction complete after 1s[0m[0m
[0m[1mmodule.vpc_aws.aws_subnet.ag_tfe_Subnet: Destruction complete after 1s[0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 3m40s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Still destroying... [id=terraform-20191118133250830800000002, 3m50s elapsed][0m[0m
[0m[1mmodule.db_aws.aws_db_instance.tfe_db: Destruction complete after 3m55s[0m[0m
[0m[1mmodule.db_aws.random_password.password: Destroying... [id=none][0m[0m
[0m[1mmodule.db_aws.aws_db_subnet_group.tfe: Destroying... [id=agtfeextdr1-rds-subnet-group][0m[0m
[0m[1mmodule.vpc_aws.aws_security_group.ag_tfe_Security_Group_db: Destroying... [id=sg-09bd7b30129de4964][0m[0m
[0m[1mmodule.db_aws.random_password.password: Destruction complete after 0s[0m[0m
[0m[1mmodule.db_aws.aws_db_subnet_group.tfe: Destruction complete after 0s[0m[0m
[0m[1mmodule.vpc_aws.aws_subnet.rds[0]: Destroying... [id=subnet-0b33618b0758403b9][0m[0m
[0m[1mmodule.vpc_aws.aws_subnet.rds[2]: Destroying... [id=subnet-0b7becf732702638d][0m[0m
[0m[1mmodule.vpc_aws.aws_subnet.rds[1]: Destroying... [id=subnet-0d03df45737943a7b][0m[0m
[0m[1mmodule.vpc_aws.aws_security_group.ag_tfe_Security_Group_db: Destruction complete after 0s[0m[0m
[0m[1mmodule.vpc_aws.aws_subnet.rds[1]: Destruction complete after 1s[0m[0m
[0m[1mmodule.vpc_aws.aws_subnet.rds[2]: Destruction complete after 1s[0m[0m
[0m[1mmodule.vpc_aws.aws_subnet.rds[0]: Destruction complete after 1s[0m[0m
[0m[1mmodule.vpc_aws.aws_vpc.ag_tfe: Destroying... [id=vpc-078b83e18678dbc8e][0m[0m
[0m[1mmodule.vpc_aws.aws_vpc.ag_tfe: Destruction complete after 0s[0m[0m
[0m[1m[32m
Destroy complete! Resources: 30 destroyed.[0m
2019-11-19_16-03
```

