# 🏛️ Cognitios POST

![Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen)
![Stack](https://img.shields.io/badge/Stack-n8n%20%7C%20Gemini%20%7C%20Google%20Sheets-blue)

**Cognitios POST** é uma solução avançada de engenharia de confiabilidade (SRE) projetada para transformar logs esparsos e mensagens de incidentes em relatórios de **Postmortem** estruturados, factuais e auditáveis em tempo recorde.

## 📋 O Desafio Operacional
Antes da implementação deste sistema, o processo de documentação de incidentes críticos apresentava gargalos significativos de eficiência:
* **Lead Time Crítico**: A entrega do relatório final demorava entre 2 a 3 semanas após a resolução do incidente.
* **Esforço Duplicado**: Exigia-se que analistas dedicassem horas diárias à busca manual e correlação de evidências.
* **Processo Sequencial**: A natureza lenta do fluxo manual impedia a rápida disseminação do conhecimento preventivo na organização.

## 📉 Impacto e Resultados (ROI)
A transição para o modelo automatizado gerou ganhos exponenciais de agilidade:

| Métrica | Processo Manual | Cognitios POST | Ganho Real |
| :--- | :--- | :--- | :--- |
| **Tempo de Entrega** | 2 - 3 Semanas | **1 Dia (Minutos)** | **-92% de Tempo** |
| **Disponibilidade** | Baixa | **Alta** | **Decisões Rápidas** |
| **Status do Processo** | Lento / Sequencial | **Ágil / Paralelo** | **Fim do Backlog** |

---

## 🛠️ Arquitetura dos Workflows (n8n)

O ecossistema é composto por cinco micro-serviços interconectados que garantem a integridade dos dados e a automação do ciclo de vida do incidente:

### 1. Ingestão em Tempo Real (Chat de Incidente)
Interface para que analistas registrem eventos durante a crise.
* **Inteligência**: O Gemini categoriza eventos (Alerta, Ação, Evidência ou Decisão) e reformula o texto para um tom profissional.
* **Armazenamento**: Dados validados via código JavaScript são inseridos automaticamente na planilha de controle.

* <img width="1500" height="488" alt="Captura de tela 2026-02-11 145703" src="https://github.com/user-attachments/assets/749db4b0-bdd8-4d81-bc2e-a580de2eefe3" />


### 2. Motor Central de Processamento (Relatório Final)
O "cérebro" que consolida logs e gera o documento final no Google Docs.
* **Análise de IA**: O Gemini realiza a análise de Postmortem baseada estritamente em evidências, eliminando alucinações.
* **Processamento Paralelo**: A resposta da IA é dividida em quatro ramos paralelos para extrair tópicos específicos (Causa Raiz, Lições Aprendidas, etc.) com precisão máxima.

* <img width="1271" height="353" alt="Captura de tela 2026-02-11 145718" src="https://github.com/user-attachments/assets/2540669e-d91d-4144-8fc9-041bfae9f2ef" />


### 3. Ingestão de Dados em Lote (Upload de Logs)
Processamento de arquivos de texto longos (.txt) para reconstrução de timelines.
* **ETL Inteligente**: Transforma logs não estruturados em um array JSON organizado através de análise sintática da IA.

* <img width="1444" height="331" alt="Captura de tela 2026-02-11 145736" src="https://github.com/user-attachments/assets/3cc0cae3-7bf4-4230-ba7f-1f8766f60dc8" />


### 4. Manutenção de Sistema (Cleanup)
Utilitário para resetar o ambiente entre incidentes.
* **Ação**: Limpa os intervalos de dados temporários preservando a estrutura da planilha de staging.

* <img width="855" height="407" alt="Captura de tela 2026-02-11 145755" src="https://github.com/user-attachments/assets/d8ef3fc3-e42d-4c94-b022-3b4eecae877d" />


### 5. Interface de Controle (Dashboard HTML)
Frontend unificado para operação do sistema.
* **GUI**: Centraliza botões de ação para abrir chat, realizar uploads, gerar relatórios e limpar dados.

* <img width="960" height="344" alt="Captura de tela 2026-02-11 145649" src="https://github.com/user-attachments/assets/f139d60f-837e-4f02-ae83-34c23a38dc2a" />


---

## 🛠️ Tecnologias Utilizadas
* **n8n**: Orquestrador de workflows e integração de APIs.
* **Google Gemini API**: Inteligência generativa para síntese técnica e estruturação de dados.
* **Google Sheets & Docs**: Repositório de dados e exportação de documentos finais.
* **Tailwind CSS**: Estilização do painel de controle para os analistas.

## 🧠 Filosofia do Projeto
O nome **Cognitios POST** reflete a transição da incerteza para o entendimento. Ao automatizar a carga cognitiva da coleta de logs, permitimos que a equipe de SRE foque no que realmente importa: a **Engenharia de Resiliência**.

---
