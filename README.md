# Gerenciamento de Instâncias EC2 - AWS

## Descrição do Projeto
Este repositório contém anotações e práticas realizadas para o gerenciamento de instâncias EC2 na AWS. O objetivo é consolidar o conhecimento adquirido durante as aulas, documentando processos, insights e boas práticas.

## Objetivos do Projeto
- Aplicar conceitos de criação, configuração e gerenciamento de instâncias EC2.
- Documentar processos técnicos de forma clara e organizada.
- Utilizar GitHub como ferramenta para armazenamento e compartilhamento do conhecimento.

## Estrutura do Repositório
- `README.md`: documentação detalhada do projeto.
- `/images`: capturas de tela relevantes das atividades.
- `/scripts` (opcional): scripts utilizados para configuração da instância.
- `notas.txt` ou `anotacoes.md`: observações e aprendizados.

## Passo a Passo Realizado
1. **Acesso à AWS**
   - Entrar no [Console da AWS](https://aws.amazon.com/console/).
   - Navegar até o serviço **EC2**.

2. **Criação da Instância EC2**
   - Selecionar uma **AMI** (Amazon Machine Image), por exemplo, Amazon Linux 2.
   - Escolher o **tipo de instância**, como t2.micro.
   - Configurar **chaves SSH** para acesso seguro.
   - Configurar **Security Groups** para liberar portas necessárias (22 para SSH, 80 para HTTP).

3. **Conexão à Instância**
   - Acessar a instância via SSH usando o terminal ou PuTTY:
     ```bash
     ssh -i "chave.pem" ec2-user@<IP-da-instancia>
     ```

4. **Configuração e Testes**
   - Instalar pacotes necessários:
     ```bash
     sudo yum update -y
     sudo yum install httpd -y
     ```
   - Iniciar serviços, por exemplo:
     ```bash
     sudo systemctl start httpd
     sudo systemctl enable httpd
     ```
   - Verificar status:
     ```bash
     sudo systemctl status httpd
     ```

5. **Documentação**
   - Capturar prints de tela da criação da instância, configuração de Security Groups e testes.
   - Organizar as imagens na pasta `/images`.

6. **Upload para GitHub**
   - Inicializar o repositório local:
     ```bash
     git init
     git add .
     git commit -m "Primeiro commit - documentação do EC2"
     git branch -M main
     git remote add origin <URL-do-repositorio>
     git push -u origin main
     ```

## Aprendizados e Insights
- A importância de configurar **Security Groups** corretamente.
- Boas práticas de organização e documentação de projetos na AWS.
- Experiência prática com SSH e gestão de instâncias EC2.

## Autor
Joziane - [Perfil GitHub](https://github.com/jozi95)

