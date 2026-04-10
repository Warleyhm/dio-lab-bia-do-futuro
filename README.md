# 💸 FinAI — Educador Financeiro com IA Generativa

> Agente inteligente de educação financeira desenvolvido como projeto final do **Bootcamp Bradesco GenAI & Dados** (DIO), inspirado na BIA, assistente virtual do Bradesco.

---

## 🎯 Sobre o Projeto

O **FinAI** é um agente conversacional proativo que atua como educador financeiro pessoal. Ele não apenas responde perguntas — antecipa necessidades, personaliza orientações com base no perfil do usuário e co-cria planos financeiros de forma consultiva e segura.

**Problema resolvido:** Pessoas que querem organizar suas finanças mas não sabem por onde começar, encontrando nas ferramentas tradicionais algo complexo e pouco personalizado.

---

## 🤖 O Agente

| Atributo | Descrição |
|---|---|
| **Nome** | FinAI |
| **Papel** | Educador e consultor financeiro pessoal |
| **Tom de voz** | Didático, empático e direto — sem jargões desnecessários |
| **Foco** | Educação financeira, metas de economia e análise de gastos |
| **Anti-alucinação** | Respostas baseadas exclusivamente na base de conhecimento e dados do usuário |

---

## 🗂️ Estrutura do Repositório

```
📁 dio-lab-bia-do-futuro/
│
├── 📄 README.md
│
├── 📁 data/                          # Base de conhecimento (dados mockados)
│   ├── transacoes.csv                # Histórico de transações
│   ├── historico_atendimento.csv     # Histórico de atendimentos
│   ├── perfil_investidor.json        # Perfil e preferências do cliente
│   └── produtos_financeiros.json     # Produtos e serviços disponíveis
│
├── 📁 docs/                          # Documentação completa do agente
│   ├── 01-documentacao-agente.md     # Caso de uso e arquitetura
│   ├── 02-base-conhecimento.md       # Estratégia de dados
│   ├── 03-prompts.md                 # Engenharia de prompts
│   ├── 04-metricas.md                # Avaliação e métricas
│   └── 05-pitch.md                   # Roteiro do pitch
│
├── 📁 src/                           # Código da aplicação
│   └── app.py                        # Chatbot interativo (Streamlit)
│
└── 📁 assets/                        # Imagens e diagramas
```

---

## 🧠 Arquitetura

```
Usuário → Interface (Streamlit) → System Prompt + Dados do Perfil
                                          ↓
                                    LLM (via API)
                                          ↓
                          Base de Conhecimento (CSV + JSON)
                                          ↓
                              Resposta personalizada e segura
```

---

## 📋 Documentação

| Documento | Conteúdo |
|---|---|
| [`01-documentacao-agente.md`](docs/01-documentacao-agente.md) | Caso de uso, persona e arquitetura |
| [`02-base-conhecimento.md`](docs/02-base-conhecimento.md) | Estratégia de dados e fontes |
| [`03-prompts.md`](docs/03-prompts.md) | System prompt e exemplos de interação |
| [`04-metricas.md`](docs/04-metricas.md) | Métricas de qualidade e avaliação |
| [`05-pitch.md`](docs/05-pitch.md) | Roteiro do pitch de 3 minutos |

---


## 🛠️ Tecnologias

- **LLM:** API de IA Generativa (Claude / OpenAI / Gemini)
- **Interface:** Streamlit
- **Dados:** CSV e JSON mockados
- **Orquestração:** LangChain

---

## 📊 Métricas de Qualidade

- ✅ Assertividade das respostas financeiras
- ✅ Taxa de respostas seguras (sem alucinações)
- ✅ Coerência com o perfil do investidor
- ✅ Satisfação simulada do usuário

---

## 🏦 Contexto

Projeto desenvolvido no **Bootcamp Bradesco GenAI & Dados** em parceria com a [DIO](https://dio.me), com foco em IA Generativa aplicada ao mercado financeiro, inspirado na BIA — assistente virtual do Bradesco.

---
