# Portfólio - Google Cybersecurity Certificate 

Este repositório documenta os projetos práticos e laboratórios concluídos durante a trilha de certificação profissional em Cibersegurança do Google.

## 📑 Índice

* [1. Auditoria de Controles de Segurança e Conformidade](#1-auditoria-de-controles-de-segurança-e-conformidade)
* [2. Análise de Tráfego de Rede e Diagnóstico DNS](#2-análise-de-tráfego-de-rede-e-diagnóstico-dns)
* [3. Análise de Tráfego e Identificação de Ataque DoS (TCP SYN Flood)](#3-análise-de-tráfego-e-identificação-de-ataque-dos-tcp-syn-flood)
* [4. Investigação de Comportamento Malicioso em um Site](#4-investigacão-de-comportamento-malicioso-em-um-site)
* [5. Fortalecimento de Rede e Avaliação de Risco](#5-fortalecimento-de-rede-e-avaliação-de-risco)
* [6. Aplicação do Framework NIST CSF: Resposta a Incidente (ICMP Flood)](#6-aplicação-do-framework-nist-csf-resposta-a-incidente-icmp-flood)
* [7. Avaliação de Privacidade de Dados e Princípio do Menor Privilégio](#7-avaliação-de-privacidade-de-dados-e-princípio-do-menor-privilégio)
* [8. Auditoria de Controle de Acesso e Investigação de Incidente](#8-auditoria-de-controle-de-acesso-e-investigação-de-incidente)
* [9. Análise de Vetor de Ataque Físico e Risco de USB (USB Baiting)](#9-análise-de-vetor-de-ataque-físico-e-risco-de-usb-usb-baiting)
* [10. Resposta a Incidente de Phishing e Execução de Playbook SOC](#10-resposta-a-incidente-de-phishing-e-execução-de-playbook-soc)
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

---

### 5. Fortalecimento de Rede e Avaliação de Risco
* **Atividade:** Elaboração de um plano de defesa em profundidade, selecionando ferramentas e técnicas de Network Hardening para corrigir vulnerabilidades críticas em uma infraestrutura corporativa.
* **Cenário:** Uma organização de mídia social sofreu uma grave violação de dados (vazamento de PII) devido a falhas básicas de segurança. Uma auditoria revelou quatro vulnerabilidades principais: compartilhamento de senhas entre funcionários, uso de senhas de administrador padrão, ausência de regras de firewall e falta de Autenticação Multifator (MFA).
* **Meu Objetivo:** Realizar uma Avaliação de Risco de Segurança para propor soluções técnicas específicas para cada falha encontrada.
* **Entregável:** Relatório de Avaliação de Risco de Segurança com propostas de remediação.
* **[🔗 Link para os arquivos do projeto](./5_Fortalecimento_de_Rede_e_Avaliacao_de_Risco)**

---

### 6. Aplicação do Framework NIST CSF: Resposta a Incidente (ICMP Flood)
* **Atividade:** Elaboração de um relatório de análise de incidente utilizando os cinco pilares do NIST Cybersecurity Framework (CSF): Identificar, Proteger, Detectar, Responder e Recuperar.
* **Cenário:** Uma empresa de multimídia sofreu uma interrupção de 2 horas em sua rede interna devido a um ataque de Negação de Serviço (DoS) do tipo ICMP Flood. O ataque explorou um firewall mal configurado, sobrecarregando os recursos da rede.
* **Meu Objetivo:** Analisar o evento e estruturar um plano de segurança para prevenir recorrências. Mapeei as ações de resposta e melhoria dentro das categorias do NIST CSF.
* **Entregável:** Relatório de Análise de Incidente (Mapeamento NIST CSF).
* **[🔗 Link para os arquivos do projeto](./6_Aplicacao_do_Framework_NIST_CSF_Resposta_a_Incidente)**

---

### 7. Avaliação de Privacidade de Dados e Princípio do Menor Privilégio
* **Atividade:** Análise de um incidente de vazamento de dados (Data Leak) causado por erro humano, avaliando a aplicação do princípio do Menor Privilégio (Least Privilege) com base nas diretrizes do NIST SP 800-53.
* **Cenário:** Uma empresa de tecnologia educacional sofreu um vazamento de dados sensíveis (planos de negócios e análises de clientes) quando um funcionário compartilhou acidentalmente uma pasta interna com um parceiro externo. A investigação revelou que as permissões de acesso não foram revogadas após uma reunião interna, violando o princípio do menor privilégio.
* **Meu Objetivo:** Analisar os fatores que levaram ao vazamento e propor melhorias nos controles de acesso. Utilizei a publicação especial NIST SP 800-53 (Controle AC-6) para fundamentar recomendações que evitassem a recorrência desse erro.
* **Entregável:** Planilha de Análise de Vazamento de Dados e Recomendações de Controle.
* **[🔗 Link para os arquivos do projeto](./7_Avaliacao_de_Privacidade_de_Dados_e_Principio_do_Menor_Privilegio)**

---

### 8. Auditoria de Controle de Acesso e Investigação de Incidente
* **Atividade:** Investigação de uma transação financeira não autorizada através da análise de logs de eventos e diretórios de funcionários, focando na tríade AAA (Autenticação, Autorização e Contabilização).
* **Cenário:** Uma empresa detectou uma transferência bancária suspeita para uma conta desconhecida. Fui encarregado de investigar a origem da transação e identificar quais falhas nos controles de acesso permitiram que isso acontecesse.
* **Meu Objetivo:** Cruzar os dados do Registro de Eventos (IP, data, hora) com o Diretório de Funcionários para identificar o autor da ação e as vulnerabilidades exploradas.
* **Entregável:** Planilha de Avaliação de Controle de Acesso e Recomendações.
* **[🔗 Link para os arquivos do projeto](./8_Auditoria_de_Controle_de_Acesso_e_Investigacao_de_Incidente)**

---

### 9. Análise de Vetor de Ataque Físico e Risco de USB (USB Baiting)
* **Atividade:** Avaliação de riscos e vetores de ataque baseada em um cenário de USB Baiting, com foco em ameaças de engenharia social e vazamento de dados.
* **Cenário:** Durante um exercício de segurança simulando a rotina de um hospital, um pendrive abandonado no estacionamento foi recolhido e aberto em um ambiente seguro (Sandbox). Fui encarregado de analisar as evidências (o conteúdo extraído do dispositivo) para determinar a gravidade do incidente.
* **Meu Objetivo:** Avaliar os arquivos encontrados sob a ótica de um atacante (Attacker Mindset). Analisei a mistura perigosa de dados pessoais do gerente de RH (PII) com documentos corporativos confidenciais (escalas de turnos e dados de novos contratados) e mapeei como isso poderia ser explorado.
* **Entregável:** Relatório de Análise de Risco (focado em ataques físicos e Engenharia Social).
* **[🔗 Link para os arquivos do projeto](./9_Analise_de_Vetor_de_Ataque_Fisico_e_Risco_de_USB)**

---

### 10. Resposta a Incidente de Phishing e Execução de Playbook SOC
* **Atividade:** Triagem e investigação de um alerta de segurança focado em Phishing, seguindo procedimentos operacionais padrão (Playbook) de um Centro de Operações de Segurança (SOC).
* **Cenário:** Atuando como Analista de Nível 1 (Tier 1), recebi um chamado (ticket A-2703) de gravidade média alertando sobre o possível download de malware por um funcionário. O funcionário havia recebido e aberto um anexo de e-mail suspeito disfarçado de currículo para uma vaga de engenharia.
* **Meu Objetivo:** Executar as etapas do Phishing Playbook da organização para avaliar o alerta, analisar os artefatos (cabeçalhos do e-mail, remetente, erros gramaticais) e determinar a veracidade e periculosidade da ameaça.
* **Entregável:** Tíquete de Alerta atualizado (com documentação da investigação e justificativa de escalonamento).
* **[🔗 Link para os arquivos do projeto](./10_Resposta_a_Incidente_de_Phishing_e_Execucao_de_Playbook_SOC)**

---


## 📜 Certificado
* **Status:** Em progresso.
