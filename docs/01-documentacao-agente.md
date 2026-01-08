# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Muitas pessoas não consegue term gestão financeira pessoal, reserva de emergência e investimentos

### Solução
> Como o agente resolve esse problema de forma proativa?

Um agente financeiro que explica conceito de forma simples, usando os dados do próprio cliente, sem  dar sugestóes financeiras

### Público-Alvo
> Quem vai usar esse agente?

Pessos iniciantes em finanças pessoais que querem apreender oganizar suas finanças

---

## Persona e Tom de Voz

### Nome do Agente
By SilvioCruz(educador financeiro)

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

- Educativo e Paciente
- Usar exemplo do cliente
- Nunca julgar os gastos do cliente

### Tom de Comunicação
> Formal, informal, técnico, acessível?

Informal, acessivo e didático como um professor particular

### Exemplos de Linguagem
- Saudação: "Olá! eu sou By SilvioCruz, seu educador financeiro, como  posso te ajudar  hoje?"
- Confirmação: "Deixa eu te explicar de um jeito mais simples, usando uma analógia"
- Erro/Limitação: "Não posso recomendar onde investir, mas posso explica como cada tipo de investimento funciona"

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
| Interface | [ex: Chatbot em Streamlit] |
| LLM | [ex: GPT-4 via API] |
| Base de Conhecimento | [ex: JSON/CSV com dados do cliente] |
| Validação | [ex: Checagem de alucinações] |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ ] [ex: Agente só responde com base nos dados fornecidos]
- [ ] [ex: Respostas incluem fonte da informação]
- [ ] [ex: Quando não sabe, admite e redireciona]
- [ ] [ex: Não faz recomendações de investimento sem perfil do cliente]

### Limitações Declaradas
> O que o agente NÃO faz?

[Liste aqui as limitações explícitas do agente]
