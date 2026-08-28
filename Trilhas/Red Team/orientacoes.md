# Red Team — SACI

## Boas-vindas!

Seja bem-vindo(a) à trilha de **Red Team do SACI**!

Se o seu objetivo é entender a mente de um atacante, mapear superfícies de exposição, explorar vulnerabilidades em aplicações e demonstrar o impacto real de falhas de segurança em ambientes corporativos, este é o seu lugar. Aqui, nós vamos além do conceito teórico: você aprenderá a usar ferramentas de reconhecimento, explorar falhas web críticas e reportar suas descobertas com rigor e ética profissional.

Vamos nessa!?

Qualquer dúvida durante o processo, mande uma mensagem em nossa comunidade do WhatsApp.

📲 **Link da comunidade:** [Grupo WhatsApp SACI](https://chat.whatsapp.com/LeKmGy9ODATKgyO0iSyOgt)

> ⚠️ **Atenção:** Esta trilha conta com apenas **08 vagas selecionadas**, garantindo acompanhamento próximo da mentoria e acesso exclusivo às bancadas e equipamentos do laboratório.

---

## 📚 Conteúdo a ser Visto na Capacitação

* **Metodologia de Red Team:** Estruturação de ataques usando a matriz *MITRE ATT&CK*.
* **Exploração Web:** Técnicas de reconhecimento, exploração de falhas (SQLi, Broken Access Control, XSS, etc.) e raciocínio investigativo.
* **Redação Técnica:** Elaboração de relatórios profissionais e Provas de Conceito (PoC).

---

## 🔬 Dinâmica do Laboratório & Infraestrutura Flexível

* **Open Lab:** Toda **Sexta-feira, das 10h00 às 12h00 (Lab 2 do DCC)**. O laboratório estará aberto para mentoria presencial, suporte técnico, troca de ideias e validação das atividades práticas.
* **Notebook Pessoal vs. PCs do Laboratório:**

  * **Opção A (Seu Notebook):** Caso opte por usar seu computador em casa ou trazê-lo para o lab, você precisará instalar o **Docker** para subir a imagem do OWASP Juice Shop localmente.
    * *Repositório oficial do Juice Shop:* `https://github.com/juice-shop/juice-shop.git`

  * **Opção B (Computadores do Lab 2):** Se preferir não usar notebook pessoal ou não quiser instalar o Docker, basta ir ao laboratório às sextas-feiras. Os monitores deixarão o ambiente isolado e as instâncias do Juice Shop configuradas e prontas para uso.

---

## 🛠️ Instruções Bloco a Bloco

### Bloco 1: Fundamentos & Onboarding de Git [Semanas 1 e 2]

**Objetivo:** Criar a base de Red Team, concluir o treinamento no TryHackMe e configurar a estrutura de versionamento no GitHub.

1. **Treinamento Inicial Obrigatório (TryHackMe):**
   * Crie uma conta gratuita na plataforma [TryHackMe](https://tryhackme.com).
   * Acesse e conclua as salas gratuitas da **SECTION 1 (Start Your Cyber Security Journey)**:
     * *Offensive Security Intro*
     * *Defensive Security Intro*
     * *Search Skills*

2. **A base da Documentação (Provas de Conceito):**
   Para elaborar uma boa documentação, precisamos entender exatamente qual tipo de vulnerabilidade estamos analisando. Em uma PoC (Proof of Concept) de qualidade, é fundamental sempre classificar a falha e informar o seu identificador ou escopo (como um registro CVE ou a sua respectiva categoria na OWASP Top 10).

   **Materiais de Estudo:**
   * 📺 **O que é um CVE:** [Hackone - Entenda as Common Vulnerabilities and Exposures](https://youtu.be/1SCy5Xcq0Bw)
   * 📺 **Conheça a OWASP Top 10:** [Solyd - As piores falhas de segurança (Atualização 2025)](https://youtu.be/WYSXGax0r5w)
   * 📖 **Redação Técnica:** [CyberHuntLab - O que é uma PoC e como redigi-la?](https://cyberhuntlab.com.br/?p=1320)

3. **Material Recomendado para Aprofundamento:**
   * 📺 **Curso Gratuito no YouTube:** [Introdução ao Hacking e Pentest 2.0 - Solyd](https://www.youtube.com/playlist?list=PLp95aw034Wn8Wi0NViVF58hOpX-m00jyg) *(Ótimo material para quem deseja ir além dos conceitos básicos).*
   * 🎓 **Curso Gratuito com Certificado:** [Plataforma Solyd](https://solyd.com.br/cursos/introducao-ao-hacking-e-pentest-2/)

4. **Configuração do Git e Resposta Teórica:**
   * Faça o **Fork** do repositório [SACI-UFLA/onboarding-2026-2](https://github.com/SACI-UFLA/onboarding-2026-2) para a sua conta.
   * Na pasta `onboarding-2026-2/Trilhas/Red Team/`, utilize o template `seu-nome.md` para preencher com seus dados e responda à pergunta contida no template. 
   * Crie a sua estrutura de entregas: Dentro de `candidatos/entregas/`, crie uma pasta chamada `trilhaRedTeam`.

* 🚩 **Entrega:** Dentro de `trilhaRedTeam`, crie uma nova pasta chamada `bloco1`. Inclua os prints comprovando a conclusão das salas da SECTION 1 do TryHackMe, o arquivo MD preenchido com a pergunta teórica e abra o **Pull Request** no GitHub.

---

### Bloco 2: Mapeamento, Reconhecimento & Exploração do Alvo [Semanas 3 e 4]

**Objetivo:** Mapear a superfície de ataque da aplicação, investigar recursos ocultos e coletar informações estratégicas sobre o sistema e seus usuários.

1. **Atividade Prática:**
   * Suba o Juice Shop em seu ambiente (via Docker ou nos PCs do Lab 2).
   * **Instrução de Reconhecimento:** Aja como um atacante real analisando a aplicação pela primeira vez. Não se limite apenas ao que está visível na página inicial:
     * Explore a navegação, analise arquivos públicos do sistema e preste atenção aos dados expostos involuntariamente.
     * Tente rastrear informações que identifiquem usuários privilegiados ou administradores do sistema.
     * Procure por funcionalidades escondidas, rotas de teste ou painéis não listados nos menus.

   * 🛠️ **Ferramental Profissional (Proxies de Interceptação):**
     * Embora o F12 (DevTools) do navegador possa ser útil, hackers profissionais utilizam ferramentas especializadas para interceptar pacotes e manipular requisições HTTP em tempo real. As mais famosas do mercado são os proxies **Burp Suite** e **OWASP ZAP**.
     * **Material Obrigatório:** Assista ao vídeo [Master Burp Suite Like A Pro In Just 1 Hour](https://youtu.be/QiNLNDSLuJY?si=YTibtb-NHkBooZhb) e aplique os conceitos de interceptação de tráfego durante o pentest no Juice Shop.

* 🚩 **Entrega:** Dentro de `candidatos/entregas/trilhaRedTeam`, crie uma nova pasta chamada `bloco2`. Adicione um relatório em Markdown ou PDF detalhando:
  * As rotas, arquivos ou endpoints interessantes que você descobriu no alvo.
  * O método utilizado para rastrear e identificar o endereço de e-mail da conta administradora do sistema.
  * Print(s) comprovando as descobertas feitas.
---

### Bloco 3: Exploração Web & Bypass de Autenticação (SQLi) [Semanas 5 e 6]

**Objetivo:** Compreender a teoria por trás da vulnerabilidade de **SQL Injection (SQLi)**, identificar pontos de entrada vulneráveis e realizar o bypass do mecanismo de login.

1. **Atividade Prática:**
   * **Análise de Vulnerabilidade:** Analise os formulários de entrada do Juice Shop onde dados do usuário são processados pelo banco de dados sem a devida higienização.
   * **Cenário de Ataque:** O seu objetivo é manipular a consulta SQL do formulário de login para autenticar-se na aplicação utilizando a conta de Administrador encontrada no Bloco 2, sem possuir a senha real.

* 🚩 **Entrega:** Dentro de `candidatos/entregas/trilhaRedTeam`, crie uma nova pasta chamada `bloco3`. Suba um relatório técnico de PoC (Markdown ou PDF) contendo:
  * **Descrição da Falha:** Explicação teórica de como o SQL Injection funciona no contexto do formulário testado.
  * **Passo a Passo da Exploração:** O *payload* exato utilizado no campo de entrada e prints comprovando o acesso bem-sucedido ao perfil do Administrador.
  * **Remediação Recomendada:** Explique detalhadamente como o código da aplicação deveria ser corrigido (ex: implementação de *Prepared Statements / Parameterized Queries*).

---

### Bloco 4: Desafio Final em Bancada (Instância do Lab) [Semanas 7 e 8]

**Objetivo (100% PRESENCIAL):** Demonstrar a capacidade de encadear explorações (*Chaining Exploits*) em tempo real na instância oficial do laboratório.

* **Agendamento:** Os 8 candidatos selecionados serão organizados em turnos nas sextas-feiras (10h às 12h - Lab 2 do DCC).
* **Cenário:** A aplicação estará rodando na rede local do laboratório em uma instância isolada configurada em **Modo CTF**. 

#### Missão em Bancada (Chaining Exploits):

1. **Etapa 1 (Recon & Bypass):** Localizar informações relevantes sobre o usuário administrador e realizar o bypass de autenticação via SQL Injection na máquina do laboratório.
2. **Etapa 2 (Exploração Administrativa & Capture The Flag):** Uma vez logado como Admin, navegue pela aplicação e descubra a rota da área restrita. Ao acessar o painel oculto, o sistema emitirá uma notificação na tela contendo uma **Flag Criptográfica (Hash)**.
3. **Etapa 3 (Defesa Oral):** Você deverá apresentar essa Flag ao mentor, explicando presencialmente o raciocínio utilizado desde o reconhecimento, o funcionamento técnico do payload injetado e as medidas corretivas para as vulnerabilidades exploradas.
