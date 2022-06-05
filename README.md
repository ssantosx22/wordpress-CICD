# wordpress

## Objetivo

Provisionar imagem AMI usando packer e já instalado wordpress usando ansible, a parte da infraestrutura fica a cargo do terraform

## Dependências

- terraform v1.0.0
- packer v1.8.0
- ansible v2.10.5

## Variaveis gitlab-ci

- AWS_ACCESS_KEY
- AWS_SECRET_KEY
- AWS_DEFAULT_REGION
- AWS_SOURCE_AMI

Criar environments *prd* e *dev* a fim de segmentar os ambientes 

<img src="https://i.imgur.com/FjSEqq8.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" />

Aprovação em prd requer uma ação manual

## Variaveis Terraform

Criar arquivo .tfvars para setar as variáveis obrigátorias no terraform segue exemplo:
```
name           = "ec2 by terraform"
instance_type  = "TYPE-INSTANCE"
region         = "REGION"
key_name       = "my-key"
vpc_id         = "vpc-abcde"
subnet_id      = "subnet-abcde"
vpc_cidr_block = "0.0.0.0/0"
```

## License
For open source projects, say how it is licensed.

