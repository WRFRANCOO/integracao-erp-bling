# Integração Bling com Google Workspace e ChatGPT

##  Objetivo
Desenvolver uma solução de integração entre o ERP **Bling**, o **Google Workspace** e o **ChatGPT**, permitindo a consulta automatizada de produtos, estoque, preços e localização diretamente no ERP, utilizando um agente conversacional.

O projeto foi concebido em um cenário de **orçamento extremamente limitado**, onde o único serviço pago disponível era o **ChatGPT Plus**.

---

##  Descrição da Solução
A solução foi construída utilizando exclusivamente ferramentas de baixo custo ou gratuitas, com foco em automação, integração via API e contorno de limitações técnicas.

### Fluxo geral:
1. Consulta de produtos no ERP Bling via API
2. Processamento e armazenamento dos dados em Google Sheets
3. Exposição dos dados via Webhook no Google Apps Script
4. Integração do ChatGPT com o Webhook por meio de um proxy no Cloudflare
5. Retorno estruturado das informações ao agente do ChatGPT

---

##  Tecnologias Utilizadas
- ERP Bling (API REST)
- Google Apps Script
- Google Sheets
- Cloudflare (proxy)
- ChatGPT (agente personalizado)
- Git & GitHub

---

##  Restrições e Desafios
- Orçamento inexistente para infraestrutura ou servidores dedicados
- Limitação de tempo de execução do Google Apps Script (máx. 4m59s)
- Necessidade de atualização periódica dos dados sem intervenção manual
- Integração segura entre ChatGPT e Google Apps Script

---

##  Soluções Implementadas
- Uso do **Google Apps Script** como camada de integração gratuita
- Criação de uma planilha como base intermediária de dados
- Implementação de um **Webhook** para padronizar requisições e respostas
- Uso do **Cloudflare** como proxy entre ChatGPT e Google Script
- Desenvolvimento de uma lógica de execução em ciclos:
  - O script roda por até 5 minutos
  - Aguarda 1 minuto
  - Retoma a execução até concluir a importação
- Atualização automática da planilha a cada **8 horas**

---

##  Resultado
A solução permitiu:
- Consultas rápidas e estruturadas via ChatGPT
- Eliminação de custos com servidores ou APIs pagas
- Centralização de dados do ERP em uma camada acessível
- Automação estável respeitando os limites da plataforma

---

##  Aprendizados
- Integração entre sistemas com recursos limitados
- Uso avançado de Google Apps Script
- Arquitetura alternativa para ambientes sem budget
- Comunicação entre agentes conversacionais e APIs externas
- Contorno de restrições de execução e escalabilidade

---

##  Status do Projeto
Em evolução — projeto de estudo aplicado com foco em integração e automação real.
