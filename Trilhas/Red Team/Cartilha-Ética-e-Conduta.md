# 🛡️ Cartilha de Ética e Conduta — Red Team SACI

## 1. O Princípio do White Hat: Com grandes poderes, vêm grandes responsabilidades
O objetivo da trilha de Red Team do SACI, promovida pelo Núcleo de Segurança e Auditoria Cibernética, é formar profissionais de excelência em segurança da informação (White Hats). Durante o treinamento, você terá acesso a técnicas, ferramentas e conhecimentos que possuem alto potencial destrutivo se utilizados de forma incorreta. 

No universo da cibersegurança corporativa, a única linha que separa uma auditoria profissional de um crime cibernético é uma única palavra: **Autorização**. 

Realizar testes de intrusão, varreduras (scans) agressivas ou exploração de vulnerabilidades em sistemas, redes ou aplicações para os quais você **não possui autorização prévia, expressa e documentada** é crime e fere os princípios éticos da nossa organização.

---

## 2. O Peso da Lei Brasileira (Legislação e Penalidades)
A legislação brasileira é rigorosa quanto a crimes cibernéticos. O desconhecimento da lei não isenta o infrator de suas responsabilidades. Ao atuar na área de segurança, você deve conhecer o arcabouço legal que rege o tema:

### A. Lei Carolina Dieckmann (Lei nº 12.737/2012)
Foi o principal marco legal que tipificou os crimes cibernéticos no Código Penal Brasileiro, criando o **Artigo 154-A**.
* **O Crime:** *"Invadir dispositivo informático de uso alheio, conectado ou não à rede de computadores, com o fim de obter, adulterar ou destruir dados ou informações sem autorização expressa ou tácita do usuário titular..."*
* **A Penalidade:** Reclusão, de 1 (um) a 4 (quatro) anos, e multa. A pena é aumentada se a invasão resultar na obtenção de comunicações eletrônicas privadas, segredos comerciais/industriais ou informações sigilosas.

### B. Marco Civil da Internet (Lei nº 12.965/2014)
Estabelece princípios, garantias, direitos e deveres para o uso da Internet no Brasil. A interceptação não autorizada de comunicações ou o vazamento de registros de conexão sem ordem judicial constituem graves violações aos direitos de privacidade do usuário.

### C. Lei Geral de Proteção de Dados - LGPD (Lei nº 13.709/2018)
Durante um pentest autorizado, é comum o acesso a bancos de dados. O vazamento, exposição ou cópia não autorizada de dados pessoais de terceiros (como clientes do alvo) pode resultar em multas severas para as empresas e processos civis/criminais para o atacante que expôs os dados, mesmo que o intuito inicial fosse "apenas testar".

---

## 3. As Regras de Ouro do Red Team SACI
Para garantir a sua segurança jurídica e a integridade da capacitação, todo membro do Red Team deve seguir rigorosamente as diretrizes abaixo:

1. **Nunca ataque alvos reais sem permissão escrita:** Só aplique as técnicas ensinadas no laboratório oficial do SACI (ex: Juice Shop) ou em plataformas de CTF baseadas em educação (TryHackMe, HackTheBox). Jamais teste aplicações da universidade, de empresas locais ou de terceiros sem um contrato formal (Rules of Engagement).
2. **Respeite o Escopo (Scope):** Se um cliente autoriza um teste no subdomínio `api.empresa.com.br`, você não pode atacar `rh.empresa.com.br`. Sair do escopo invalida a autorização e o torna um invasor perante a lei.
3. **Não cause indisponibilidade (Do No Harm):** Evite ferramentas automatizadas sem entender o que fazem. Ataques de Negação de Serviço (DDoS) ou payloads destrutivos (como dropar tabelas de banco de dados) só devem ser executados se explicitamente exigidos e aprovados no contrato.
4. **Reporte Responsável (Responsible Disclosure):** Se você esbarrar em uma falha de segurança em um sistema externo acidentalmente, não a explore. Reporte o problema aos administradores de forma ética, privada e sem exigir recompensas sob ameaça (o que configura extorsão).
5. **Sigilo Absoluto (NDA):** O que é descoberto no laboratório ou durante operações de Red Team do Saci. fica no escopo do projeto. O compartilhamento de vulnerabilidades com pessoas não autorizadas quebra o Acordo de Confidencialidade.

---

## 4. Termo de Ciência e Compromisso
A participação na Trilha Red Team pressupõe a leitura, compreensão e aceitação irrestrita desta cartilha. O uso indevido dos conhecimentos aqui ministrados para fins ilícitos, prejudiciais a terceiros ou que violem a legislação vigente resultará em:
* Desligamento imediato da capacitação e do laboratório.
* Comunicação formal às instâncias competentes em caso de danos a infraestruturas.

> *"A segurança da informação é construída sobre a confiança. Seja um profissional digno dessa confiança."*

***
