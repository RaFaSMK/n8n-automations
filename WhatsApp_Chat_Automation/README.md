# 🤖 Agente de IA para WhatsApp com Registro de Leads

Este projeto é um agente inteligente integrado ao **WhatsApp** via **Z-API**, com registro automático de leads em **Google Sheets** e processamento inteligente de mensagens. Ele utiliza um **webhook** para escutar mensagens recebidas, faz o tratamento dos dados e responde utilizando um **modelo de IA hospedado na Groq (LLaMA 3)**. A comunicação com o WhatsApp é feita por meio de chamadas POST utilizando o **n8n**, nessas fotos foi utilizado meu próprio número para testes.

## 📌 Funcionalidades

- ✅ Integração com WhatsApp via **Z-API**
- ✅ Registro automático de leads (clientes em potencial) em **Google Sheets**
- ✅ Filtro automático de mensagens: ignora grupos, newsletters e broadcasts
- ✅ **Memória de contexto simples (janela de até 5 interações)** por usuário
- ✅ Respostas automáticas com IA via **Groq (modelo LLaMA 3)**
- ✅ Uso de ferramentas auxiliares (Wikipedia e Calculadora) conforme o tipo de pergunta
- ✅ Tratamento inteligente das mensagens para enviar apenas o necessário ao Google Sheets e ao modelo de IA
- ✅ Utiliza **n8n** para orquestrar o envio de mensagens do agente de volta ao WhatsApp

## 🛠 Tecnologias Utilizadas

- [Z-API](https://www.z-api.io/) – Integração com WhatsApp
- [n8n](https://n8n.io/) – Orquestração de fluxo e requisições HTTP
- [Google Sheets API](https://developers.google.com/sheets/api) – Armazenamento dos leads
- [Groq API](https://groq.com/) – Execução do modelo LLaMA 3
- [LLaMA 3](https://ai.meta.com/llama/) – Modelo de linguagem natural
- [Wikipedia API](https://www.mediawiki.org/wiki/API:Main_page) – Consulta de informações gerais
- Operações matemáticas via ferramenta de calculadora customizada
- Webhooks e filtros em Python/JavaScript (dependendo da implementação)

## 🔄 Fluxo do Sistema

1. Usuário envia mensagem no WhatsApp
2. Webhook do Z-API recebe a mensagem e envia via POST para o n8n
3. n8n verifica se é uma mensagem válida (exclui grupos, newsletters e broadcasts)
4. A mensagem é tratada (removendo excesso de informação)
5. A IA responde usando a Groq (LLaMA 3)
6. A resposta da IA é enviada de volta ao WhatsApp via POST do n8n → Z-API
7. Informações relevantes da conversa (ID, mensagem, resposta, timestamp) são registradas no Google Sheets

## 🧪 Testes

A aplicação pode ser testada por meio de um site específico (ou ambiente de staging) configurado para simular as interações via WhatsApp.