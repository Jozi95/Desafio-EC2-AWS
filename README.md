# Gerenciamento de Instâncias EC2 - AWS

## Descrição do Projeto
Este repositório contém anotações, práticas e scripts realizados para o gerenciamento de instâncias EC2 na AWS. O objetivo é consolidar o conhecimento adquirido durante as aulas, documentando processos, insights e boas práticas.

## Objetivos do Projeto
- Aplicar conceitos de criação, configuração e gerenciamento de instâncias EC2.
- Documentar processos técnicos de forma clara e organizada.
- Utilizar GitHub como ferramenta para armazenamento e compartilhamento do conhecimento.

## Estrutura do Repositório
- `README.md`: documentação detalhada do projeto.
- `/images`: capturas de tela relevantes das atividades.
  - `criacao_ec2.png`
  - `security_group.png`
  - `teste_http.png`
- `/scripts`: scripts utilizados para configuração da instância.
  - `instalar_httpd.sh`
- `notas.md`: observações e aprendizados durante a prática.

## Passo a Passo Realizado

### 1. Acesso à AWS
- Entrar no [Console da AWS](https://aws.amazon.com/console/).
- Navegar até o serviço **EC2**.

### 2. Criação da Instância EC2
- Selecionar uma **AMI** (Amazon Machine Image), por exemplo, Amazon Linux 2.
- Escolher o **tipo de instância**, como t2.micro.
- Configurar **chaves SSH** para acesso seguro.
- Configurar **Security Groups** para liberar portas necessárias (22 para SSH, 80 para HTTP).

### 3. Conexão à Instância
- Acessar a instância via SSH:
```bash
ssh -i "chave.pem" ec2-user@<IP-da-instancia>




