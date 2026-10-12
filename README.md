<div align="center">

<img src="https://raw.githubusercontent.com/muryllodouglashsoares/muryllodouglashsoares/main/hero.svg?v=2" width="100%" alt="Muryllo Douglas — Construindo software do zero para resolver problemas reais"/>

<br>

<a href="https://portfolio-c1u.pages.dev/" target="_blank">
  <img src="https://img.shields.io/badge/Portf%C3%B3lio-12081F?style=for-the-badge&logo=googlechrome&logoColor=8B5CF6" alt="Portfólio" />
</a>
<a href="https://linkedin.com/in/muryllodouglashsoares" target="_blank">
  <img src="https://img.shields.io/badge/LinkedIn-12081F?style=for-the-badge&logo=linkedin&logoColor=8B5CF6" alt="LinkedIn" />
</a>
<a href="mailto:muryllodouglashsoares@gmail.com" target="_blank">
  <img src="https://img.shields.io/badge/Email-12081F?style=for-the-badge&logo=gmail&logoColor=8B5CF6" alt="Email" />
</a>

</div>

<br>

## Sobre mim

Estudante de Informática (Ensino Médio Integrado ao Técnico) no **IFPB — Campus Itaporanga** e desenvolvedor em formação. Construo projetos reais porque acredito que a melhor forma de aprender é fazendo.

Meu foco é desenvolvimento web, com interesse em automação, robótica, arquitetura de software e estruturas de dados. Não estou tentando parecer alguém com anos de experiência: mostro o que consigo construir agora e evoluo rápido.

**Busco minha primeira oportunidade como estagiário ou desenvolvedor trainee.**

**Minha evolução, projeto a projeto:**

```
Fundamentos  →  Exploração  →  Construção  →  Publicação  →  Evolução
```

<br>

## Projetos em destaque

### Tekidu — gestão e acompanhamento acadêmico

<table>
<tr>
<td width="60%" valign="top">

Plataforma que substitui planilhas e sistemas dispersos por um único ambiente para notas, frequência, boletim, turmas e comunicados, com **quatro experiências** separadas: administrador, professor, estudante e responsável (somente leitura).

- Autenticação com Firebase (login, primeiro acesso com e-mail transacional e recuperação de senha).
- Autorização por perfil nas **Firestore Security Rules**, não apenas escondida na interface, com suíte própria de testes (Vitest + Firebase Emulator).
- Notas, médias, boletim, frequência por sessão, relatórios e justificativas de falta com documento comprobatório.
- Exportação de boletim em PDF e de frequência e relatórios em Excel/PDF.
- PWA instalável, painel de acessibilidade, dark mode e navegação mobile dedicada.

**Stack:** React 18 · TypeScript · Vite · Tailwind CSS · Framer Motion · React Router · Firebase Auth · Cloud Firestore · Cloudflare Pages Functions · Vitest
**Status:** em desenvolvimento

<a href="https://github.com/muryllodouglashsoares/Tekidu">
  <img src="https://img.shields.io/badge/Ver%20c%C3%B3digo-12081F?style=for-the-badge&logo=github&logoColor=FFFFFF" alt="Ver código"/>
</a>
<a href="https://tekidu.pages.dev/">
  <img src="https://img.shields.io/badge/Abrir%20aplica%C3%A7%C3%A3o-8B5CF6?style=for-the-badge&logo=cloudflare&logoColor=12081F" alt="Abrir aplicação"/>
</a>
<a href="https://portfolio-c1u.pages.dev/projects/tekidu">
  <img src="https://img.shields.io/badge/Estudo%20de%20caso-12081F?style=for-the-badge&logo=googlechrome&logoColor=8B5CF6" alt="Estudo de caso no portfólio"/>
</a>

</td>
<td width="40%" valign="top">

<img src="https://github.com/muryllodouglashsoares/Tekidu/raw/main/docs/screenshots/landing-page.png" width="100%" alt="Landing page do Tekidu"/>
<img src="https://github.com/muryllodouglashsoares/Tekidu/raw/main/docs/screenshots/dashboard.png" width="100%" alt="Dashboard do Tekidu"/>

</td>
</tr>
</table>
<details>
<summary><strong>Dois desafios técnicos que enfrentei</strong></summary>
<br>

**1. Esconder botões não protege os dados.** Um usuário autenticado ainda poderia ler ou escrever dados de outro perfil direto na API do Firestore. Revisei o que cada perfil precisa ler e escrever e passei a autorização para as Security Rules, testadas com Vitest, Firebase Emulator e `@firebase/rules-unit-testing`, com cenários de acesso permitido e negado.

**2. Um estudante não deveria baixar o código do painel administrativo.** Mapeei as rotas por perfil e passei a carregar a maioria das páginas sob demanda com `React.lazy` e `Suspense`, agrupadas por perfil.

**O que ainda falta (conforme o roadmap do repositório):** pipeline de CI/CD, testes de componentes de interface, monitoramento de erros em produção e auditoria de acessibilidade.

</details>

<br>

### LexContract — gestão de contratos jurídicos (SaaS B2B)

<table>
<tr>
<td width="60%" valign="top">

Pequenos escritórios de advocacia costumam gerenciar clientes, contratos, modelos e cobranças em planilhas, e-mail e papel, sem rastreabilidade. O LexContract centraliza esse fluxo: cada escritório cadastra clientes, gera contratos a partir de modelos reutilizáveis e acompanha o ciclo do contrato, com documentos, parcelas de pagamento e histórico de auditoria.

- API própria em **Fastify + TypeScript**, com dados relacionais em **PostgreSQL** via **Prisma**.
- Autenticação com **JWT** e permissões por papel (`ADMIN`, `LAWYER`, `ASSISTANT`) verificadas **no backend**, não só na interface.
- **Multi-tenant por escritório**: os services filtram os dados pelo `officeId` do usuário autenticado.
- Contratos gerados a partir de modelos com variáveis, versionamento do conteúdo e transições de status controladas.
- Aceite eletrônico por link de uso único (assinatura simples, **não** ICP-Brasil), pagamentos por parcela e histórico de atividades.
- Backend organizado em módulos por domínio (rotas, controllers, services e schemas Zod) e repositório com testes (Vitest, Playwright E2E), Docker e pipeline de CI no GitHub Actions.

**Stack:** React 19 · TypeScript · Vite · Tailwind CSS 4 · Fastify · Prisma · PostgreSQL · Zod · Vitest · Playwright · Docker

<a href="https://github.com/muryllodouglashsoares/law-contract-management">
  <img src="https://img.shields.io/badge/Ver%20c%C3%B3digo-12081F?style=for-the-badge&logo=github&logoColor=FFFFFF" alt="Ver código"/>
</a>
<a href="https://law-contract-management.pages.dev">
  <img src="https://img.shields.io/badge/Abrir%20aplica%C3%A7%C3%A3o-8B5CF6?style=for-the-badge&logo=cloudflare&logoColor=12081F" alt="Abrir aplicação"/>
</a>

</td>
<td width="40%" valign="top">

<img src="https://github.com/muryllodouglashsoares/law-contract-management/raw/main/docs/screenshots/dashboard.webp" width="100%" alt="Dashboard do LexContract"/>
<img src="https://github.com/muryllodouglashsoares/law-contract-management/raw/main/docs/screenshots/contrato-pagamentos.webp" width="100%" alt="Pagamentos de um contrato no LexContract"/>

</td>
</tr>
</table>

<details>
<summary><strong>Decisões técnicas documentadas no repositório</strong></summary>
<br>

- **Modular monolith em vez de microserviços:** para o estágio do produto, vários serviços trariam custo operacional sem benefício real. Os módulos já têm fronteiras claras, o que facilita uma extração futura.
- **RBAC com `requireRole()` nos `preHandler`s** em vez de uma tabela de permissões: com três papéis fixos, uma camada dinâmica adicionaria complexidade sem necessidade. Autenticação, autorização e validação são etapas separadas e sequenciais.
- **Regras relacionais explícitas no Prisma** (`@@unique`, `@@index`): por exemplo, um CPF/CNPJ não se repete dentro do mesmo escritório, mas pode existir em escritórios diferentes.

O repositório também documenta CI/CD, testes E2E e observabilidade na pasta `docs/`, e declara que não alega conformidade com a LGPD.

</details>

<br>

### IFConnect — rede social acadêmica

<table>
<tr>
<td width="60%" valign="top">

Comunicação acadêmica costuma ficar fragmentada entre grupos de mensagem, murais e avisos soltos. O IFConnect reúne feed social, chat em tempo real e painel administrativo, com permissões distintas para aluno, professor e administrador.

- Cadastro e login por e-mail/senha e Google, com verificação de e-mail e recuperação de senha.
- Feed com curtidas, upvotes e comentários, seguidores e feed personalizado.
- Chat privado e em grupo em tempo real, notificações, badges e conquistas.
- Cargos com permissões distintas e painel de moderação.
- Feito em **JavaScript puro**, sem framework, integrado direto ao Firebase. Não há backend próprio: as permissões por cargo ficam no código do cliente (no Tekidu, a autorização é validada no banco).

**Stack:** JavaScript · HTML · CSS · Firebase Auth · Realtime Database
**Status:** concluído

[Código](https://github.com/muryllodouglashsoares/plataforma-comunicacao) · [Estudo de caso no portfólio](https://portfolio-c1u.pages.dev/projects/ifconnect)

</td>
<td width="40%" valign="top">

<img src="https://github.com/muryllodouglashsoares/plataforma-comunicacao/raw/main/screenshots/Captura%20de%20Tela%20(206).png" width="100%" alt="Feed do IFConnect"/>
<img src="https://github.com/muryllodouglashsoares/plataforma-comunicacao/raw/main/screenshots/Captura%20de%20Tela%20(212).png" width="100%" alt="Painel administrativo do IFConnect"/>

</td>
</tr>
</table>

<br>

### Savora — landing page com reservas integradas

<table>
<tr>
<td width="60%" valign="top">

Peça de portfólio que mostra a diferença entre uma landing page bonita e uma entrega completa: animação autoral na hero e um formulário que realmente termina em algum lugar. O restaurante e seus dados são **fictícios**.

- Hero com a montagem animada de um prato, feita só com `transform` e `opacity` e com versão estática para `prefers-reduced-motion`.
- Cardápio digital por categoria, galeria, avaliações, FAQ e mapa de localização.
- Reservas de ponta a ponta: React Hook Form → server function → webhook do Make → Google Sheets → relatório em PDF.
- Iniciado no Lovable e evoluído manualmente, incluindo a limpeza do scaffold de UI.

**Stack:** React 19 · TypeScript · TanStack Start · Tailwind CSS 4 · Motion · shadcn/ui · React Hook Form · Cloudflare Workers

[Código](https://github.com/muryllodouglashsoares/savora-landing-page) · [Demonstração](https://savora-landing-page.muryllodouglash-soares.workers.dev/) · [Estudo de caso no portfólio](https://portfolio-c1u.pages.dev/projects/savora)

</td>
<td width="40%" valign="top">

<img src="https://github.com/muryllodouglashsoares/savora-landing-page/raw/main/screenshots/Pagina_principal.png" width="100%" alt="Página principal do Savora"/>

</td>
</tr>
</table>

<br>

## Outros projetos

| Projeto | O que demonstra | Links |
|---|---|---|
| **FORJA Training Studio** *(fictício)* | Landing page com formulário validado em duas camadas (cliente com Zod e servidor), campo honeypot anti-bot, integração Make → Google Sheets e SEO técnico (JSON-LD, Open Graph, sitemap). TanStack Start · React 19 · TypeScript · Tailwind CSS 4. | [Código](https://github.com/muryllodouglashsoares/gym-landing-page) · [Demo](https://gym-landing-page.muryllodouglash-soares.workers.dev/) · [Portfólio](https://portfolio-c1u.pages.dev/projects/forja) |
| **OdontoPrime** *(fictício)* | Landing page renderizada via SSR a partir de um design de referência, com dados estruturados (`Dentist` e `FAQPage`) e formulário integrado a webhook, com modo demonstração. TanStack Start · React 19 · TypeScript. | [Código](https://github.com/muryllodouglashsoares/clinica-landing-page) · [Demo](https://clinica-landing-page.muryllodouglash-soares.workers.dev/) · [Portfólio](https://portfolio-c1u.pages.dev/projects/odontoprime) |
| **Mini Olimpíada de Robótica** | Robô seguidor de linha em LEGO Spike Prime para a competição do IFPB, com duas abordagens comparadas: dois sensores de cor em blocos e um sensor em Python. O repositório traz fotos e vídeos do processo. | [Código](https://github.com/muryllodouglashsoares/mini-robotics-competition) · [Portfólio](https://portfolio-c1u.pages.dev/projects/mini-olimpiada-robotica) |

<br>

## Stack

**Usada nos projetos**

<img src="https://skillicons.dev/icons?i=html,css,js,ts,react,tailwind,nodejs,fastify,postgres,prisma,firebase,cloudflare,docker,vitest,git,python&theme=dark&perline=8" alt="HTML, CSS, JavaScript, TypeScript, React, Tailwind CSS, Node.js, Fastify, PostgreSQL, Prisma, Firebase, Cloudflare, Docker, Vitest, Git e Python"/>

<sub>HTML · CSS · JavaScript · TypeScript · React · Tailwind CSS · TanStack Start · Node.js · Fastify · Prisma · PostgreSQL · Firebase Auth · Cloud Firestore · Realtime Database · Vitest · Playwright · Firebase Emulator · Zod · Make · Docker · Cloudflare · Git/GitHub · GitHub Actions · Python · LEGO Spike Prime</sub>

**Atualmente estudando**

Estruturas de dados e algoritmos · Arquitetura de software · Automação e robótica autônoma

<br>

## Práticas de engenharia

Só o que já apareceu em código real nos projetos acima:

- **Autorização no banco** — permissões por perfil em Firestore Security Rules, com testes (Tekidu).
- **Autorização no backend** — papéis verificados em `preHandler`s do Fastify e isolamento de dados por escritório nos services (LexContract).
- **Qualidade** — testes das regras de segurança com Vitest e Firebase Emulator; validação de formulário em duas camadas (FORJA); validação de requisições com Zod e testes E2E com Playwright no repositório (LexContract); code splitting por perfil (Tekidu).
- **Organização** — camada de serviços por domínio, componentes reaproveitados entre telas e log de auditoria assíncrono para alterações sensíveis (Tekidu).
- **Dados relacionais** — modelagem com Prisma e PostgreSQL, com restrições de unicidade e índices (LexContract).
- **Credenciais fora do cliente** — e-mail de primeiro acesso enviado por Cloudflare Pages Functions (Tekidu).
- **Integração e deploy** — formulários ligados a automações reais (Make → Google Sheets), publicação em Cloudflare Pages e Workers, Docker e pipeline de CI no GitHub Actions (LexContract), com Git e GitHub em todos os projetos.

<br>

## Próximos passos

- Estruturas de dados e algoritmos, e arquitetura de software, para construir sistemas mais completos.
- Automação e robótica autônoma.
- Evoluir o Tekidu conforme o roadmap do repositório: CI/CD, testes de componentes de interface, monitoramento de erros e auditoria de acessibilidade.

<br>

<div align="center">

## Disponível para oportunidades

**Buscando minha primeira oportunidade profissional em tecnologia**
como **Estagiário** ou **Desenvolvedor Trainee** — Web / Software

Estou sempre aberto a oportunidades de aprendizado e a experiências em que eu possa contribuir e continuar evoluindo como desenvolvedor.

<a href="https://portfolio-c1u.pages.dev/">Portfólio</a> ·
<a href="https://linkedin.com/in/muryllodouglashsoares">LinkedIn</a> ·
<a href="mailto:muryllodouglashsoares@gmail.com">E-mail</a>

<br><br>

<img src="https://raw.githubusercontent.com/muryllodouglashsoares/muryllodouglashsoares/main/footer_wave.svg" width="100%" alt=""/>

</div>
