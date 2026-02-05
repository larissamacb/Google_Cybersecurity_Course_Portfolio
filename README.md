# Portfólio - Google Cybersecurity Certificate 

Este repositório documenta os projetos práticos e laboratórios concluídos durante a trilha de certificação profissional em Cibersegurança do Google.

## 📑 Índice

* [1. Auditoria de Controles de Segurança e Conformidade](#1-auditoria-de-controles-de-segurança-e-conformidade)
* [2. Análise de Tráfego de Rede e Diagnóstico DNS](#2-análise-de-tráfego-de-rede-e-diagnóstico-dns)
* [3. Análise de Tráfego e Identificação de Ataque DoS (TCP SYN Flood)](#3-análise-de-tráfego-e-identificação-de-ataque-dos-tcp-syn-flood)
* [Certificado](#-certificado)

---

## 📂 Projetos e Atividades Práticas

### 1. Auditoria de Controles de Segurança e Conformidade
* **Atividade:** Avaliação de postura de segurança através de Análise de Lacunas (Gap Analysis), verificando a implementação de controles administrativos e técnicos com base no NIST CSF.
* **Cenário:** A Botium Toys, no processo de expansão internacional e digital, precisava validar se sua infraestrutura atual atendia aos requisitos de segurança e leis de conformidade antes de continuar seu crescimento.
* **Meu Objetivo:** Analisar o relatório de escopo e riscos da empresa para realizar uma *Gap Analysis* (Análise de Lacunas). Utilizei uma lista de verificação (checklist) para determinar quais controles de segurança e requisitos de conformidade estavam efetivamente implementados e quais precisavam de atenção imediata.
* **Entregável:** Lista de Verificação de Controles e Conformidade (Compliance Checklist) preenchida com a análise dos ativos.
* **[🔗 Link para os arquivos do projeto](./1_Auditoria_de_Controles_de_Seguranca_e_Conformidade)**

---

### 2. Análise de Tráfego de Rede e Diagnóstico DNS
* **Atividade:** Análise de captura de pacotes de rede por meio do tcpdump para investigar interrupções de serviço, com foco na interpretação de protocolos da camada de transporte (UDP) e mensagens de erro da camada de internet (ICMP).
* **Cenário:** Usuários relataram incapacidade de acessar o site www.yummyrecipesforme.com, recebendo o erro "destination port unreachable". Fui acionada para investigar os logs de rede gravados no momento do incidente e determinar qual serviço específico estava falhando.
* **Meu Objetivo:** Examinar os logs do tcpdump para identificar a causa raiz da falha de conexão. Diagnostiquei que o problema não era no servidor web (HTTPS), mas sim uma falha na resolução de nomes (DNS). Os logs mostravam que as requisições UDP na porta 53 eram respondidas com pacotes ICMP contendo o erro "Port Unreachable", indicando que o serviço de DNS estava inativo e não conseguia traduzir o domínio para um endereço IP.
* **Entregável:** Relatório de Análise de Incidente de Rede (focado em DNS/ICMP).
* **[🔗 Link para os arquivos do projeto](./2_Analise_de_Trafego_de_Rede_e_Diagnostico_DNS)**
 
---

### 3. Análise de Tráfego e Identificação de Ataque DoS (TCP SYN Flood)
* **Atividade:** Análise de captura de pacotes (logs de rede) para diagnosticar interrupções de serviço causadas por ataques de rede, com foco na interpretação do handshake TCP de três vias.
* **Cenário:** O servidor web de uma agência de publicidade ficou inacessível para os funcionários, apresentando erros de "Connection Timeout". O sistema de monitoramento alertou sobre o problema e uma análise de tráfego revelou um volume massivo de solicitações TCP SYN vindas de um único endereço IP desconhecido.
* **Meu Objetivo:** Analisar os logs, explicar o ataque e sugerir formas de preveni-lo.
* **Entregável:** Relatório de Incidente de Segurança Cibernética.
* **[🔗 Link para os arquivos do projeto](./3_Analise_de_Trafego_e_Identificacao_de_Ataque_DoS)**

---

### 4. Investigação de Comportamento Malicioso em um Site
* **Atividade:** Resposta a incidente de segurança envolvendo comprometimento de servidor web, análise de tráfego (tcpdump) e documentação pós-incidente.
* **Cenário:** O site yummyrecipesforme.com foi invadido por um ex-funcionário que utilizou um ataque de força bruta para descobrir a senha administrativa (que era a padrão). O atacante injetou código malicioso (JavaScript) que induzia os visitantes a baixar um malware e os redirecionava para um site falso (greatrecipesforme.com).
* **Meu Objetivo:** Analisar os logs do tcpdump para identificar os protocolos de rede manipulados (DNS e HTTP). Documentei a cronologia do ataque, desde a exploração da senha fraca até o redirecionamento dos usuários.
* **Entregável:** Relatório de Incidente de Segurança (com análise técnica e sugestões de prevenção futura).
* **[🔗 Link para os arquivos do projeto](./4_Investigacao_de_Comportamento_Malicioso_em_um_Site)**
* 
---

## 📜 Certificado
* **Status:** Em progresso.
