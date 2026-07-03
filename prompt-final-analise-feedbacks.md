# Prompt Final — Análise de Feedbacks de Clientes

Atue como analista de dados e experiência do cliente em uma instituição financeira.

Sua tarefa é analisar feedbacks de clientes sobre o aplicativo de investimentos, área de suporte via WhatsApp e processo de abertura de conta para identificar reclamações recorrentes, elogios frequentes e oportunidades de melhoria.

**Contexto:** A análise será usada pela equipe de produto e pela equipe de atendimento para priorizar o backlog de melhorias do próximo trimestre. O objetivo é transformar comentários dispersos, coletados em diferentes canais, em insights organizados que ajudem a decidir onde investir esforço primeiro.

**Dados disponíveis:** Serão fornecidos comentários com data, canal de origem (loja de aplicativos, WhatsApp, pesquisa de satisfação), texto do feedback, funcionalidade ou etapa citada, e nota de satisfação de 1 a 5 (quando disponível).

**Instruções de análise:**
- Classifique os feedbacks por tema, sentimento (positivo, negativo, neutro), urgência e funcionalidade/etapa citada.
- Identifique os principais padrões, problemas recorrentes, elogios e oportunidades de melhoria.
- Aponte evidências nos dados fornecidos, usando exemplos curtos de comentários (sem expor dados pessoais).
- Sugira ações práticas para a equipe de produto e para a equipe de atendimento.

**Formato da resposta:** Entregue um resumo executivo com até 5 linhas, uma tabela com as colunas tema, sentimento, evidência e ação sugerida, e uma lista final com as 3 prioridades mais importantes a serem tratadas.

**Restrições:**
- Use apenas os dados fornecidos.
- Não invente números, causas ou conclusões.
- Não exponha dados pessoais ou sensíveis (nomes, CPFs, números de conta, etc.).
- Informe limitações quando os dados não forem suficientes para uma conclusão.
- Use linguagem simples, direta e voltada para tomada de decisão.

---

## Demonstração prática do prompt em ação

Para validar o prompt final, ele foi testado com uma base de dados fictícia de exemplo. Abaixo estão os dados de entrada e o resultado gerado pela IA.

### Base de dados fornecida

```json
[
  {
    "data": "2026-07-01",
    "canal_de_atendimento": "Chat",
    "texto_do_feedback": "Tentei fazer um Pix ontem à noite para pagar o aluguel e o aplicativo ficou dando erro de timeout o tempo todo. Só consegui hoje de manhã. Falta de respeito!",
    "produto_citado": "Pix / Aplicativo",
    "nota_de_satisfacao": 1
  },
  {
    "data": "2026-07-02",
    "canal_de_atendimento": "Loja de Aplicativos",
    "texto_do_feedback": "O novo layout do app ficou lindo e muito mais rápido para ver o saldo. Parabéns pela atualização!",
    "produto_citado": "Aplicativo",
    "nota_de_satisfacao": 5
  },
  {
    "data": "2026-07-02",
    "canal_de_atendimento": "Chat",
    "texto_do_feedback": "O atendimento humano no chat demorou mais de 40 minutos para responder sobre o estorno do meu cartão. O robô inicial não resolve nada e só enrola.",
    "produto_citado": "Atendimento por Chat / Cartão de Crédito",
    "nota_de_satisfacao": 2
  },
  {
    "data": "2026-07-03",
    "canal_de_atendimento": "Reclame Aqui",
    "texto_do_feedback": "Apareceu uma cobrança duplicada na fatura do meu cartão de crédito deste mês. Quero o estorno imediato pois já paguei o valor correto.",
    "produto_citado": "Cartão de Crédito",
    "nota_de_satisfacao": 1
  },
  {
    "data": "2026-07-03",
    "canal_de_atendimento": "Chat",
    "texto_do_feedback": "Gostei muito da facilidade de ajustar o limite do cartão direto pelo aplicativo, foi bem intuitivo.",
    "produto_citado": "Cartão de Crédito / Aplicativo",
    "nota_de_satisfacao": 4
  }
]
```

### Resultado gerado pela IA

**Resumo executivo:**
Os feedbacks revelam dois problemas críticos de confiabilidade (falha no Pix e cobrança duplicada no cartão) e um gargalo grave no atendimento via chat, todos com forte impacto negativo na satisfação. Em contrapartida, o novo layout do aplicativo e os ajustes de limite de cartão foram muito bem avaliados, indicando que os investimentos recentes em usabilidade estão no caminho certo. A prioridade imediata deve ser resolver falhas transacionais (Pix e faturamento), já que envolvem dinheiro do cliente e geram alto risco de reclamação pública.

**Tabela de temas:**

| Tema | Sentimento | Evidência | Ação sugerida |
|---|---|---|---|
| Falha técnica no Pix (timeout) | Negativo | "aplicativo ficou dando erro de timeout... Falta de respeito!" | Investigar estabilidade do serviço de Pix em horários noturnos e priorizar correção urgente |
| Cobrança duplicada no cartão | Negativo | "Apareceu uma cobrança duplicada na fatura... Quero o estorno imediato" | Auditar processo de faturamento e agilizar fluxo de estorno automático |
| Demora no atendimento via chat | Negativo | "demorou mais de 40 minutos... robô inicial não resolve nada" | Revisar tempo de resposta do atendimento humano e capacidade do chatbot inicial |
| Novo layout do aplicativo | Positivo | "layout do app ficou lindo e muito mais rápido" | Manter linha de design e comunicar a atualização como case de sucesso |
| Ajuste de limite pelo app | Positivo | "facilidade de ajustar o limite do cartão... bem intuitivo" | Replicar esse padrão de usabilidade em outras funcionalidades |

**Top 3 prioridades:**
1. Corrigir instabilidade do Pix, especialmente em horários de pico noturno — risco direto de perda de confiança em transações financeiras.
2. Resolver cobranças duplicadas em cartão de crédito e agilizar estornos — impacto financeiro direto no cliente.
3. Reduzir tempo de resposta no atendimento via chat e aprimorar o chatbot inicial — gargalo recorrente que afeta múltiplos temas.

**Limitação:** a base contém apenas 5 registros, o que é insuficiente para afirmar que esses padrões são estatisticamente recorrentes — recomenda-se validar com uma amostra maior antes de decisões definitivas.
