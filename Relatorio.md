# Redução dos Custos em Farmácias com AWS

## 1. Objetivo
Desenvolver uma solução utilizando serviços da AWS para **reduzir custos operacionais em farmácias**, automatizando processos, otimizando o gerenciamento de estoque e monitorando recursos de forma eficiente.

---

## 2. Descrição do Projeto
A farmácia enfrenta desafios comuns:  
- Custos altos com infraestrutura de TI.  
- Dificuldade em armazenar, processar e analisar dados de estoque, vendas e prescrições.  
- Necessidade de automação em processos repetitivos e geração de relatórios.

A solução proposta inclui:  
- Armazenamento escalável e seguro de dados de vendas e prescrições.  
- Processamento serverless para análise e automação de tarefas.  
- Monitoramento contínuo de recursos e custos.  
- Dashboards interativos para visualização de dados financeiros e de estoque.

---

## 3. Arquitetura da Solução

### Fluxo sugerido:
1. **Entrada de dados**: dados de vendas e prescrições enviados por planilhas ou aplicativo da farmácia.  
2. **Armazenamento de dados**:  
   - **Amazon S3**: armazenamento de dados brutos de forma econômica e escalável.  
3. **Processamento e análise**:  
   - **AWS Lambda**: processa os dados automaticamente, calculando relatórios diários e indicadores de estoque.  
   - **Amazon Comprehend Medical**: identifica padrões de consumo de medicamentos e possíveis excessos de estoque.  
4. **Banco de dados estruturado**:  
   - **Amazon DynamoDB ou RDS**: dados estruturados para consultas rápidas e geração de relatórios.  
5. **Monitoramento e alerta de custos**:  
   - **Amazon CloudWatch**: monitoramento em tempo real dos recursos.  
   - **AWS Budgets / Cost Explorer**: alertas de uso e custos, evitando desperdícios.  
6. **Visualização de dados**:  
   - **Amazon QuickSight**: dashboards interativos com informações de vendas, estoque e custos operacionais.

### Diagrama de Arquitetura
```text
[Entrada de dados: vendas/prescrições] --> [S3] --> [Lambda] --> [DynamoDB/RDS] --> [QuickSight]
                                     |
                                     v
                                [CloudWatch + Budgets]
