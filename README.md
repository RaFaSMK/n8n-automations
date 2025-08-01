# 🤖 Agente de IA Integrado com Web e WhatsApp

Este repositório contém dois projetos complementares de automação com inteligência artificial utilizando Groq (LLaMA3), n8n, Google Sheets e integrações via API.

A proposta é criar agentes inteligentes que interagem com usuários através de diferentes canais (web e WhatsApp), registram as interações como leads e utilizam ferramentas auxiliares como calculadora e Wikipedia para enriquecer as respostas.

---

## 📁 Estrutura do Projeto

### 🔹 `web-agent/`
Agente conversacional com interface web.  
📌 Principais funcionalidades:
- Interface web de teste com entrada de usuário.
- Integração com IA via **Groq API (LLaMA3)**.
- Registra todas as perguntas no **Google Sheets** com ID de conversa.
- Memória simples com até 5 janelas de contexto.
- Uso de ferramentas (Wikipedia, calculadora).
- Tratamento de entrada para evitar ruído nos registros e na IA.

### 🔹 `whatsapp-agent/`
Agente de IA integrado ao WhatsApp via **Z-API**.  
📌 Principais funcionalidades:
- Recebe mensagens do WhatsApp por webhook.
- Filtra mensagens de grupo, newsletter e broadcast.
- Registra **leads qualificados** no **Google Sheets**.
- Envia a resposta da IA de volta ao WhatsApp utilizando **n8n**.
- Mesma IA e memória do `web-agent`.

---

## 🧰 Tecnologias Utilizadas

- 🤖 **Groq API** com modelo **LLaMA3** para respostas da IA
- 🔗 **Z-API** para integração com WhatsApp
- 📊 **Google Sheets API** para registro de leads e perguntas
- 🔄 **n8n** para orquestração de fluxos e automações
- 🌐 **Webhook & HTTP Requests** para integração entre serviços

---

## 🧪 Objetivos do Projeto

- Criar agentes inteligentes multiplataforma com registros persistentes.
- Automatizar atendimento e captação de leads de forma inteligente.
- Explorar o uso de IA em aplicações reais com conectividade e memória.

---

## 📌 Próximos Passos

- Melhorar o gerenciamento da memória da IA.
- Implementar painel de visualização dos dados registrados.
- Explorar envio de mensagens proativas no WhatsApp.

---

## 📂 Como Executar

Cada subpasta possui seu próprio `README.md` com instruções específicas de instalação, configuração e execução.

---

## 📬 Contato

Quer saber mais ou colaborar?  
Entre em contato por aqui mesmo no GitHub ou [LinkedIn](https://www.linkedin.com/in/rafael-chaves-souza-a856b524b/).

---
