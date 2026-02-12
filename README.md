# 🏛️ Cognitios POST

![Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen)
![Stack](https://img.shields.io/badge/Stack-n8n%20%7C%20Gemini%20%7C%20Google%20Sheets-blue)

O **Cognitios POST** é um framework conceitual de automação para Engenharia de Confiabilidade (**SRE**) focado na resolução do "toil" (trabalho repetitivo) durante a documentação técnica. O projeto demonstra como integrar orquestração de workflows e Inteligência Artificial Generativa para transformar fluxos de dados não estruturados em relatórios de incidentes coesos e factuais.

## 💡 O Conceito
A documentação de incidentes (Postmortems) frequentemente sofre com a dispersão de evidências em diferentes canais. O **Cognitios POST** propõe uma arquitetura onde a coleta, a categorização e a síntese desses dados ocorrem de forma automatizada, permitindo que o foco humano se desloque da compilação de logs para a análise estratégica de causa raiz.

---

## 🛠️ Arquitetura Técnica (Workflows n8n)

A solução é composta por micro-serviços independentes que operam de forma modular:

### 1. Ingestão Inteligente em Tempo Real
Interface de chat projetada para capturar inputs humanos e convertê-los instantaneamente em dados estruturados.
* [cite_start]**Processamento**: Utiliza LLM (Gemini) para classificar o input em categorias como Alerta, Ação, Evidência ou Decisão[cite: 13, 14].
* [cite_start]**Persistência**: Sanitização via JavaScript e armazenamento em banco de dados de staging (Google Sheets)[cite: 13].

<img width="1000" alt="Workflow de Ingestão" src="https://github.com/user-attachments/assets/749db4b0-bdd8-4d81-bc2e-a580de2eefe3" />

### 2. Motor de Síntese e Relatório
O núcleo de processamento responsável pela análise semântica das evidências acumuladas.
* [cite_start]**Fidelidade Factual**: Camadas de controle via Prompt Engineering que restringem a IA apenas aos logs fornecidos, eliminando alucinações[cite: 11, 15].
* [cite_start]**Arquitetura Paralela**: Segmentação do processamento em ramos simultâneos para extração de tópicos específicos, garantindo precisão na montagem do documento final[cite: 11].

<img width="1000" alt="Motor de Processamento" src="https://github.com/user-attachments/assets/2540669e-d91d-4144-8fc9-041bfae9f2ef" />

### 3. Processamento de Dados em Lote (ETL)
Módulo especializado na ingestão de arquivos de texto volumosos para reconstrução retroativa de timelines.
* [cite_start]**Parser Inteligente**: Identifica padrões cronológicos e responsáveis em logs brutos e exportações de chats[cite: 10].

<img width="1000" alt="Processamento em Lote" src="https://github.com/user-attachments/assets/3cc0cae3-7bf4-4230-ba7f-1f8766f60dc8" />

### 4. Interface Operacional (GUI)
Um dashboard desenvolvido em HTML5 e Tailwind CSS que abstrai a complexidade do backend.
* [cite_start]**UX Centralizada**: Permite o acionamento de todos os módulos (Chat, Upload, Geração e Limpeza) através de uma interface unificada[cite: 16].

<img width="1000" alt="Dashboard de Controle" src="https://github.com/user-attachments/assets/f139d60f-837e-4f02-ae83-34c23a38dc2a" />

---

## 🚀 Tecnologias Utilizadas
* **Orquestração**: n8n.
* **Inteligência Artificial**: Google Gemini API.
* **Frontend**: HTML5, Tailwind CSS, Lucide Icons.
* **Dados e Documentação**: Google Workspace APIs (Sheets & Docs).

## 🧠 Visão do Projeto
Este repositório serve como uma **Prova de Conceito (PoC)** para demonstrar como a automação de baixo código (low-code) combinada com LLMs pode elevar a maturidade de processos de SRE, reduzindo a carga cognitiva e aumentando a agilidade na entrega de documentação técnica de alta qualidade.

---
> [!NOTE]
> Este projeto é uma iniciativa de estudo pessoal. Todos os dados, fluxos e identificadores aqui apresentados foram higienizados para fins de demonstração acadêmica e profissional.
