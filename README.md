# alura-prometheus-grafana

Este repositório contém o projeto desenvolvido durante o curso "Monitoramento: Prometheus, Grafana e Alertmanager" da Alura. O objetivo é demonstrar como monitorar uma aplicação Java Spring Boot utilizando Prometheus e Grafana, além de configurar alertas com o Alertmanager.

## Estrutura do Projeto

- **app/**: Código-fonte da aplicação Spring Boot a ser monitorada.
- **prometheus/**: Configurações do servidor Prometheus para coleta de métricas.
- **grafana/**: Configurações do Grafana para visualização das métricas coletadas.
- **alertmanager/**: Configurações do Alertmanager para gerenciamento de alertas.
- **nginx/**: Configurações do Nginx para balanceamento de carga ou proxy reverso.
- **mysql/**: Configurações do banco de dados MySQL utilizado pela aplicação.
- **client/**: Simulador de chamadas para gerar métricas na aplicação.
- **docker-compose.yaml**: Arquivo para orquestração dos serviços via Docker Compose.

## Tecnologias Utilizadas

- **Prometheus**: Sistema de monitoramento e alerta.
- **Grafana**: Plataforma de visualização de métricas.
- **Alertmanager**: Gerenciador de alertas integrado ao Prometheus.
- **Spring Boot**: Framework Java para construção da aplicação monitorada.
- **Docker**: Plataforma para criação e gerenciamento de containers.
- **Nginx**: Servidor web e proxy reverso.
- **MySQL**: Sistema de gerenciamento de banco de dados relacional.

## Instruções para Execução

1. Certifique-se de ter o Docker e o Docker Compose instalados em sua máquina.
2. Clone este repositório:
   ```bash
   git clone https://github.com/moraesv/alura-prometheus-grafana.git
   ```
3. Navegue até o diretório do projeto:
   ```bash
   cd alura-prometheus-grafana
   ```
4. Inicie os serviços com o Docker Compose:
   ```bash
   docker-compose up -d
   ```
5. Acesse o Grafana através do navegador no endereço `http://localhost:3000` e faça login com as credenciais padrão (`admin`/`admin`).
6. Configure o Prometheus como fonte de dados no Grafana e importe os dashboards desejados.

## Conceitos Relacionados

- **SRE (Site Reliability Engineering)**: Disciplina que aplica princípios de engenharia para garantir que sistemas de software sejam altamente confiáveis e escaláveis.
- **SLI (Service Level Indicator)**: Métrica que indica o nível real de desempenho de um serviço.
- **SLO (Service Level Objective)**: Objetivo específico de desempenho que um serviço deve atingir, baseado nos SLIs.
- **SLA (Service Level Agreement)**: Acordo formal entre um provedor de serviço e o cliente, definindo os níveis de serviço esperados e as consequências caso não sejam atingidos.
- **Alertas**: Notificações geradas quando métricas monitoradas ultrapassam limites pré-definidos, indicando possíveis problemas que necessitam de atenção.
- **Aprendizado com Falhas**: Processo de analisar incidentes e falhas para extrair lições e implementar melhorias que previnam ocorrências futuras.
- **Plano de Recuperação e Continuidade**: Estratégias e procedimentos estabelecidos para assegurar a rápida recuperação e continuidade dos serviços após incidentes ou desastres.
- **Engenharia do Caos**: Prática de introduzir falhas controladas em sistemas para testar sua resiliência e identificar pontos fracos antes que ocorram problemas reais.
- **Métricas DORA**: Conjunto de métricas desenvolvidas pelo DevOps Research and Assessment (DORA) para avaliar o desempenho de equipes de desenvolvimento e operações, incluindo frequência de deploys, tempo de recuperação e taxa de falhas.
- **DevOps**: Cultura e conjunto de práticas que promovem a colaboração entre as equipes de desenvolvimento e operações, visando a entrega contínua e eficiente de software de alta qualidade.
- **FinOps**: Conjunto de práticas que combinam finanças e operações para otimizar os custos e o valor dos serviços em nuvem dentro de uma organização.
- **Observabilidade**: Capacidade de um sistema de ser monitorado e compreendido, permitindo a detecção e resolução de problemas de forma eficiente.
- **Monitoramento**: Processo de coleta, análise e visualização de métricas e logs para entender o desempenho e saúde de um sistema.
