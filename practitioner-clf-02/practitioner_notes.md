# ====================================================================
# Visão geral do exame 
# ====================================================================
- 90 Minutos 
- 65 Questões / múltipla escolha ou múltipla resposta
- Domínio 1: Conceitos da nuvem (24% do conteúdo pontuado)
- Domínio 2: Segurança e conformidade (30% do conteúdo pontuado)
- Domínio 3: Tecnologia e serviços da nuvem (34% do conteúdo pontuado) 
- Domínio 4: Cobrança, preços e suporte (12% do conteúdo pontuado)

# ====================================================================
# Cloud Advantages and Benefits
# ====================================================================
- Velocidade de implementação 
- Update de sistemas operacionais sem interromper o serviço
- Custo baixo
- Data security (segurança dos dados)
- Scalability   (serviços e aplicações Escaláveis)

# ====================================================================
# Types of Cloud (Basico para avançado)
# ====================================================================
- IaaS -> Infra (Hospedar -> SysAdmins / Você provisiona e configura a infra)
- PaaS -> Plataform (Programar -> Developers / Sistema operacional e dependencias)
- SaaS -> Software (Usar -> Final Users / Gmail, Office... etc, pay to use the software)

- Regions -> AZs -> Local zones

- Public Cloud  (AWS disponibiliza ao publico)
- Hybrid Cloud  (Parte on-premise parte AWS cloud)
- Private Cloud (AWS aluga o hardware fisico somente para você)

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
