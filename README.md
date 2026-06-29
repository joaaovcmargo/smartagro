# SmartAgro - Inteligência Agrícola 🌾🚀

O **SmartAgro** é uma plataforma web premium, moderna e responsiva voltada para o agronegócio brasileiro. O sistema consolida dados meteorológicos, indicadores do mercado financeiro, cotações de commodities (soja e milho), índices da Bolsa de Valores de Nova York (NYSE) e um portal de notícias em tempo real, auxiliando produtores rurais e agrônomos na tomada de decisões estratégicas no campo.

## 📱 Funcionalidades Principais

- **Dashboard Estilo Fintech:** Monitoramento consolidado de indicadores operacionais.
- **Geolocalização & Clima:** Integração dinâmica com a API *Open-Meteo* para detecção de temperatura, umidade e alertas de manejo baseados no clima local.
- **Cotações e Câmbio:** Integração com a *AwesomeAPI* para o dólar comercial em tempo real e simulação estruturada para o mercado físico de grãos.
- **NYSE em Tempo Real:** Exibição dos índices S&P 500, Nasdaq e Dow Jones com variações percentuais.
- **Portal de Notícias Avançado:** Layout inspirado no *Canal Rural* (destaques grandes + grid de cards), com integração via proxy a feeds RSS e sistema de busca com filtro em tempo real.
- **AgroAI Insights:** Módulo de inteligência artificial simulada que cruza dados de clima e mercado para gerar recomendações agronômicas.
- **Gráficos Interativos:** Linhas de tendência geradas dinamicamente usando *Chart.js*.
- **Modo Escuro (Dark/Light Mode):** Alternador de tema visual com persistência no navegador via `localStorage`.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5** Semântico
- **CSS3** (Grid, Flexbox, Variáveis nativas e efeitos de *Glassmorphism*)
- **JavaScript Puro (Vanilla JS)** (Manipulação de DOM, Fetch API, Promises)
- **Chart.js** (Renderização gráfica)
- **FontAwesome & Google Fonts (Inter)** (Elementos visuais e tipografia)

---

## 🗒️ Histórico de Prompts de Desenvolvimento

Para fins de auditoria, manutenção e engenharia de prompt, abaixo estão listados os comandos estruturados utilizados para gerar o escopo atual do projeto:

### 1. Prompt de Arquitetura e Design System
> "Crie as diretrizes visuais para uma plataforma agro chamada SmartAgro inspirada no portal Canal Rural e em interfaces fintech modernas. Utilize paleta de cores baseada em tons de verde escuro, preto e branco, com gradientes suaves, efeitos de desfoque de fundo (glassmorphism) e sombras elegantes. O design precisa ser responsivo, limpo e utilizar a tipografia Inter."

### 2. Prompt do Dashboard e Integração de APIs
> "Escreva o código JavaScript para integrar a API Open-Meteo capturando a geolocalização do usuário de forma assíncrona. Caso o usuário recuse, configure o fallback para a cidade de São Paulo. Integre também a AwesomeAPI para coletar o valor do dólar comercial em tempo real e estruture uma função com o proxy AllOrigins para realizar scraping de cotações agrícolas de soja e milho."

### 3. Prompt do Portal de Notícias e Feeds RSS
> "Crie uma seção de notícias que consoma feeds XML do Google News utilizando termos de busca do Canal Rural, BASF, Syngenta e The AgriBiz. O layout deve conter dois cards grandes de destaque no topo e uma barra lateral corporativa. Implemente um array de objetos estáticos como fallback de segurança para que o layout nunca quebre caso o CORS bloqueie as requisições. Adicione um campo de busca que filtre os títulos das notícias em tempo real sem recarregar a página."

### 4. Prompt do Módulo de Análise (AgroAI) e Gráficos
> "Implemente uma função chamada `computeAgroAI` que faça uma leitura dos dados carregados na tela (temperatura, umidade e valor do dólar) e exiba um texto contextualizado com recomendações reais para o fazendeiro (ex: alertar sobre risco de fungos se a umidade passar de 75%). Instancie 3 gráficos do Chart.js para exibir o histórico de 6 semanas da soja, do milho e do dólar."

---

## 📂 Estrutura do Projeto

O projeto foi intencionalmente modularizado em três arquivos essenciais para garantir um código limpo, sustentável e de fácil manutenção:

```bash
├── index.html          # Estrutura de marcação e esqueleto semântico
├── style.css           # Estilização completa, animações e regras de tema
└── script.js           # Lógica de negócio, consumo de APIs e renderização
