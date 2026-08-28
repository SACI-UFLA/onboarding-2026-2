# DevSecOps — SACI

## Boas-vindas!

Seja bem-vindo(a) à trilha de **DevSecOps do SACI**!

Se você quer entender como segurança pode (e deve) ser integrada em todas as etapas do ciclo de desenvolvimento de software, em vez de ser tratada como uma etapa isolada no final, este é o seu lugar. Aqui, você vai aprender a pensar em "shift-left security": encontrar e corrigir vulnerabilidades cedo, automatizar verificações de segurança dentro de pipelines de CI/CD e proteger containers, dependências e infraestrutura antes que cheguem à produção.

Vamos nessa!?

Após a capacitação, acreditamos que você será capaz de construir e defender um pipeline seguro de ponta a ponta no desafio final. Qualquer dúvida durante o processo, mande uma mensagem em nossa comunidade do WhatsApp.

📲 **Link da comunidade:** [https://chat.whatsapp.com/LeKmGy9ODATKgyO0iSyOgt](https://chat.whatsapp.com/LeKmGy9ODATKgyO0iSyOgt)

---

## 📚 Conteúdo a ser Visto na Capacitação

* **Fundamentos de DevSecOps:** cultura shift-left, integração de segurança no ciclo de vida de desenvolvimento (SDLC).
* **CI/CD Seguro:** construção de uma pipeline (GitHub Actions) que roda a cada push, com *gates* de segurança automatizados que bloqueiam o build/merge quando há achados críticos, seguida de deploy automático quando tudo passa na `main`.
* **Análise Estática e de Dependências:** SAST (Static Application Security Testing) e SCA (Software Composition Analysis).
* **Segurança de Containers:** hardening e scanning de imagens Docker.
* **Gestão de Segredos:** boas práticas para não vazar credenciais em código e pipelines.

### Nivelamento (recomendado para calouros)
0. **Git e GitHub Básico:** [https://www.youtube.com/watch?v=pyM5QLS2h6M](https://www.youtube.com/watch?v=pyM5QLS2h6M) — recomendado para quem ainda não tem familiaridade com versionamento e fluxo de commits/push, pré-requisito para o Bloco 1.
1. **Como usar IA para aprender programação sem virar uma farsa:** [https://www.youtube.com/watch?v=7ca3E6Phg-E](https://www.youtube.com/watch?v=7ca3E6Phg-E) — como usar ferramentas de IA (ChatGPT, Copilot, Claude, etc.) como apoio ao aprendizado sem virar dependência ou travar quando precisar pensar sozinho.

### Aulas Recomendadas:
1. **Introdução ao DevSecOps:** [https://www.youtube.com/watch?v=CCp30BD9uRo](https://www.youtube.com/watch?v=CCp30BD9uRo)
2. **Docker:** [https://www.youtube.com/watch?v=DdoncfOdru8&t=1506s](https://www.youtube.com/watch?v=DdoncfOdru8&t=1506s)
3. **GitHub Actions:** [https://www.youtube.com/watch?v=F51HlrEeedw](https://www.youtube.com/watch?v=F51HlrEeedw)
4. **OWASP Top 10:** [https://owasp.org/www-project-top-ten/](https://owasp.org/www-project-top-ten/)

---

## 🖥️ Dinâmica da Mentoria & Configuração de Ambiente

* **Suporte via WhatsApp:** não haverá encontros semanais fixos. O grupo do WhatsApp ficará aberto para dúvidas a qualquer momento — se precisar de ajuda, é só chamar por lá.
* **Google Meet sob demanda:** caso a dúvida exija uma conversa mais aprofundada, um encontro via Google Meet pode ser marcado em horário combinado entre você e a mentoria.
* **Acompanhamento das entregas:** como não há validação semanal ao vivo, o progresso de cada bloco será verificado pelas **datas dos commits** feitos nas pastas correspondentes (`bloco1/`, `bloco2/`, `bloco3/`) do seu repositório — por isso é importante commitar de forma incremental, à medida que avança, em vez de subir tudo de uma vez no fim do prazo.
* **Configuração de Ambiente:** é responsabilidade de cada trainee configurar sua própria máquina para acompanhar a trilha. Não haverá máquinas de laboratório disponíveis para esta trilha — todas as atividades devem ser executadas no seu próprio notebook/computador.

### O que instalar antes do Bloco 1

1. **Git** — controle de versão, usado em todos os blocos.
   * Download: [https://git-scm.com/downloads](https://git-scm.com/downloads)
   * Verificar instalação: `git --version`
2. **Conta no GitHub** — necessária para criar seu repositório de entregas.
   * Criar conta: [https://github.com/join](https://github.com/join)
3. **Editor de código** — recomendado o VS Code.
   * Download: [https://code.visualstudio.com/](https://code.visualstudio.com/)

### O que instalar antes do Bloco 2

4. **Docker Desktop** (ou Docker Engine, em Linux) — necessário para subir aplicações em container.
   * Download: [https://www.docker.com/products/docker-desktop/](https://www.docker.com/products/docker-desktop/)
   * Verificar instalação: `docker --version`
5. **Semgrep** (SAST) — usado para análise estática de código.
   * Instalação via pip: `pip install semgrep`
   * Verificar instalação: `semgrep --version`

### O que instalar antes do Bloco 3

6. **Trivy** (SCA / scan de containers) — instruções de instalação por sistema operacional: [https://aquasecurity.github.io/trivy/latest/getting-started/installation/](https://aquasecurity.github.io/trivy/latest/getting-started/installation/)
   * Verificar instalação: `trivy --version`
7. **Gitleaks** (detecção de segredos) — instruções de instalação: [https://github.com/gitleaks/gitleaks#installing](https://github.com/gitleaks/gitleaks#installing)
   * Verificar instalação: `gitleaks version`
8. **Conta no Render** — usada para o deploy automático da aplicação.
   * Criar conta: [https://render.com/](https://render.com/) (não exige cartão de crédito)

> ⚠️ Caso tenha dificuldades na instalação de qualquer ferramenta, procure a mentoria pelo grupo do WhatsApp.

---

## 🛠️ Instruções Bloco a Bloco

### Bloco 1: Fundamentos & Onboarding de Git [Semanas 1 e 2]
**Objetivo:** Criar e organizar seu próprio repositório de entregas, obter o código-base da trilha e demonstrar entendimento da filosofia DevSecOps.

1. Leia atentamente o arquivo `orientacoes.md` da trilha, disponível em [https://github.com/SACI-UFLA/onboarding-2026-2/blob/main/Trilhas/DevSecOps/orientacoes.md](https://github.com/SACI-UFLA/onboarding-2026-2/blob/main/Trilhas/DevSecOps/orientacoes.md) — não é necessário clonar ou dar fork nesse repositório, apenas ler o conteúdo.
2. Crie um **novo repositório público na sua própria conta do GitHub** (ex: `devsecops-trilha-seu-nome`), que será usado para **todas as entregas da trilha**.
3. Clone o **seu novo repositório** (criado no passo anterior) para sua máquina local.
4. Organize a estrutura de pastas do seu repositório espelhando os blocos da trilha, por exemplo:
   ```
   devsecops-trilha-seu-nome/
   ├── app/            (código-base fornecido pela mentoria)
   ├── bloco1/
   ├── bloco2/
   ├── bloco3/
   └── README.md
   ```
5. Adicione à pasta `app/` o **código-base fornecido pela mentoria** — uma aplicação simples que servirá de projeto-alvo para os Blocos 2 e 3 *(link será disponibilizado pela mentoria antes do início do Bloco 2)*.
6. Dentro da pasta `bloco1/`, crie um arquivo `respostas.md` com seus dados e a resposta à pergunta sobre **SAST vs DAST**.
7. Faça o commit e o push para o seu repositório.

* **Entrega:** o arquivo `bloco1/respostas.md` deve estar disponível no seu repositório. Não há entrega separada neste bloco — o progresso é acompanhado pelas datas dos commits na pasta `bloco1/`, e a entrega oficial de tudo acontece ao final da Semana 6 (veja a seção "Entrega Final" abaixo).

---

### Bloco 2: Mão na Massa — Pipeline Seguro & Análise Estática (SAST) [Semanas 3 e 4]
**Objetivo:** Construir uma pipeline de CI/CD que rode automaticamente a cada push e funcione como o primeiro *gate* de segurança do projeto.

1. **Ambiente:** Utilize o **código-base fornecido pela mentoria** (adicionado na pasta `app/` do seu repositório no Bloco 1) como projeto-alvo — ele já vem preparado com um `Dockerfile`, então nenhum candidato precisa escolher ou montar seu próprio projeto do zero.
2. **Pipeline com GitHub Actions:** Crie um workflow (`.github/workflows/`) disparado automaticamente a cada `push`/`pull_request`, contendo:
   * Uma etapa de **build/instalação de dependências** do projeto (padrão de qualquer pipeline de CI).
   * Uma etapa de **SAST** com o [Semgrep](https://semgrep.dev/), configurada como *gate*: se o Semgrep encontrar um achado de severidade relevante, o job deve **falhar** (pipeline vermelha), impedindo o merge.
3. **Execução e Correção:** Rode a pipeline, analise os alertas encontrados, corrija ao menos uma vulnerabilidade real ou simulada apontada pela ferramenta e valide que a pipeline volta a passar (verde).

* **Entrega:** na pasta `bloco2/` do seu repositório, adicione o arquivo `.yml` do workflow criado e prints mostrando a pipeline falhando (com o achado do Semgrep) e depois passando após a correção.

---

### Bloco 3: Segurança de Containers, Dependências & Segredos + Deploy Automatizado [Semanas 5 e 6]
**Objetivo:** Evoluir a pipeline do Bloco 2 adicionando novos *gates* automatizados de segurança — SCA, scan de containers e detecção de segredos — e fechar o ciclo com deploy automático.

1. **Aplicação-alvo:** Continue utilizando o mesmo código-base fornecido pela mentoria (pasta `app/`) do Bloco 2, que já conta com um `Dockerfile`.
2. **Evolua a mesma pipeline do Bloco 2**, adicionando novas etapas automatizadas (também como *gates*, falhando o job em caso de achado crítico):
   * **Scan de dependências e imagem Docker** com o [Trivy](https://github.com/aquasecurity/trivy).
   * **Detecção de segredos** com o [Gitleaks](https://github.com/gitleaks/gitleaks), rodando sobre o código e o histórico do repositório.
3. **Gate final de Deploy Automático:** Configure um serviço Web gratuito no [Render](https://render.com/) conectado ao seu repositório, com **Auto-Deploy** habilitado. A ideia é que o deploy só aconteça depois que todos os gates de segurança passarem em um push/merge na branch `main` — ou seja, a pipeline vermelha nunca deve chegar ao deploy.
   * Configure o Render para builda a partir do `Dockerfile` do projeto (Web Service → *Deploy an existing image or build from a repo*).
   * Habilite "Auto-Deploy on push to main" nas configurações do serviço.
   * Documente que, por ser o plano gratuito, o serviço "hiberna" após 15 minutos de inatividade e leva alguns segundos para responder à primeira requisição depois disso — isso é esperado e deve ser explicado na defesa.
4. **Execução e Correção:** Rode a pipeline completa (Semgrep + Trivy + Gitleaks + Deploy), corrija os achados críticos (ex: atualizar dependência vulnerável, trocar imagem base, remover/rotacionar segredo commitado) e valide que todos os gates passam e que a aplicação sobe corretamente no Render.
5. **Relatório de Viabilidade:** Escreva um relatório curto (máximo 1 página) em PDF explicando os achados mais críticos de cada ferramenta e as recomendações de remediação (ex: atualização de versão, uso de imagens base mínimas/*distroless*, uso de secret manager em vez de credenciais em texto puro).

* **Entrega:** na pasta `bloco3/` do seu repositório, adicione o `.yml` atualizado do workflow (agora com os 3 gates de segurança + deploy), o relatório em PDF, o link da aplicação publicada no Render e prints da pipeline completa rodando com sucesso.

---

## 📮 Entrega Final (fim da Semana 6)

Ao final da Semana 6, seu repositório deve conter as pastas `bloco1/`, `bloco2/` e `bloco3/` com todos os artefatos pedidos. Você deverá enviar o **link do seu repositório** através do **formulário (Google Forms)** que será disponibilizado pela mentoria, até **domingo, 08/11, às 23:59**.

> ⚠️ Qualquer commit feito após esse prazo será desconsiderado na avaliação — só conta o estado do repositório até esse momento.

---

### Bloco 4: Desafio Final [Semanas 7 e 8]
**Objetivo:** Demonstração ao vivo da pipeline completa construída durante a trilha, com defesa técnica via Google Meet.

* **Agendamento:** Os candidatos selecionados serão divididos em turnos de atendimento; horário a definir.

#### Missão Integrada:
* **Etapa 1:** Colocar toda a pipeline construída ao longo da trilha (Semgrep + Trivy + Gitleaks + deploy automático no Render) para rodar do início ao fim, ao vivo, demonstrando o fluxo completo desde o push até a aplicação publicada.
* **Etapa 2:** Explicar passo a passo como cada gate foi implementado — as escolhas técnicas, o que cada ferramenta verifica e como a pipeline reage a um achado crítico.
* **Defesa Oral:** Responder perguntas técnicas da mentoria sobre qualquer parte do que foi construído (configuração das ferramentas, lógica dos gates, decisões de correção das vulnerabilidades, funcionamento do deploy no Render, etc.).

* **Entrega:** na pasta `bloco4/` do seu repositório, adicione uma documentação em Markdown ou PDF, de forma resumida mas explicativa, contendo:
  * Visão geral da pipeline construída (diagrama ou lista das etapas, na ordem em que rodam).
  * O que cada gate (Semgrep, Trivy, Gitleaks) verifica e por que foi configurado daquela forma.
  * As vulnerabilidades encontradas ao longo da trilha e como cada uma foi corrigida.
  * Como o deploy automático no Render foi configurado.
  * Link da aplicação publicada e do repositório final.
  * Essa documentação deve ser entregue **antes** da apresentação ao vivo, servindo de apoio para a correção e para as perguntas técnicas da defesa.