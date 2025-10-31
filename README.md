# Gerenciamento de Instâncias EC2 na AWS

## Sobre o Projeto
Este repositório documenta minha experiência prática no gerenciamento de instâncias EC2 na AWS. Durante este projeto, realizei a criação, configuração e testes de instâncias, registrando aprendizados e boas práticas adquiridas ao longo do processo.

## Objetivos
- Entender e aplicar conceitos de criação e gerenciamento de instâncias EC2.
- Registrar passo a passo das atividades realizadas para estudo e consulta futura.
- Organizar scripts e comandos úteis para facilitar reuso em outros projetos.

## Estrutura do Repositório
- `README.md`: documentação detalhada do projeto.
- `/scripts` (opcional): scripts utilizados durante a configuração das instâncias.
- `notas.md`: anotações pessoais sobre aprendizados, problemas enfrentados e soluções aplicadas.

## Passo a Passo Realizado

### 1. Acesso ao Console AWS
- Entrei no [Console da AWS](https://aws.amazon.com/console/).
- Naveguei até o serviço **EC2** para iniciar a criação da instância.

### 2. Criação da Instância EC2
- Escolhi a **AMI Amazon Linux 2** por ser compatível com os testes que eu queria realizar.
- Selecionado o tipo de instância **t2.micro**, adequado para testes gratuitos.
- Configurei a **chave SSH** para permitir acesso seguro à máquina.
- Ajustei os **Security Groups** para liberar portas essenciais:
  - 22 → SSH  
  - 80 → HTTP

### 3. Conexão à Instância
- Conectei à instância usando o terminal:
```bash
ssh -i "minha_chave.pem" ec2-user@<IP-da-instancia>
