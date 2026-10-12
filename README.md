<div align="center">

<img src="https://raw.githubusercontent.com/muryllodouglashsoares/muryllodouglashsoares/main/hero.svg?v=2" width="100%" alt="Muryllo Douglas — Construindo software do zero para resolver problemas reais"/>

<br>

<a href="https://muryllodouglashsoares.github.io/portfolio/" target="_blank">
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

Estudante do curso técnico integrado em Informática do **IFPB — Campus Itaporanga** e desenvolvedor em formação, com foco em **desenvolvimento web e engenharia de software**. Também estudo estruturas de dados, arquitetura de software e robótica autônoma.

Aprendo construindo: meus projetos próprios cobrem interface, autenticação, persistência de dados, integração com serviços externos e deploy. Gosto de entender o problema antes de escolher a solução técnica.

**Busco minha primeira oportunidade como estagiário ou desenvolvedor trainee**, para evoluir dentro de uma equipe de desenvolvimento.

<br>

## Projetos em destaque

### Tekidu — gestão e acompanhamento acadêmico

<table>
<tr>
<td width="60%" valign="top">

Plataforma web que reúne notas, frequência, boletim, turmas e avisos em um só lugar, com experiências separadas para **administradores, professores e estudantes**.

- Login, primeiro acesso (com e-mail transacional via EmailJS) e recuperação de senha, com Firebase Authentication.
- Permissões por perfil validadas nas **Firestore Security Rules**, não apenas na interface.
- **Testes automatizados** com Vitest: regras de negócio (médias e frequência) e Security Rules, estas via Firebase Emulator.
- Camada de serviços por domínio, code splitting por perfil e log de auditoria básico para alterações sensíveis.

**Stack:** React 18 · TypeScript · Vite · Tailwind CSS · Firebase (Auth + Firestore) · Cloudflare Pages
**Status:** em desenvolvimento contínuo

<a href="https://github.com/muryllodouglashsoares/Tekidu">
  <img src="https://img.shields.io/badge/Ver%20c%C3%B3digo-12081F?style=for-the-badge&logo=github&logoColor=FFFFFF" alt="Ver código"/>
</a>
<a href="https://tekidu.pages.dev/">
  <img src="https://img.shields.io/badge/Abrir%20aplica%C3%A7%C3%A3o-8B5CF6?style=for-the-badge&logo=cloudflare&logoColor=12081F" alt="Abrir aplicação"/>
</a>
<a href="https://github.com/muryllodouglashsoares/Tekidu#readme">
  <img src="https://img.shields.io/badge/Documenta%C3%A7%C3%A3o-12081F?style=for-the-badge&logo=markdown&logoColor=8B5CF6" alt="Documentação"/>
</a>

</td>
<td width="40%" valign="top">

<img src="https://github.com/muryllodouglashsoares/Tekidu/raw/main/preview.png" width="100%" alt="Preview do Tekidu"/>

</td>
</tr>
</table>

<br>

### IFConnect — rede social acadêmica

<table>
<tr>
<td width="60%" valign="top">

Plataforma para conectar alunos, professores e administradores em um ambiente digital integrado, reunindo comunicação e moderação de conteúdo.

- Feed com curtidas, comentários e seguidores; chat privado e em grupo em tempo real; notificações e badges de conquistas.
- Cadastro e login por e-mail/senha e Google, com verificação de e-mail e recuperação de senha.
- Cargos (aluno, professor, administrador), denúncias, fila de moderação e painel administrativo.
- Aplicação em JavaScript puro conectada diretamente ao Firebase, sem backend próprio; o controle de permissões por cargo fica no cliente (no Tekidu, ele é validado nas Security Rules).

**Stack:** JavaScript · HTML5 · CSS3 · Firebase Authentication · Realtime Database
**Status:** em evolução

[Código](https://github.com/muryllodouglashsoares/IFConnect) · [Demonstração](https://ifconnect.pages.dev/) · [Documentação](https://github.com/muryllodouglashsoares/IFConnect#readme)

</td>
<td width="40%" valign="top">

<img src="https://github.com/muryllodouglashsoares/IFConnect/raw/main/screenshots/Captura%20de%20Tela%20(206).png" width="100%" alt="Feed do IFConnect"/>

</td>
</tr>
</table>

<br>

### Savora — landing page com reservas integradas

Site de um restaurante **fictício**, com cardápio digital e animações, mas também com um fluxo real de ponta a ponta: o formulário de reservas chama uma *server function* que roda no Cloudflare Worker e repassa os dados a um webhook do Make, cuja URL fica em um secret do servidor, fora do bundle do navegador. A base do projeto foi iniciada no Lovable e evoluída manualmente.

**Stack:** React 19 · TypeScript · TanStack Start · Tailwind CSS 4 · Motion · React Hook Form · Cloudflare Workers

[Código](https://github.com/muryllodouglashsoares/savora-landing-page) · [Demonstração](https://savora-landing-page.muryllodouglash-soares.workers.dev/) · [Documentação](https://github.com/muryllodouglashsoares/savora-landing-page#readme)

<br>

## Robótica e sistemas embarcados

Projetos em que aplico lógica, sensores e controle de motores em hardware real.

- **[Mini Olimpíada de Robótica](https://github.com/muryllodouglashsoares/mini-robotics-competition)** — robô seguidor de linha com LEGO SPIKE Prime, em duas versões: dois sensores de cor (programação em blocos) e um sensor (Python). O repositório inclui fotos, vídeos e as regras da prova.
- **Robô de Resgate — OBR** — robô autônomo para missões simuladas de resgate na Olimpíada Brasileira de Robótica. *Em desenvolvimento.*
- **Sistema de Alarme de Incêndio** — sistema embarcado que lê sensores de fumaça e temperatura para disparar alertas.

<br>

## Outros projetos web

Landing pages fictícias, com demonstração publicada e foco em interface responsiva, SEO e formulários integrados.

| Projeto | O que demonstra | Links |
|---|---|---|
| **FORJA Training Studio** | Formulário validado no cliente e no servidor com o mesmo schema Zod, campo honeypot, integração com Make → Google Sheets e testes automatizados do envio (`node:test`). React 19, TypeScript, TanStack Start. | [Código](https://github.com/muryllodouglashsoares/gym-landing-page) · [Demo](https://gym-landing-page.muryllodouglash-soares.workers.dev/) |
| **OdontoPrime** | Renderização no servidor (SSR), dados estruturados (JSON-LD), `sitemap.xml` e endpoint de contato que valida o envio e o encaminha a um webhook. TanStack Start, React 19. | [Código](https://github.com/muryllodouglashsoares/clinica-landing-page) · [Demo](https://clinica-landing-page.muryllodouglash-soares.workers.dev/) |

<br>

## Stack

**Usada nos projetos**

<img src="https://img.shields.io/badge/JavaScript-12081F?style=for-the-badge&logo=javascript&logoColor=F7DF1E" alt="JavaScript"/>
<img src="https://img.shields.io/badge/TypeScript-12081F?style=for-the-badge&logo=typescript&logoColor=3178C6" alt="TypeScript"/>
<img src="https://img.shields.io/badge/React-12081F?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React"/>
<img src="https://img.shields.io/badge/HTML5-12081F?style=for-the-badge&logo=html5&logoColor=E34F26" alt="HTML5"/>
<img src="https://img.shields.io/badge/CSS3-12081F?style=for-the-badge&logo=css3&logoColor=1572B6" alt="CSS3"/>
<img src="https://img.shields.io/badge/Tailwind%20CSS-12081F?style=for-the-badge&logo=tailwindcss&logoColor=06B6D4" alt="Tailwind CSS"/>
<img src="https://img.shields.io/badge/Firebase-12081F?style=for-the-badge&logo=firebase&logoColor=FFCA28" alt="Firebase"/>
<img src="https://img.shields.io/badge/Cloudflare-12081F?style=for-the-badge&logo=cloudflare&logoColor=F38020" alt="Cloudflare"/>
<img src="https://img.shields.io/badge/Vitest-12081F?style=for-the-badge&logo=vitest&logoColor=6E9F18" alt="Vitest"/>
<img src="https://img.shields.io/badge/Git-12081F?style=for-the-badge&logo=git&logoColor=F05032" alt="Git"/>
<img src="https://img.shields.io/badge/LEGO%20SPIKE%20Prime-12081F?style=for-the-badge&logo=lego&logoColor=E01A22" alt="LEGO SPIKE Prime"/>

**Estudando e aprofundando**

<img src="https://img.shields.io/badge/Python-1A1025?style=for-the-badge&logo=python&logoColor=3776AB" alt="Python"/>
<img src="https://img.shields.io/badge/Estruturas%20de%20Dados-1A1025?style=for-the-badge&logo=leetcode&logoColor=F1C21B" alt="Estruturas de Dados"/>
<img src="https://img.shields.io/badge/Arquitetura%20de%20Software-1A1025?style=for-the-badge&logo=blueprint&logoColor=8B5CF6" alt="Arquitetura de Software"/>
<img src="https://img.shields.io/badge/Rob%C3%B3tica%20Aut%C3%B4noma-1A1025?style=for-the-badge&logo=robotframework&logoColor=8B5CF6" alt="Robótica Autônoma"/>

<br>

## Práticas de engenharia

Cada ponto abaixo tem evidência no código ou na documentação de um dos projetos acima.

- **Controle de acesso no banco** — permissões por perfil em Firestore Security Rules (Tekidu).
- **Testes automatizados** — Vitest e Firebase Emulator para regras de negócio e Security Rules (Tekidu); `node:test` para o tratamento do formulário (FORJA).
- **Validação e tratamento de erros** — schema Zod compartilhado entre cliente e servidor, honeypot, timeout e resposta de falha sem expor dados (FORJA).
- **Segredos fora do cliente** — URLs de webhook lidas apenas no servidor (Savora, FORJA, OdontoPrime).
- **Organização do código** — serviços por domínio e carregamento sob demanda por perfil (Tekidu).
- **Versionamento e deploy** — Git/GitHub e publicação em Cloudflare Pages e Workers.

**Em evolução:** CI/CD, testes de componentes de interface, acessibilidade e monitoramento de erros — itens que ainda constam como próximos passos no roadmap do Tekidu.

<br>

<div align="center">

## Disponível para oportunidades

**Buscando minha primeira oportunidade profissional em tecnologia**
como **Estagiário** ou **Desenvolvedor Trainee** — Web / Software

Quero aplicar o que construí nos projetos acima e continuar aprendendo com uma equipe real.

<a href="https://linkedin.com/in/muryllodouglashsoares">LinkedIn</a> ·
<a href="mailto:muryllodouglashsoares@gmail.com">E-mail</a> ·
<a href="https://muryllodouglashsoares.github.io/portfolio/">Portfólio</a>

<br>

<i>"A capacidade de construir resolve a maioria dos problemas."</i>

<br><br>

<img src="https://raw.githubusercontent.com/muryllodouglashsoares/muryllodouglashsoares/main/footer_wave.svg" width="100%" alt=""/>

</div>
