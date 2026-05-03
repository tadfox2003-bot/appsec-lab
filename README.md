# Desafio DevSecOps — Gerenciador de Tarefas

## Sobre o Projeto
Este repositório faz parte do desafio prático do módulo de DevSecOps da ADA Tech.
Você receberá este projeto com vulnerabilidades propositais e uma pipeline incompleta.
Seu objetivo é **implementar a pipeline de segurança** e **corrigir as vulnerabilidades**.

## Estado atual
A pipeline está **incompleta**. Os steps de segurança precisam ser implementados por você.

## Sua missão
1. Implementar os steps de segurança no `pipeline.yml`
2. Fazer a pipeline **quebrar** ao detectar os problemas
3. Corrigir as vulnerabilidades encontradas
4. Fazer a pipeline **passar** com tudo verde ✅
5. Documentar o funcionamento da pipeline neste README

## O que implementar
- [ ] Secrets Scanning com **Gitleaks**
- [ ] SAST com **Semgrep**
- [ ] SCA com **Grype**
- [ ] Deploy com **GitHub Pages**
      
## Como a pipeline funciona
-  Gitleaks: Varre o histórico de commits em busca de segredos (chaves, senhas) expostos. É vital para evitar vazamento de credenciais.
- Semgrep (SAST): Analisa o código-fonte estático procurando padrões de código inseguro (vulnerabilidades de lógica).
- Grype (SCA): Analisa as dependências (bibliotecas de terceiros) para garantir que não estamos usando pacotes com vulnerabilidades conhecidas.
- Deploy: Só é executado se todos os passos anteriores passarem, garantindo que apenas código seguro vá para produção.

   O uso de .innerHTML com dados não confiáveis é uma causa comum de ataques Cross-Site Scripting (XSS) baseados no DOM (DOM XSS). Riscos incluem roubo de cookies/sessões, sequestro de contas, desfiguração de sites e injeção de scripts maliciosos que executam no navegador da vítima, burlando a política de mesma origem.

## Riscos Principais de XSS.

  - Roubo de Sessão/Cookies: Invasores capturam tokens de autenticação (cookies) para assumir contas.
  - Sequestro de Conta e Ações: Executar comandos no navegador da vítima como se fossem ações legítimas.
  - Redirecionamentos e Phishing: Usuários são enviados para sites maliciosos ou enganados por falsos formulários.
  - Captura de Dados: Monitoramento de teclas ou dados preenchidos pelo usuário

## Por que o .innerHTML é Perigoso.

  Renderização de Script: O innerHTML interpreta tags HTML, incluindo <script> ou eventos como "<img src=x onerror=...>". Se um atacante conseguir injetar esse HTML, o JavaScript malicioso será executado.
  XSS Baseado no DOM: O atacante usa o JavaScript do lado cliente para manipular dados do usuário (como URLs ou formulários) e inseri-los no DOM de forma insegura, sem passar pelo servidor.

## URL de Produção
https://tadfox2003-bot.github.io/projeto-devsecops-desafio-II/
