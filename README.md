📌 Sobre o projeto.

Este laboratório teve como objetivo realizar o diagnóstico de um problema de conectividade em uma infraestrutura na AWS, envolvendo uma instância EC2, configuração de rede e serviço Apache.

O cenário simula uma situação de suporte técnico em que uma aplicação web não estava acessível após a criação de um servidor.

🎯 Objetivos

Investigar falhas de conectividade.

Verificar o funcionamento do serviço Apache.

Utilizar comandos Linux para diagnóstico.

Analisar componentes de rede da AWS.

Verificar configurações de VPC, Subnet, Route Table e Security Groups.

🛠️ Tecnologias utilizadas

Tecnologia

Utilização

AWS

Infraestrutura em nuvem

EC2

Instância de computação

VPC

Rede virtual

Amazon Linux

Sistema operacional

Apache

Servidor web

SSH

Acesso remoto

HTTP

Acesso à aplicação

🖥️ 1. Arquitetura da infraestrutura

A infraestrutura do laboratório utiliza uma VPC, Internet Gateway, subnet pública e uma instância EC2.

<img width="1240" height="478" alt="image" src="https://github.com/user-attachments/assets/3ec92b69-c287-4c88-b196-1a4982495cd3" />


Insira aqui a imagem da arquitetura:



🔐 2. Acesso à instância EC2 via SSH

Foi realizado o acesso remoto à instância EC2 utilizando SSH para executar os comandos de diagnóstico.

<img width="1325" height="491" alt="image" src="https://github.com/user-attachments/assets/42cfef22-e60d-432a-96ca-cea705bb40d4" />


Insira aqui a captura de tela do acesso SSH:



🔎 3. Verificação do serviço Apache

Inicialmente, foi verificado o status do serviço Apache utilizando:

sudo systemctl status httpd.service

O serviço foi identificado como inativo.

<img width="1645" height="933" alt="image" src="https://github.com/user-attachments/assets/64d42154-cd14-479c-b9d1-eb2a890c72bc" />


Inicialização do serviço

Para iniciar o Apache, foi utilizado:

sudo systemctl start httpd.service

Em seguida, foi realizada uma nova verificação:

sudo systemctl status httpd.service

<img width="1358" height="641" alt="image" src="https://github.com/user-attachments/assets/22fe897b-bfa9-48be-a2a8-32eca0ed63c6" />


🌐 4. Análise dos componentes de rede da AWS

Durante o diagnóstico, foram analisados os seguintes componentes:

VPC: rede virtual utilizada pela infraestrutura.

Subnet: associação da instância à sub-rede.

Route Table: verificação das rotas configuradas.

Internet Gateway: verificação da associação com a VPC.

Security Groups: análise das regras de entrada e saída.

Network ACLs: verificação das regras de controle de tráfego.

📷 Imagem 5 – Configuração da VPC e componentes de rede

<img width="1717" height="506" alt="image" src="https://github.com/user-attachments/assets/54a0b57d-96a1-4a2a-8c44-817dbf945e1e" />

Realizado edição no grupo de segurança adicionando HTTP e HTTPS

🌍 5. Teste de acesso ao servidor web

Após iniciar o Apache, foi realizado o teste de acesso pelo navegador utilizando o endereço IP público da instância:

http://44.251.16.210/

<img width="1867" height="844" alt="image" src="https://github.com/user-attachments/assets/d0a6dd97-78dd-4618-a6df-de44735169be" />

📚 Conhecimentos desenvolvidos

Durante a atividade, foram praticados conhecimentos relacionados a:

Diagnóstico de conectividade em ambientes AWS.

Administração básica de serviços Linux.

Gerenciamento de instâncias EC2.

Análise de infraestrutura de rede.

Verificação de regras de segurança.

Troubleshooting de aplicações web.

✅ Conclusão

O laboratório permitiu praticar uma rotina de troubleshooting em ambiente de nuvem, envolvendo análise de conectividade, verificação de serviços Linux e investigação dos componentes de rede da AWS.

A atividade reforçou a importância de realizar testes por etapas para identificar possíveis pontos de falha em uma infraestrutura.

📁 Estrutura do repositório

troubleshooting-rede-aws/
│
├── README.md
│
└── images/
    ├── 01-arquitetura-vpc.png
    ├── 02-conexao-ssh.png
    ├── 03-apache-inativo.png
    ├── 04-apache-ativo.png
    ├── 05-configuracao-vpc.png
    └── 06-pagina-apache.png

Observação: substitua as imagens pelos seus próprios prints do laboratório. O material original não informa uma causa raiz específica para a falha, portanto ela não foi presumida neste README.
