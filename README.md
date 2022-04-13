### List workspace
`terraform workspace list`

### Use aws-vault command, to login AWS credentials.
`aws-vault exec admin --no-session`

`docker-compose -f deploy/docker-compose.yml run --rm terraform workspace select prod`

### Check the AWS resource changes

`docker-compose -f deploy/docker-compose.yml run --rm terraform plan -var-file tfvars/prod.tfvars`

### Apply AWS resource changes

`docker-compose -f deploy/docker-compose.yml run --rm terraform apply -var-file tfvars/prod.tfvars -auto-approve`
