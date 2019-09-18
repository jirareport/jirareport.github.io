---
layout: default
title: Não consigo fazer login
parent: FAQ
nav_order: 1
permalink: /unable-to-login
---

# Não consigo fazer login

- O Sistema de login do Jiratório é atrelado ao sistema de login do Jira, portanto, verifique se você tem acesso ao Jira utilizando as mesmas credenciais que está tentando colocar no Jiratório;
- Em alguns casos onde já houveram algumas tentativas de login sem sucesso o Jira pede que haja a confirmação de um captcha e o Jiratório não mostra esse captcha, para resolver isso, faça logoff e login no Jira para que você consiga validar o captcha na interface do próprio Jira e após isso tente fazer o login novamente no Jiratório;
- Quando o Jiratório está configurado para coletar métricas do Jira na versão cloud é necessário que seja utilizado o API Token da conta no lugar da senha da conta. [Como Gerar API Token](https://confluence.atlassian.com/cloud/api-tokens-938839638.html).