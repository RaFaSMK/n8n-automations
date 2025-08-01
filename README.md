# 🤖 Agente Conversacional com Memória + Logging no Google Sheets

Este projeto é um chatbot web com um agente de IA pelo n8n, com funcionalidades de logging inteligente e ferramentas externas para expandir suas capacidades de resposta.

---

## 📌 Funcionalidades Principais

- 🔗 **Acesso via Web**: Interface amigável hospedada para testes com usuários.
- 🧠 **Memória Conversacional**: Janela de contexto simples com até **5 interações anteriores**, preservando coerência nas respostas.
- 📊 **Registro no Google Sheets**:
  - Armazena **ID da conversa**
  - **Perguntas dos usuários**
  - Dados são processados e tratados antes do envio
- ⚙️ **Agente de IA**: Utiliza a API do **Groq** como motor de IA **llama3** para geração de respostas.
- 🛠️ **Ferramentas Integradas**:
  - 📚 **Wikipedia** (busca contextual)
  - 🧮 **Calculadora** (resolução de cálculos matemáticos simples e expressões)
- 🧼 **Tratamento Inteligente de Input**: Apenas o conteúdo relevante da mensagem do usuário é enviado ao Groq e ao Google Sheets, garantindo performance e precisão.

---

## 🚀 Tecnologias Utilizadas

| Tecnologia         | Uso principal                                   |
|--------------------|-------------------------------------------------|
| **n8n**            | Automação e orquestração dos fluxos             |
| **Groq API**       | Infraestrutura de execução de modelos LLM com baixa latência |
| **Meta Llama3**    | Modelo de linguagem natural utilizado via Groq  |
| **Google Sheets**  | Registro estruturado das interações             |
| **Wikipedia API**  | Resposta baseada em conhecimento enciclopédico  |

---

## 🧪 Como Testar

1. Acesse: [Site para chat](https://rafasmk.app.n8n.cloud/webhook/ec50bd9b-b964-4c9b-8f68-bb9f888cffc9/chat).
2. Inicie uma conversa normalmente.
3. Veja o log sendo atualizado em tempo real no [Google Sheets](https://docs.google.com/spreadsheets/d/16VXrE-U-CLz8WJoIyLyI6pA5ftJFO2RnPM1_cZn-3hI/edit?usp=sharing) .
4. Faça perguntas como:
   - "Qual é a capital da França?" → Wikipedia
   - "Quanto é 45*3?" → Calculadora
   - "Como posso usar IA na minha empresa?" → Groq responde com contexto e memória.

---

## 🗃️ Estrutura do Projeto

