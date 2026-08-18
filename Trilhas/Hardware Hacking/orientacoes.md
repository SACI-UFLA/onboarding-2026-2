# Hardware Hacking — SACI

## Boas-vindas!
Seja bem-vindo(a) à trilha de **Hardware Hacking do SACI**!

Se você é fascinado pela fusão entre o mundo físico e o digital, e quer aprender a explorar vulnerabilidades que softwares sozinhos não conseguem tocar, este é o seu lugar. Aqui, nós quebramos as barreiras tradicionais da tela do computador: entendemos como ondas de rádio, cartões de proximidade e microcontroladores operam para realizar auditorias de perímetro e intrusão física.

Vamos nessa!?

Após a capacitação, acreditamos que você será capaz de executar o desafio final em bancada com excelência. Qualquer dúvida durante o processo, mande uma mensagem em nossa comunidade do WhatsApp.

📲 **Link da comunidade:** [https://chat.whatsapp.com/LeKmGy9ODATKgyO0iSyOgt](https://chat.whatsapp.com/LeKmGy9ODATKgyO0iSyOgt)

> ⚠️ **Atenção:** Esta trilha conta com **apenas 06 vagas selecionadas**, garantindo acompanhamento próximo e acesso exclusivo às bancadas e equipamentos do laboratório.

---

## Conteúdo a ser Visto na Capacitação
* Fundamentos de redes e arquitetura de rádio.
* Radiofrequência aplicada (LF vs HF) e segurança em sistemas RFID/NFC.
* Introdução ao Git, versionamento de código e Linux CLI.

### Aulas Recomendadas:
1. **Base do Hardware Hacking:** [https://www.youtube.com/watch?v=AVOQKERqEDw](https://www.youtube.com/watch?v=AVOQKERqEDw)
2. **Redes de Computadores:** [https://www.youtube.com/watch?v=q0S75nKpmcw](https://www.youtube.com/watch?v=q0S75nKpmcw)
   * **2.1 Redes Sem Fio:** [https://www.youtube.com/watch?v=xXzRKgZbKW8](https://www.youtube.com/watch?v=xXzRKgZbKW8)
3. **Tudo sobre o Proxmark3:** [https://youtube.com/playlist?list=PLH2adjhk7sK_5TJKthGcGU51XGaeW2aWU&si=24IpSKQ3_EalUMOs](https://youtube.com/playlist?list=PLH2adjhk7sK_5TJKthGcGU51XGaeW2aWU&si=24IpSKQ3_EalUMOs)
4. **Base do Raspberry Pi:** Usar o tutorial em PDF disponibilizado na pasta do Drive como guia principal de estudo.
   * 📁 **Pasta do Drive (Hardware Hacking):** [https://drive.google.com/drive/folders/1UOpA738qKFG9kJTrkyqnBQdW56Drz6Xz?usp=sharing](https://drive.google.com/drive/folders/1UOpA738qKFG9kJTrkyqnBQdW56Drz6Xz?usp=sharing)

---

## Dinâmica do Laboratório & Uso dos Equipamentos
* **Open Lab (Toda Sexta-feira, das 10h00 às 12h00 - Lab 2 do DCC):** O laboratório estará aberto para tirada de dúvidas, uso livre dos hardwares (**Proxmark3** e **Raspberry Pi Zero**) e mentoria presencial.
* **Infraestrutura Flexível:** Você pode usar seu próprio notebook pessoal ou utilizar as máquinas do próprio Lab 2 durante os horários de bancada.
* **Aulas Práticas Obrigatórias:** A participação presencial no Lab 2 é **OBRIGATÓRIA** nas sextas-feiras de prática do Proxmark3 e no Desafio Final.

---

## Instruções Bloco a Bloco

### Bloco 1: Fundamentos & Onboarding de Git [Semanas 1 e 2]
**Objetivo:** Configurar seu ambiente Git e demonstrar entendimento sobre a base de rádio.

1. Faça o Fork do repositório [https://github.com/SACI-UFLA/onboarding-2026-2](https://github.com/SACI-UFLA/onboarding-2026-2) para sua conta do GitHub.
2. Clone o repositório para sua máquina local (ou PC do lab).
3. Crie uma Branch com o seu nome (ex: `feat/joao-silva`).
4. Na pasta `candidatos/`, utilize o template `seu-nome.md` para preenchê-lo e modificá-lo de acordo com seus dados e resposta.
5. Responda à pergunta sobre **RFID vs NFC**, faça o Commit, Push e abra o Pull Request.

* **Entrega:** Na pasta `candidatos/entregas/`, crie um arquivo chamado `bloco1.txt` e adicione o link do Pull Request da sua branch para a `main`.

---

### Bloco 2: Mão na Massa e Prática Proxmark3 [Semanas 3 e 4]
**Objetivo (PRESENCIAL OBRIGATÓRIO):** Compilação dos clientes e primeiro contato direto com o leitor RFID/NFC Proxmark3.

1. **Aulas no Lab (Sextas, 10h às 12h):** Compareça ao Lab 2 para conectar o Proxmark3 do núcleo.
2. **Prática Proxmark3:** Execute os comandos de baixo nível (`hf search`, `lf search`, leitura de UID) e garanta que o hardware é reconhecido e responde sem erros no terminal.
3. **Validação Raspberry Pi:** No ambiente Linux (seu note ou PC do lab), instale e valide o funcionamento do `responder` e do `john` (`responder -h`).

* **Entrega:** Na pasta `candidatos/entregas/`, adicione os prints do terminal mostrando a comunicação real com o cliente do Proxmark3 conectado e o comando do `responder` executado com sucesso.

---

### Bloco 3: O Analista/Pesquisador [Semanas 5 e 6]
**Objetivo:** Entender a arquitetura interna de ataques USB/NTLMv2.

1. **Pesquisa Técnica:** Estude o ataque de captura de credenciais via emulação de rede USB (Raspberry Pi Zero com `Responder`) e como ele explora protocolos legados (LLMNR, NetBIOS).
2. **Relatório de Viabilidade:** Escreva um relatório curto (máximo 1 página) em PDF explicando o vetor de ataque e os riscos de acesso físico às portas USB.

* **Entrega:** Na pasta `candidatos/entregas/`, suba o relatório em PDF referente à sua pesquisa.

---

### Bloco 4: Desafio Final em Bancada [Semanas 7 e 8]
**Objetivo (100% PRESENCIAL):** Execução prática ao vivo no Lab 2 do DCC.

* **Agendamento:** Os 6 candidatos serão divididos em turnos de atendimento nas sextas-feiras (10h às 12h).

#### Missão Integrada:
* **Etapa 1:** Ler um cartão Mifare Classic, quebrar chaves lógicas, clonar o UID, abrir a fechadura eletrônica do cofre e resgatar a Raspberry Pi dentro dele.
* **Etapa 2:** Espetar a Pi Zero na máquina alvo, capturar o hash NTLMv2 e realizar a quebra offline da senha.
* **Defesa Oral:** Explicar a lógica utilizada e como superou os desafios físicos ao mentor.