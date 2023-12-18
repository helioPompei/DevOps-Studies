# What is cloud computing?

> **Cloud computing is the on-demand delivery of IT resources over the Internet with pay-as-you-go pricing. Instead of buying, owning, and maintaining physical data centers and servers, you can access technology services, such as computing power, storage, and databases, on an as-needed basis from a cloud provider like Amazon Web Services (AWS)**

### Deployments Models of the cloud
- `Private Cloud` Dedicated cloud infrastructure exclusively used by a single organization.
- `Public Cloud` Resources and services are hosted on shared infrastructure accessible over the internet. AWS itself operates as a public cloud provider.
- `Hybrid Cloud` Combination of public and private clouds allowing data and applications to be shared between them.

### Types of cloud
- `IaaS (Infra as a Service)` You host and manage the infrastructure, provisioning and configuring servers, storage, and networking resources.
- `PaaS (Plataform as a Service)` Offers an operating system and necessary dependencies for application development, allowing developers to focus on coding without managing the underlying infrastructure.
- `SaaS (Software as a Service)` For End Users. Access ready-to-use software applications like Gmail, Office 365, etc., paying for usage without worrying about installation or infrastructure management.

# ====================================================================
# IAM (Identity and Access management)
# ====================================================================
- User      
- Groups    (Varios usuarios)
- Policies  (Permitir ou bloquear acesso de grupos ou usuarios)
- Roles     (politicas para serviços ex: ec2 logar em um S3)
- MFA + Password Policy  (Mudar a politica de senhas)

- IAM Security Tools:
  - IAM credentials report  (List all account's user and the status)
  - IAM Access advisor      (Show when services were last accesssed)

## AWS ACCESS
    - CONSOLE
    - CLI
    - SDK
    - CloudShell

# ====================================================================
# EC2 Elastic Compute Cloud 
# ====================================================================
## Types of EC2 Instances 
  - General Purpose       ( Proposito geral )
  - Compute Optimized     ( Otimizada para CPU )
  - Memory Optimized      ( Otimizada para Memoria RAM )
  - Storage Optimized     ( Otimizada para SDD/HDD/ARMAZENAMENTO )
  - Accelerated Computing ( Baseadas em GPU )

## EC2 Pricing 
  - On-Demand             ( Pay for what you use )
  - Saving Plans          ( commitment of usage, in USD per hour, 1 or 3 years )
  - Reserved Instances    ( commitment of instance configuration, 1 or 3 years )
  - Spot Instances        ( AWS reivindicar a qualquer momento 90% de desconto)
  - Dedicated Hosts       ( Physical EC2 server fully dedicated for your use )
  - Dedicated Instances   ( Pay by the hour, for instances that run on single-tenant hardware)
  - Capacity Reservations ( Reserve capacity in a specific AZ for any duration )

## EC2 Scaling
- Amazon EC2 Auto Scaling
- Auto Scaling Group
- Dynamic Scaling
- Predictive Scaling

## EC2 Elastic Load Balancing
- Automatically distributes incoming application traffic across multiple targets and virtual appliances in one or more Availability Zones

## Messaging and Queuing 
- Amazon SQS (Simple Queue Service)
- Amazon SNS (Simple Notification Service)

## Additional Compute Services 
- AWS Lambda -> Serverless means that your code runs on servers, but you do not need to provision or manage these servers.
- Amazon Elastic Container Service (Amazon ECS)
- Amazon Elastic Kubernetes Service (Amazon EKS)(opens in a new tab) 
- AWS Fargate -> When using AWS Fargate, you do not need to provision or manage servers. AWS Fargate manages your server infrastructure for you. 

# ====================================================================
# S3 (Simple Storage Service) 
# ====================================================================
- Bucket (Pasta com nome unico e universal)
- ACL (Access List)
- Buckets Policys (Políticas de acesso para o bucket)

## Types of S3 
- S3 Standard (Mais caro, rapido e confiável)
- S3 Intelligent-Tiering (Move automaticamente para as classes mais baratas os arquivos menos usados)
- Standard-IA Infrequent Access (Recomendado para backups, arquivos que não podem ser acessados muitas vezes para evitar custos adicionais)
- One Zone-IA Infrequent Access (Mesmo do de cima porém single zone)
- Glacier (Arquivos acessados 1 ou 2 vezes por ANO)
- S3 Glacier Deep Archive (Acesso de no minimo 7 a 10 anos)

- Mover aquivos possuem custo
- É possivel fazer versionamento no S3 (Ao habilitar não é possivel desabilitar)
- Rastreamento para tudo que acontece na Bucket S3
- Server Access Logging (Logs de acesso para bucket S3)
- Hospedagem de Website no S3

# ====================================================================
# VPC (Virtual Private Cloud)
# ====================================================================
- VPC               Linked to a Region
- Subnets           Linked to a Availability Zone  
- Route Tables      Define access to the internet and between subnets 
- IGW               Roteador virtual que conecta uma VPC à internet
- NAT               Network address translation

- NACL              Controls traffic from and to subnet (Subnet level)
- SG                A firewall that controls traffic to and from an EC2 instance

- VPC Peering (Conexão entre VPC's)
- VPC Endpoints (A VPC endpoint enables customers to privately connect to supported AWS services and VPC endpoint services powered by AWS PrivateLink)
    - Endpoint gateway: S3, DynamoDB 
    - Another Services
