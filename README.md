# AWS E-commerce Infrastructure with Terraform 🚀

Este repositório contém a infraestrutura como código (IaC) para um ambiente de e-commerce escalável na AWS. O objetivo deste projeto é criar uma rede segura e resiliente seguindo as melhores práticas de mercado.

## 🏗️ Arquitetura da Rede (VPC)

A infraestrutura foi desenhada para separar as camadas de aplicação e banco de dados, garantindo maior segurança:

* **VPC:** Rede isolada com endereçamento IP customizado para o e-commerce.
* **Public Subnets:** Destinadas a recursos que precisam de acesso direto à internet (ex: Load Balancers).
* **Private Subnets:** Onde ficam os servidores de aplicação e bancos de dados, protegidos do acesso externo.
* **NAT Gateway:** Permite que as subnets privadas baixem atualizações sem exposição direta.
* **Internet Gateway:** Porta de entrada e saída principal para o tráfego da internet.

---

### 📸 Screenshots do Projeto (Evidências de Implementação)

Aqui estão as capturas de tela das etapas de configuração e dos recursos provisionados:

<div align="center">
  <img src="https://github.com/user-attachments/assets/02e615ef-66ba-436c-afb4-860a9eaf491a" width="45%" alt="Print 1" />
  <img src="https://github.com/user-attachments/assets/c7cc1042-675d-424b-823f-742fddd2af97" width="45%" alt="Print 2" />
  <img src="https://github.com/user-attachments/assets/379022c3-2f51-40fd-89dd-9e61b2f16a78" width="45%" alt="Print 3" />
  <img src="https://github.com/user-attachments/assets/7b87de2c-4fe4-43f2-8def-4e732ae44e99" width="45%" alt="Print 4" />
  <img src="https://github.com/user-attachments/assets/c3f3910d-31a6-4834-95aa-4a64de91b823" width="45%" alt="Print 5" />
  <img src="https://github.com/user-attachments/assets/2f68b2ab-d475-4ce4-a80b-80781791ee58" width="45%" alt="Print 6" />
</div>

---

## 🛠️ Tecnologias Utilizadas

* **Terraform** - Ferramenta de IaC para provisionamento automatizado.
* **AWS (Amazon Web Services)** - Provedor de nuvem.
* **Git/GitHub** - Controle de versão e documentação.

## 📁 Estrutura de Arquivos

```text
networking/
├── vpc.tf                # Criação da rede principal
├── vpc_public_subnet.tf  # Subnets com acesso à internet
├── vpc_private_subnet.tf # Subnets isoladas
├── internet_gateway.tf   # Conexão com a internet
├── vpc_nat_gateway.tf    # Saída segura para subnets privadas
├── route_table.tf        # Definição das rotas
├── variables.tf          # Variáveis globais
└── main.tf               # Configuração do Provider e Backend



