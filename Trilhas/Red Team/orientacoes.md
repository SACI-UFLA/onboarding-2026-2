# Red Team — SACI


## Boas-vindas!

Seja bem-vindo(a) à trilha de **Red Team do SACI**!

Se o seu objetivo é entender a mente de um atacante, mapear superfícies de exposição, explorar vulnerabilidades em aplicações e demonstrar o impacto real de falhas de segurança em ambientes corporativos, este é o seu lugar. Aqui, nós vamos além do conceito teórico: você aprenderá a usar ferramentas de reconhecimento, explorar falhas web críticas e reportar suas descobertas com rigor profissional.

Vamos nessa!?

Qualquer dúvida durante o processo, mande uma mensagem em nossa comunidade do WhatsApp.

📲 **Link da comunidade:** [Grupo WhatsApp SACI](https://chat.whatsapp.com/LeKmGy9ODATKgyO0iSyOgt)

> ⚠️ **Atenção:** Esta trilha conta com apenas **08 vagas selecionadas**, garantindo acompanhamento próximo e acesso exclusivo às bancadas e equipamentos do laboratório.

---

## 📚 Conteúdo a ser Visto na Capacitação

* **Metodologia de Red Team:** Estruturação de ataques usando a matriz *MITRE ATT&CK*.
* **Exploração Web:** Técnicas de reconhecimento, exploração de falhas (SQLi, Broken Access Control, XSS, etc.) e raciocínio investigativo.
* **Redação Técnica:** Elaboração de relatórios profissionais e Provas de Conceito (PoC).

---

## 🔬 Dinâmica do Laboratório & Infraestrutura Flexível

* **Open Lab:** Toda **Sexta-feira, das 10h00 às 12h00 (Lab 2 do DCC)**. O laboratório estará aberto para mentoria presencial, suporte técnico e validação das atividades práticas.
* **Notebook Pessoal vs. PCs do Laboratório:**

  * **Opção A (Seu Notebook):** Caso opte por usar seu computador em casa ou trazê-lo para o lab, você precisará instalar o **Docker** para subir a imagem do OWASP Juice Shop localmente.
    * *Repositório oficial do Juice Shop:* ` https://github.com/juice-shop/juice-shop.git`

  * **Opção B (Computadores do Lab 2):** Se preferir não usar notebook pessoal ou não quiser instalar o Docker, basta ir ao laboratório às sextas-feiras. Os monitores deixarão o ambiente e as instâncias do Juice Shop configuradas e prontas para uso.

---

## 🛠️ Instruções Bloco a Bloco

### Bloco 1: Fundamentos & Onboarding de Git [Semanas 1 e 2]

**Objetivo:** Criar a base de Red Team, concluir o treinamento base no TryHackMe e configurar a estrutura no GitHub.

1. **Treinamento Inicial Obrigatório (TryHackMe):**
   * 1) Crie uma conta gratuita na plataforma [TryHackMe](https://tryhackme.com).
   * Acesse e conclua as salas gratuitas da **SECTION 1 (Start Your Cyber Security Journey)**:
     * *Offensive Security Intro*
     * *Defensive Security Intro*
     * *Search Skills*

    * 2) Veja o que é uma POC e como faze-la: [cyberhuntlab](https://cyberhuntlab.com.br/?p=1320).

2. **Material Recomendado para Aprofundamento:**
   * 📺 **Curso Gratuito no YouTube:** [Introdução ao Hacking e Pentest 2.0 - Solyd](https://www.youtube.com/playlist?list=PLp95aw034Wn8Wi0NViVF58hOpX-m00jyg) *(Ótimo material para quem deseja ir além dos conceitos básicos).*

3. **Configuração do Git e Resposta Teórica:**
   * Faça o Fork do repositório [SACI-UFLA/onboarding-2026-2](https://github.com/SACI-UFLA/onboarding-2026-2) para sua conta.

   * Na pasta `onboarding-2026-2/Trilhas/Red Team/`, utilize o template `seu-nome.md` para preencher com seus dados e responda a pergunta contida no template. 

   * Crie a sua estrutura de entregas: Dentro de`candidatos/entregas/` crie uma pasta chamada `trilhaRedTeam`.


* **Entrega:** Dentro de `trilhaRedTeam` crie uma nova pasta chamada `bloco1`, inclua os prints comprovando a conclusão das salas da SECTION 1 do TryHackMe, o arquivo MD preenchido com a pergunta teórica e abra o **Pull Request** no GitHub.

---

### Bloco 2: Mapeamento, Reconhecimento & Exploração do Alvo [Semanas 3 e 4]

**Objetivo:** Mapear a superfície de ataque da aplicação, investigar recursos ocultos e coletar informações estratégicas sobre o sistema e seus usuários.

1. **Atividade Prática:**
   * Suba o Juice Shop em seu ambiente (via Docker ou nos PCs do Lab 2).
   * **Instrução de Reconhecimento:** Aja como um atacante real analisando a aplicação pela primeira vez. Não se limite apenas ao que está visível na página inicial:
     * Explore a navegação, inspecione requisições, analise arquivos públicos do sistema e preste atenção aos dados expostos involuntariamente na interface.
     * Tente rastrear informações que identifiquem usuários privilegiados ou administradores do sistema.
     * Procure por funcionalidades escondidas, rotas de teste ou painéis que não deveriam estar expostos publicamente.

* **Entrega:** Dentro de `candidatos/entregas/trilhaRedTeam` crie uma nova pasta chamada `bloco2`, adicione um relatório em Markdown ou PDF detalhando:
  * As rotas, arquivos ou endpoints interessantes que você descobriu no alvo.
  * O método utilizado para rastrear e identificar o endereço de e-mail da conta administradora do sistema.
  * Print(s) comprovando as descobertas.

---

### Bloco 3: Exploração Web & Bypass de Autenticação (SQLi) [Semanas 5 e 6]

**Objetivo:** Compreender a teoria por trás da vulnerabilidade de **SQL Injection (SQLi)**, identificar pontos de entrada vulneráveis e realizar o bypass do mecanismo de login.

1. **Atividade Prática:**
   * **Análise de Vulnerabilidade:** Analise os formulários de entrada do Juice Shop onde dados do usuário são processados pelo banco de dados sem a devida higienização.
   * **Cenário de Ataque:** O seu objetivo é manipular a consulta SQL do formulário de login para autenticar-se na aplicação sem possuir a senha do usuário.


* **Entrega:** Dentro de `candidatos/entregas/trilhaRedTeam` crie uma nova pasta chamada `bloco3`, suba um relatório técnico de PoC (Markdown ou PDF) contendo:
  * **Descrição da Falha:** Explicação teórica de como o SQL Injection funciona no contexto do formulário testado.
  * **Passo a Passo da Exploração:** O *payload* exato utilizado no campo de entrada e prints comprovando o acesso bem-sucedido ao perfil do Administrador.
  * **Remediação Recomendada:** Explique detalhadamente como o código da aplicação deveria ser corrigido (ex: implementação de *Prepared Statements / Parameterized Queries*).

---

### Bloco 4: Desafio Final em Bancada (Instância do Lab) [Semanas 7 e 8]

**Objetivo (100% PRESENCIAL):** Demonstrar a capacidade de encadear explorações (*Chaining Exploits*) em tempo real na instância oficial do laboratório.

* **Agendamento:** Os 8 candidatos selecionados serão organizados em turnos nas sextas-feiras (10h às 12h - Lab 2 do DCC).
* **Cenário:** A aplicação estará rodando na rede local do laboratório em uma instância isolada.

#### Missão em Bancada (Chaining Exploits):

1. **Etapa 1 (Recon & Bypass):** Localizar informações relevantes sobre algum usuário administrador e realizar o bypass de autenticação via SQL Injection.
2. **Etapa 2 (Exploração Administrativa):** Uma vez logado como Admin, navegue pela área restrita da aplicação e localize a **Flag** / cupom secreto exclusivo configurado pela mentoria para comprovar o comprometimento do ambiente.
3. **Etapa 3 (Defesa Oral):** Explicar presencialmente ao mentor o raciocínio utilizado, o funcionamento técnico do payload e as medidas corretivas para aquela vulnerabilidade.