<p align="center">
  <a href="https://portfolio-c1u.pages.dev/">
    <img src="https://raw.githubusercontent.com/muryllodouglashsoares/muryllodouglashsoares/main/hero.svg?v=2" alt="Muryllo Douglas — Construindo software do zero para resolver problemas reais" width="100%">
  </a>
</p>

<p align="center">
  <a href="https://portfolio-c1u.pages.dev/"><img alt="Portfólio" src="https://img.shields.io/badge/Portf%C3%B3lio-12081F?style=for-the-badge&logo=googlechrome&logoColor=8B5CF6"></a>
  <a href="https://www.linkedin.com/in/muryllo-douglas-henrique-soares-7a8416416/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-12081F?style=for-the-badge&logo=linkedin&logoColor=8B5CF6"></a>
  <a href="mailto:muryllodouglashsoares@gmail.com"><img alt="E-mail" src="https://img.shields.io/badge/Email-12081F?style=for-the-badge&logo=gmail&logoColor=8B5CF6"></a>
</p>

## Sobre mim

Estudo Informática (Ensino Médio Integrado ao Técnico) no **IFPB — Campus Itaporanga** e sou desenvolvedor em formação. Aprendo construindo: cada projeto abaixo parte de um problema concreto, tem código disponível e declara o que ainda falta.

Meu foco é desenvolvimento web e engenharia de software, com interesse em aplicações desktop, segurança, arquitetura de software, automação e robótica. Não me apresento como alguém com anos de experiência; mostro o que consigo construir agora.

**Busco minha primeira oportunidade como estagiário ou desenvolvedor trainee (web / software).**

## Projetos em destaque

### LexContract — gestão de contratos jurídicos (SaaS B2B)

Pequenos escritórios de advocacia costumam acompanhar contratos, modelos e cobranças em planilhas, e-mail e papel, sem rastreabilidade. O LexContract centraliza clientes, contratos, documentos, parcelas e histórico de auditoria, com os dados de cada escritório isolados.

- API em **Fastify + TypeScript** com **PostgreSQL** via **Prisma**, organizada em módulos por domínio (rotas, controllers, services e schemas Zod).
- Autenticação com JWT; permissões por papel (`ADMIN`, `LAWYER`, `ASSISTANT`) verificadas **no backend**; isolamento multi-tenant, com os services filtrando por `officeId`.
- Contratos gerados a partir de modelos com variáveis, versionamento do conteúdo e transições de status controladas; aceite eletrônico por link de uso único (assinatura simples, **não** ICP-Brasil).
- Qualidade e operação: testes com Vitest, 4 fluxos E2E com Playwright, Docker e CI no GitHub Actions, com deploy só depois de todos os testes passarem.
- Decisões documentadas: *modular monolith* em vez de microserviços e RBAC com `requireRole()` em vez de tabela de permissões, por serem suficientes para o estágio do produto. O repositório não alega conformidade com a LGPD.

**Stack:** React 19 · TypeScript · Vite · Tailwind CSS 4 · Fastify · Prisma · PostgreSQL · Zod · Vitest · Playwright · Docker<br>
**Estado:** demo publicada (frontend no Cloudflare Pages, API no Render).<br>
[Código](https://github.com/muryllodouglashsoares/law-contract-management) · [Demo](https://law-contract-management.pages.dev) · [Estudo de caso](https://portfolio-c1u.pages.dev/projects/lexcontract)

<p>
  <img src="https://github.com/muryllodouglashsoares/law-contract-management/raw/main/docs/screenshots/dashboard.webp" alt="Dashboard do LexContract" width="49%">
  <img src="https://github.com/muryllodouglashsoares/law-contract-management/raw/main/docs/screenshots/contrato-pagamentos.webp" alt="Pagamentos de um contrato no LexContract" width="49%">
</p>

### Tekidu — gestão e acompanhamento acadêmico

Notas, frequência, boletim, turmas e comunicados costumam ficar em planilhas e sistemas separados. O Tekidu reúne tudo em um ambiente com experiências distintas para administrador, professor e estudante.

- Autenticação com Firebase (login, primeiro acesso com e-mail transacional e recuperação de senha).
- **Autorização nas Firestore Security Rules**, não apenas escondida na interface, com suíte própria de testes (Vitest + Firebase Emulator) cobrindo acessos permitidos e negados.
- Notas, médias, boletim, frequência por sessão, relatórios, avisos e calendário acadêmico.
- Páginas carregadas sob demanda por perfil (`React.lazy`), para que um estudante não baixe o código do painel administrativo, e log de auditoria assíncrono para alterações sensíveis.

**Stack:** React 18 · TypeScript · Vite · Tailwind CSS · Firebase Auth · Cloud Firestore · Cloudflare Pages Functions · Vitest<br>
**Estado:** em desenvolvimento. Pendências do roadmap do repositório: CI/CD, testes de componentes, monitoramento de erros e melhorias de acessibilidade.<br>
[Código](https://github.com/muryllodouglashsoares/Tekidu) · [Aplicação](https://tekidu.pages.dev/) · [Estudo de caso](https://portfolio-c1u.pages.dev/projects/tekidu)

<p>
  <img src="https://github.com/muryllodouglashsoares/Tekidu/raw/main/docs/screenshots/landing-page.png" alt="Landing page do Tekidu" width="49%">
  <img src="https://github.com/muryllodouglashsoares/Tekidu/raw/main/docs/screenshots/dashboard.png" alt="Dashboard do Tekidu" width="49%">
</p>

### Evidence Finder — pesquisa local em evidências digitais (desktop)

Encontrar uma informação em muitas capturas de tela, PDFs e conversas exige abrir arquivo por arquivo, e fica difícil provar de onde veio cada trecho. O Evidence Finder organiza os arquivos em projetos independentes, pesquisa o conteúdo **localmente** e exporta os trechos escolhidos com a fonte e o hash.

- Importação de PNG, JPEG, PDF, TXT e texto copiado, com detecção de duplicatas por SHA-256 e **OCR local** (Tesseract, dependência externa).
- Três modos de pesquisa: exata (SQLite FTS5), por significado (embeddings locais) e híbrida.
- Exportação em PDF + `manifest.json` + cópias das fontes com SHA-256 verificado. O repositório explica que o hash não prova autenticidade nem cadeia de custódia.
- Privacidade: sem cliente de rede nem telemetria no código (testes com rede bloqueada em Linux), permissões mínimas do Tauri, CSP restritiva e caminhos escolhidos em diálogos nativos, nunca enviados pela interface.
- Testes registrados no repositório: 82 de frontend e 258 em Rust, rodados em Linux.

**Stack:** Tauri 2 · Rust · React 19 · TypeScript · SQLite · Vitest<br>
**Estado:** v0.1.0, em desenvolvimento. Ainda **pendentes**: validação em Windows real, instalador (não há release publicada), testes com o modelo semântico real e criptografia do armazenamento local.<br>
[Código](https://github.com/muryllodouglashsoares/evidence-finder) · [Estudo de caso](https://portfolio-c1u.pages.dev/projects/evidence-finder)

<p>
  <img src="https://github.com/muryllodouglashsoares/evidence-finder/raw/main/docs/screenshots/Dashboard.png" alt="Tela de projetos do Evidence Finder" width="49%">
  <img src="https://github.com/muryllodouglashsoares/evidence-finder/raw/main/docs/screenshots/Tela_Pesquisa.png" alt="Tela de pesquisa do Evidence Finder" width="49%">
</p>

### GitFlow Desktop — interface gráfica para operar repositórios Git (nome provisório)

Aplicativo desktop para operar repositórios Git locais sem digitar comandos, com foco em mostrar exatamente o que cada operação vai fazer antes de executá-la.

- **Fase 1:** status, arquivos alterados e diffs. **Fase 2:** criar e trocar branches e criar commits selecionando explicitamente os arquivos. **Fase 3:** diagnóstico de sincronização e `fetch`, `pull` e `push` com confirmação do destino.
- O commit usa `git commit --only` com os arquivos marcados, nunca `git add .`; a revisão gera uma impressão digital do estado e o commit é recusado se algo mudar antes da confirmação.
- Segurança: o Git é executado sem shell, com caminhos validados e interpretados literalmente; o app nunca usa `--force` e não armazena credenciais.
- A lógica de Git fica em um crate Rust separado do Tauri, testado com Git real em repositórios temporários e remotos locais.

**Stack:** Tauri · Rust · React · TypeScript · Tailwind CSS · Vitest<br>
**Estado:** em desenvolvimento, sem instalador. O repositório lista como próximas etapas: merge manual, importação de ZIP, resolução de conflitos e pull requests.<br>
[Código](https://github.com/muryllodouglashsoares/gitflow)

## Mais projetos

- **IFConnect** — rede social acadêmica (feed, chat em tempo real, badges, moderação e painel administrativo) em JavaScript puro, com Firebase Auth e Realtime Database. Não tem backend próprio: as permissões por cargo ficam no código do cliente (no Tekidu, a autorização é validada no banco). [Código](https://github.com/muryllodouglashsoares/IFConnect) · [Estudo de caso](https://portfolio-c1u.pages.dev/projects/ifconnect)
- **Landing pages de portfólio** (negócios, equipes e depoimentos **fictícios**) com TanStack Start, SSR, SEO técnico (JSON-LD, Open Graph, sitemap) e formulários integrados a Make → Google Sheets:
  - [Savora](https://github.com/muryllodouglashsoares/savora-landing-page) (restaurante, hero animada e reservas) · [demo](https://savora-landing-page.muryllodouglash-soares.workers.dev/)
  - [FORJA Training Studio](https://github.com/muryllodouglashsoares/gym-landing-page) (validação no cliente e no servidor, honeypot anti-bot) · [demo](https://gym-landing-page.muryllodouglash-soares.workers.dev/)
  - [OdontoPrime](https://github.com/muryllodouglashsoares/clinica-landing-page) (SSR a partir de um design de referência) · [demo](https://clinica-landing-page.muryllodouglash-soares.workers.dev/)
- **Mini Olimpíada de Robótica** — robô seguidor de linha em LEGO Spike Prime, com duas abordagens comparadas: dois sensores em blocos e um sensor em Python. [Código](https://github.com/muryllodouglashsoares/mini-robotics-competition)
- **Woman Importance** — jogo 2D *top-down* em GameMaker (GML) com batalha de chefe em três fases, feito para um evento de Ciências e Tecnologia do IFPB. [Código](https://github.com/muryllodouglashsoares/gamer-make-project)

## Stack

Somente o que aparece em código dos projetos acima.

| Categoria | Tecnologias (projeto onde usei) |
| --- | --- |
| Linguagens | TypeScript · JavaScript · Rust · Python (robótica) · GML (Woman Importance) · HTML/CSS |
| Frontend | React · Vite · Tailwind CSS · TanStack Start (landing pages) · Framer Motion (Tekidu) |
| Backend e dados | Node.js + Fastify, PostgreSQL + Prisma, Zod (LexContract) · Firebase Auth, Firestore e Realtime Database (Tekidu, IFConnect) · SQLite FTS5 (Evidence Finder) |
| Desktop | Tauri 2 com Rust + React (Evidence Finder, GitFlow Desktop) |
| Testes e qualidade | Vitest · Playwright (LexContract) · `cargo test` · Firebase Emulator (Tekidu) · ESLint |
| DevOps | Docker e GitHub Actions (LexContract) · Cloudflare Pages/Workers · Render · Make |
| Ambiente | Git · GitHub · VS Code · Windows · Linux |

**Estudando agora:** estruturas de dados e algoritmos · arquitetura de software · automação e robótica autônoma.

## Práticas de engenharia

| Prática | Onde aparece |
| --- | --- |
| Autorização no backend e isolamento de dados por escritório | LexContract |
| Autorização no banco (Security Rules) com testes de acesso permitido e negado | Tekidu |
| Validação de entradas no servidor | LexContract (Zod), FORJA, GitFlow Desktop |
| Testes automatizados (unidade, integração e E2E) | LexContract, Tekidu, Evidence Finder, GitFlow Desktop |
| CI/CD com deploy condicionado aos testes | LexContract |
| Privacidade e integridade local (offline, SHA-256, CSP) | Evidence Finder |
| Limitações e pendências documentadas | Evidence Finder, LexContract, Tekidu |

## Disponível para oportunidades

**Buscando minha primeira oportunidade profissional em tecnologia** como **estagiário** ou **desenvolvedor trainee** — web / software.

[Portfólio](https://portfolio-c1u.pages.dev/) · [LinkedIn](https://www.linkedin.com/in/muryllo-douglas-henrique-soares-7a8416416/) · [E-mail](mailto:muryllodouglashsoares@gmail.com)

<p align="center">
  <img src="https://raw.githubusercontent.com/muryllodouglashsoares/muryllodouglashsoares/main/footer_wave.svg" alt="" width="100%">
</p>
