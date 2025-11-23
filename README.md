# assistente-logistico
#  Agente de Análise Logística & Automação de Relatórios

> **Status:** Projeto de Automação com GenAI para Eficiência Operacional.

##  O Desafio
No cenário logístico de operações sensíveis (como entrega de chips/TIM), o volume de dados vindo de dashboards e planilhas manuais é alto. O processo manual enfrentava problemas como:
- **Risco de SLA:** Dificuldade em calcular rapidamente pedidos em atraso (D1, D2, D3...) com a regra de corte das 14:00.
- **Fragmentação:** Dados espalhados em múltiplas planilhas.
- **Tempo:** A consolidação para o relatório diário (deadline 21h) consumia horas preciosas.

##  A Solução: Agente Inteligente
Desenvolvi um Agente de IA focado em **Análise de Dados Não-Estruturados** e **Geração de Relatórios**. O agente atua como um analista sênior, processando os dados brutos e gerando insights acionáveis.

### Principais Funcionalidades:
1.  **Cálculo Automático de SLA:** Aplica a lógica de negócio complexa (regra das 14h) para categorizar atrasos automaticamente.
2.  **Identificação de Pendências:** Cruza dados de "fechado em" vs "criado em" para listar pendências por Ponto de Apoio.
3.  **Redação de E-mail:** Gera um texto de "quebra-gelo" profissional e o corpo do e-mail estruturado, pronto para envio à diretoria.

## Engenharia de Prompt (Como funciona)
O "cérebro" do agente está configurado no arquivo `system_prompt.txt`. Utilizei técnicas de:
- **Role Prompting:** Definindo a persona de um "Especialista em Logística".
- **Chain of Thought:** Instruindo a IA a seguir passos lógicos (Analisar -> Calcular -> Redigir).
- **Constraints:** Regras claras do que *não* fazer (evitar redundâncias).

## Tecnologias Utilizadas
- **GenAI / LLMs:** Para interpretação de texto e geração de linguagem natural.
- **Lógica de Scripts:** Para manipulação de dados tabulares (simulado).
- **Engenharia de Prompt:** Para garantir consistência na saída.

## Impacto (Contexto Real)
Esta lógica é a base das automações que aplico no dia a dia, contribuindo para a redução de tempo operacional e aumento na precisão dos relatórios de status.
