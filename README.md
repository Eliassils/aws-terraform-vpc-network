# AWS E-commerce Infrastructure with Terraform 🚀

Este repositório contém a infraestrutura como código (IaC) para um ambiente de e-commerce escalável na AWS. O objetivo deste projeto é criar uma rede segura e resiliente seguindo as melhores práticas de mercado.

## 🏗️ Arquitetura da Rede (VPC)

A infraestrutura foi desenhada para separar as camadas de aplicação e banco de dados, garantindo maior segurança:

* **VPC:** Rede isolada com endereçamento IP customizado.
* **Public Subnets:** Destinadas a recursos que precisam de acesso direto à internet (ex: Load Balancers, Bastion Hosts).
* **Private Subnets:** Onde ficam os servidores de aplicação e bancos de dados, protegidos do acesso externo direto.
* **NAT Gateway:** Permite que os recursos nas subnets privadas baixem atualizações sem ficarem expostos.
* **Internet Gateway:** Porta de entrada e saída para o tráfego da internet nas subnets públicas.

## 🛠️ Tecnologias Utilizadas

* [Terraform](https://www.terraform.io/) - Ferramenta de IaC para provisionamento de recursos.
* [AWS](https://aws.amazon.com/) - Provedor de nuvem utilizado.
* [Git](https://git-scm.com/) - Controle de versão.

## 📁 Estrutura de Arquivos

```text
networking/
├── vpc.tf                # Definição da VPC principal
├── vpc_public_subnet.tf  # Subnets com acesso à internet
├── vpc_private_subnet.tf # Subnets isoladas
├── internet_gateway.tf   # Gateway para tráfego externo
├── vpc_nat_gateway.tf    # Gateway para saída de subnets privadas



├── route_table.tf        # Tabelas de roteamento
├── variables.tf          # Variáveis do projeto
└── main.tf               # Configuração do Provider e Backend

<img width="1919" height="1079" alt="Captura de tela 2026-04-01 114908" src="https://github.com/user-attachments/assets/02e615ef-66ba-436c-afb4-860a9eaf491a" />

<img width="1919" height="1027" alt="Captura de tela 2026-04-01 114928" src="https://github.com/user-attachments/assets/c7cc1042-675d-424b-823f-742fddd2af97" />

<img width="1919" height="658" alt="Captura de tela 2026-04-01 115004" src="https://github.com/user-attachments/assets/379022c3-2f51-40fd-89dd-9e61b2f16a78" />

<img width="1446" height="758" alt="Captura de tela 2026-04-01 115019" src="https://github.com/user-attachments/assets/7b87de2c-4fe4-43f2-8def-4e732ae44e99" />

<img width="1914" height="865" alt="Captura de tela 2026-04-01 115032" src="https://github.com/user-attachments/assets/c3f3910d-31a6-4834-95aa-4a64de91b823" />

<img width="1919" height="866" alt="Captura de tela 2026-04-01 115043" src="https://github.com/user-attachments/assets/2f68b2ab-d475-4ce4-a80b-80781791ee58" />

<img width="1919" height="866" alt="Captura de tela 2026-04-01 115056" src="https://github.com/user-attachments/assets/dc67d3a2-9c45-407b-b71d-b8f60aa9bb92" />

<img width="1919" height="802" alt="Captura de tela 2026-04-01 115108" src="https://github.com/user-attachments/assets/36e5eea6-b78a-448d-ad34-222a8249df45" />

<img width="1919" height="787" alt="Captura de tela 2026-04-01 115121" src="https://github.com/user-attachments/assets/c9317166-15b2-4607-be37-8babbaa96422" />

<img width="1919" height="866" alt="Captura de tela 2026-04-01 115131" src="https://github.com/user-attachments/assets/2ece501f-9ee2-4f37-a262-041fa49b98c7" />

<img width="1919" height="872" alt="Captura de tela 2026-04-01 115142" src="https://github.com/user-attachments/assets/af781078-98a5-477a-ae06-453288039a9d" />

<img width="1919" height="935" alt="Captura de tela 2026-04-01 115154" src="https://github.com/user-attachments/assets/68adc129-7bee-404d-b556-8da0a39d654e" />

<img width="1548" height="71" alt="Captura de tela 2026-04-01 120036" src="https://github.com/user-attachments/assets/b1b01fb0-c99a-4179-989f-0ac516db3883" />

<img width="1543" height="361" alt="Captura de tela 2026-04-01 120128" src="https://github.com/user-attachments/assets/40d92656-e565-4ac2-b5e4-564665bb3bb6" />

<img width="1606" height="336" alt="Captura de tela 2026-04-01 120147" src="https://github.com/user-attachments/assets/cf2117bf-a76a-44ea-a663-91252258f881" />

<img width="1537" height="254" alt="Captura de tela 2026-04-01 120211" src="https://github.com/user-attachments/assets/3896ae9c-67f2-458f-8380-0f20361ab189" />

<img width="1579" height="99" alt="Captura de tela 2026-04-01 120232" src="https://github.com/user-attachments/assets/9a57a082-9b50-44d2-9239-f5081f9d5dd4" />

<img width="1576" height="134" alt="Captura de tela 2026-04-01 120314" src="https://github.com/user-attachments/assets/1050b4c5-9b7e-4620-a5dd-7856558dcf78" />

<img width="1609" height="409" alt="Captura de tela 2026-04-01 120340" src="https://github.com/user-attachments/assets/9d3fe630-6bf8-4ec2-a49e-25c7ee56296e" />

<img width="1606" height="401" alt="Captura de tela 2026-04-01 120416" src="https://github.com/user-attachments/assets/545dfed2-2524-4353-817d-65e8cb885bdf" />

<img width="1568" height="331" alt="Captura de tela 2026-04-01 120445" src="https://github.com/user-attachments/assets/43506dd8-6fb5-4750-9fcd-1324bd428009" />























