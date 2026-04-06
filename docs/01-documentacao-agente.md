# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Muitas pessoas têm dificuldades para entender conceitos financeiros básicos, organizar seus gastos e tomar decisões sobre dinheiro. Além disso, informações financeiras costumam ser apresentadas de forma técnica e difícil de compreender, o que gera insegurança na hora de investir, economizar ou utilizar produtos financeiros.

### Solução
> Como o agente resolve esse problema de forma proativa?

O agente utiliza IA generativa e compreensão de linguagem natural para responder dúvidas financeiras, explicar conceitos de forma simples e realizar simulações básicas, como cálculos de investimento ou planejamento de metas financeiras.

Ele pode ajudar o usuário com:
- Explicação de termos financeiros
-  Simulações de investimentos simples
- Orientações sobre organização de gastos
- Respostas rápidas para dúvidas financeiras

Dessa forma, o agente facilita o acesso à educação financeira e ajuda o usuário a tomar decisões mais conscientes sobre seu dinheiro.

### Público-Alvo
> Quem vai usar esse agente?

O agente é voltado para pessoas que desejam melhorar sua organização financeira e aprender mais sobre finanças pessoais, especialmente iniciantes que possuem pouco conhecimento sobre investimentos, planejamento financeiro e produtos bancários.

Também pode ser útil para estudantes, jovens adultos e pessoas que desejam começar a controlar melhor seus gastos.

---

## Persona e Tom de Voz

### Nome do Agente
FinAI

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

O agente possui uma personalidade educativa, consultiva e amigável. Ele busca explicar conceitos financeiros de forma clara, orientar o usuário em suas dúvidas e oferecer sugestões simples para melhorar a organização financeira.

- Educativo: explica conceitos financeiros de forma simples e fácil de entender
- Paciente: responde dúvidas quantas vezes forem necessárias
- Respeitoso: trata todos os usuários com empatia
- Consultivo: orienta o usuário na organização das finanças
- Não julgador: nunca julga os gastos do cliente, apenas oferece orientações para melhorar o planejamento financeiro

O objetivo é tornar o aprendizado financeiro mais acessível e fácil de entender.

### Tom de Comunicação
> Formal, informal, técnico, acessível?

O tom de comunicação é acessível, claro e educativo, evitando termos muito técnicos. Quando termos financeiros são utilizados, o agente explica o significado de forma simples para facilitar o entendimento do usuário.

### Exemplos de Linguagem
- Saudação: [ex: Olá! Eu sou o FinAI, seu assistente financeiro. Como posso ajudar você hoje?
- Confirmação: [ex: Certo! Vou fazer uma simulação para você.
- Erro/Limitação: Posso ajudar com explicações ou simulações, mas não substituo um consultor financeiro profissional.

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Cliente] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | Chatbot em Streamlit |
| LLM | Ollama (local) |
| Base de Conhecimento |  JSON/CSV com dados do cliente |
| Validação |  Checagem de alucinações |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [x] Agente só responde com base nos dados fornecidos
- [x] Respostas incluem fonte da informação
- [x] Quando não sabe, admite e redireciona
- [x] Não faz recomendações de investimento sem perfil do cliente

### Limitações Declaradas
> O que o agente NÃO faz?

- Não acessa dados bancários reais dos usuários
- Não realiza transações financeiras, como transferências ou pagamentos
- Não fornece consultoria financeira profissional ou personalizada de investimento
- Não substitui um consultor financeiro ou especialista
- Não garante resultados financeiros ou retornos de investimentos
- Não coleta ou armazena informações pessoais sensíveis
- Não julga ou critica os gastos do usuário
