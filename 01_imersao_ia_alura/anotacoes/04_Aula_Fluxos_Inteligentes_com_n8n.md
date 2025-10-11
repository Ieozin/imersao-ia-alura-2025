# Tema 4: Aula 04 - Fluxos Inteligentes com AI Studio e n8n (10/10)

## 📋 Resumo da Aula

A última aula foi sobre criar um chatbot do zero com n8n e Gemini.

### 🌉 A Ferramenta: n8n como Ponte
* **O que é**: n8n é uma ferramenta de automação que conecta serviços. Usamos como "ponte" para colocar a inteligência do Gemini em um chat acessível por link.

### ⚙️ Passo a Passo da Configuração
1.  **Gatilho (Trigger)**: Iniciar o fluxo no n8n com `When chat message received`.
2.  **Adicionar "Cérebro" (AI Agent)**: Conectar um nó de `AI Agent` ao Gemini.
3.  **Obter Chave de API**: Pegar a chave privada no Google AI Studio.
4.  **Conectar e Configurar**: Colar a chave no n8n, adicionar memória (`Simple Memory`) e, o mais importante, dar uma personalidade com o **System Prompt**.
5.  **Dica**: Tabelas não funcionam bem em system prompts, é melhor usar texto corrido.
6.  **Ativar**: O workflow precisa ser ativado para o link funcionar (evita o erro 404).

## 💭 Meu Entendimento Pessoal

**"Última aula. Essa foi mais densa, mexendo com ferramenta externa."**

O n8n parece poderoso, mas complexo. A ideia de "ponte" faz sentido. A parte da chave de API é um bom lembrete sobre segurança. O mais interessante foi a engenharia do system prompt; ver que precisei insistir com o Gemini pra ele transformar o cardápio em texto puro é um bom aprendizado. Mostra que a interação com a IA é um processo de refinar o pedido. No fim, ter um link com um chatbot funcional é um resultado concreto para a imersão.