# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

**Data:** 23/04/2026  
**Empresa:** Abstergo Industries  
**Responsável:** Alexandre Ribeiro Vidal

---

## 📋 Introdução

Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por Alexandre Ribeiro Vidal. 
O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar diminuição de custos imediatos.

---

## 📝 Descrição do Projeto

O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:

---

### 🚀 Etapa 1: Amazon EC2 Auto Scaling

| Campo | Descrição |
|-------|-----------|
| **Nome da ferramenta** | Amazon EC2 Auto Scaling |
| **Foco da ferramenta** | Escalabilidade horizontal e gerenciamento de custos computacionais |
| **Descrição de caso de uso** | A indústria farmacêutica lida com cargas de trabalho extremamente variáveis, como processamento em lote durante a noite e picos de acesso a sistemas internos em horário comercial. Utilizando o EC2 Auto Scaling no modo "Scaling Dinâmico" (conforme página 32 do anexo AWS.pdf), a Abstergo Industries substituirá a necessidade de manter uma frota de servidores parados aguardando a carga máxima. O serviço ajustará automaticamente a quantidade de instâncias EC2 conforme a demanda real de processamento de dados laboratoriais. Isso elimina o custo fixo de superdimensionamento ("escalar para capacidade total") e mitiga riscos de falha ao substituir instâncias não íntegras automaticamente. |

---

### 💾 Etapa 2: Amazon S3 (Simple Storage Service)

| Campo | Descrição |
|-------|-----------|
| **Nome da ferramenta** | Amazon S3 (Simple Storage Service) |
| **Foco da ferramenta** | Armazenamento de objetos com classificação inteligente de dados (Ciclo de Vida) |
| **Descrição de caso de uso** | Para atender às rigorosas exigências de conformidade legal do setor farmacêutico (que obrigam a retenção de dados de pesquisas clínicas por 7 a 10 anos), será implementado o Amazon S3 com a estratégia de classes de armazenamento (páginas 41-51 do AWS3.pdf). Dados recentes de experimentos, que exigem alta frequência de acesso, permanecerão no S3 Standard. Após 90 dias sem acesso, os dados serão migrados automaticamente para o S3 Glacier Deep Archive, uma camada de armazenamento de custo extremamente baixo, ideal para preservação digital de longo prazo. Essa transição reduz imediatamente os custos de retenção sem violar as políticas de imutabilidade exigidas por órgãos reguladores como a ANVISA. |

---

### ⚡ Etapa 3: AWS Lambda

| Campo | Descrição |
|-------|-----------|
| **Nome da ferramenta** | AWS Lambda |
| **Foco da ferramenta** | Computação sem servidor (Serverless) |
| **Descrição de caso de uso** | Diversos processos internos da farmacêutica, como a validação de documentos de qualidade, conversão de relatórios em PDF ou disparo de alertas de temperatura em freezers de armazenamento, não precisam de um servidor 24 horas por dia funcionando. Conforme a descrição de Computação sem Servidor (página 45 do AWS.pdf), o AWS Lambda permite executar código sob demanda, sem provisionar ou gerenciar servidores. A empresa pagará apenas pelo tempo de execução do código em milissegundos, em vez de manter uma instância EC2 ligada de forma ininterrupta aguardando um gatilho, resultando em uma drástica redução de custos operacionais para funções esporádicas. |

---

## ✅ Conclusão

A implementação de ferramentas na empresa Abstergo Industries tem como esperado:

-  A eliminação de gastos com capacidade ociosa de servidores;
-  A redução do custo de armazenamento de dados legados ao mover informações não acessadas para camadas de arquivamento frio;
-  A economia com infraestrutura ociosa em processos esporádicos;

o que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.

---

## 📎 Anexos

| # | Documento | Descrição |
|---|-----------|-----------|
| 1 | `TCO_Analise.xlsx` | Planilha de Cálculo de TCO (Total Cost of Ownership) comparando Data Center físico vs. Cloud AWS |

---

**Assinatura do Responsável pelo Projeto:**

> *Alexandre Ribeiro Vidal*

---

<div align="center">

📊 **Abstergo Industries © 2026** — Todos os direitos reservados

</div>
