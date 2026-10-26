# TechMock - Simulador de Entrevistas Técnicas 🚀

## 1. Breve descrição da aplicação desenvolvida e códigos (GitHub)
O **TechMock** é uma aplicação web interativa em modelo *Single Page Application* (SPA) focada na preparação de candidatos para vagas de tecnologia. Com um design moderno em *dark mode* e desenvolvido utilizando React e Tailwind CSS, ele simula o ambiente de uma entrevista técnica. O sistema guia o usuário por uma sabatina de perguntas focadas na stack escolhida (ex: Java, Python, SQL) e nível de senioridade, finalizando com um relatório de desempenho.

**Código-fonte:** O código completo gerado pela IA está disponível neste repositório no arquivo principal `app.tsx`.

---

## 2. Prompts e LLMs utilizados
*   **Plataforma de Geração UI/UX:** [v0 by Vercel](https://v0.app/) (Utiliza modelos de IA avançados para gerar código React/Tailwind em tempo real).
*   **Motor Lógico e Estruturação:** Google Gemini (Utilizado para planejar a arquitetura da aplicação, refinar a lógica de estados e criar o prompt mestre).

**Prompt Mestre utilizado no v0.app:**
> "Crie uma aplicação web responsiva em React e Tailwind CSS chamada "TechMock", um simulador interativo de entrevistas técnicas. A UI deve adotar um tema Dark Mode elegante com detalhes em verde-esmeralda e azul-marinho. A aplicação possui 3 visualizações controladas por estado: 1. Tela de Setup (formulário com Vaga, Tecnologias, Nível), 2. Tela de Entrevista (Modo Chat simulando recrutador IA e candidato com limite de 5 perguntas), 3. Tela de Dashboard (Feedback final com Score e pontos fortes/fracos). Escreva o código completo, funcional e com transições suaves."

---

## 3. Exemplos e explicação das telas e da aplicação

A aplicação foi dividida em três estados principais, garantindo uma navegação fluida sem necessidade de recarregar a página:

### 📱 Tela 1: Setup (Preparação)
Uma interface inicial em estilo *glassmorphism*. Nela, o usuário preenche o seu nome, a vaga desejada (ex: Engenharia de Software), a stack de tecnologias e o nível de experiência (Estágio, Júnior, Pleno). Estes dados servem como base de contexto para a inteligência artificial formular as perguntas adequadas.

### 💬 Tela 2: Entrevista (Modo Chat)
Ao iniciar a simulação, o usuário é levado para um ambiente focado. O layout apresenta um cabeçalho indicando o progresso (ex: Pergunta 1 de 5) e uma interface de chat. O "Recrutador IA" faz perguntas técnicas sequenciais. Para manter o rigor de uma entrevista real, o recrutador não diz se a resposta está certa ou errada imediatamente, apenas conduz a conversa e aprofunda os temas.

### 📊 Tela 3: Dashboard de Feedback
Após a 5ª interação, a entrevista é encerrada e a tela de chat dá lugar a um painel analítico. Esta tela exibe:
*   **Score Geral:** Uma pontuação de desempenho.
*   **Pontos Fortes:** O que o candidato demonstrou dominar.
*   **Gargalos Técnicos:** Correções de conceitos que o candidato errou durante o chat.
*   **Plano de Estudo Sugerido:** Tópicos recomendados para focar antes da entrevista real.
