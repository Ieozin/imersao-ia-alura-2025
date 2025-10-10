# Tema 7: Aula 04 - Fluxos Inteligentes com AI Studio e n8n (10/10)

## 📋 Resumo da Aula

A última aula foi sobre criar um chatbot do zero com ferramentas no-code/low-code, usando o Gemini conectado ao n8n para atuar como um atendente do nosso café.

### 🌉 A Ferramenta: n8n como Ponte

* **O que é**: n8n é uma ferramenta de automação que conecta diferentes serviços. Aqui, usamos ele como uma "ponte" para colocar a inteligência do Gemini dentro de um chat que pode ser acessado por um link, sem precisar programar um back-end complexo.
* **Setup**: É preciso criar uma conta (trial de 14 dias) e iniciar uma automação do zero ("Start from scratch").

### ⚙️ Passo a Passo da Configuração

1.  **Gatilho (Trigger)**: O primeiro passo no n8n é o gatilho. Usamos o `When chat message received` para iniciar o fluxo quando alguém manda uma mensagem.
2.  **Adicionar o "Cérebro" (AI Agent)**: Adicionamos um nó `AI Agent`. Essa é a "casca" que vamos conectar ao Gemini.
3.  **Obter a Chave de API**: Para conectar, precisamos de uma chave de API do Gemini.
    * Acessar o Google AI Studio.
    * Ir em `Get API key` e `Create API key in a new project`.
    * **Importante**: Essa chave é privada e não deve ser compartilhada.
4.  **Conectar no n8n**: Voltamos ao n8n, criamos uma nova credencial para o Google Gemini e colamos a chave de API.
5.  **Adicionar a "Memória"**: Para que o chatbot lembre da conversa, adicionamos o `Simple Memory`. Isso define a janela de contexto do chat.
6.  **Dar uma Personalidade (System Prompt)**: O passo mais importante. No `AI Agent`, em `Options > System Message`, inserimos o contexto do nosso garçom virtual.
    * **Dica da aula**: Tabelas não funcionam bem em system prompts. É melhor usar um texto corrido. Tive que pedir algumas vezes pro Gemini transformar o cardápio em um texto para o prompt.
7.  **Ativar e Testar**:
    * O workflow precisa ser ativado no botão `Inactive` -> `Active`. Se não fizer isso, o link do chat dá erro 404 (Not Found).
    * Depois de ativo, o chat funciona e o agente responde com base no system prompt.
    * A aparência do chat (título, etc.) pode ser editada nas opções do nó de gatilho.

### 📢 Próximos Passos

* Segunda-feira (13/10) tem a live de encerramento, focada em carreira.
* A aula recomendou um guia de engenharia de prompt, que anotei em separado.

## 💭 Meu Entendimento Pessoal

**"Última aula. Essa foi mais densa, mexendo com ferramenta externa."**

O n8n parece poderoso, mas também complexo. Criar a conta e seguir o passo a passo da aula foi tranquilo, mas dá pra ver que é fácil se perder ali com tantas opções de nós e configurações. A ideia de usar ele como uma "ponte" faz todo o sentido, não dá pra só jogar a IA inteira num site e esperar que funcione.

A parte da chave de API é um bom lembrete sobre segurança. É algo pessoal e intransferível. Anotado.

O mais interessante foi a engenharia do system prompt. Ver na prática que uma tabela não funciona bem e que precisei insistir com o Gemini pra ele transformar em texto puro é um bom aprendizado. Mostra que a interação com a IA não é mágica, é um processo de refinar o pedido até conseguir o que você quer.

No fim, ter um link com um chatbot funcional, mesmo que simples, é um resultado concreto para a imersão. A imersão acaba aqui nas aulas, mas ainda tem a live de encerramento na segunda. Veremos.