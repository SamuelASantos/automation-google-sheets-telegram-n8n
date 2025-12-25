# 📊 Automação de Notificações em Tempo Real com Google Sheets, n8n e Telegram

## 📌 Visão Geral

Este projeto apresenta uma automação completa desenvolvida com **n8n**, capaz de monitorar alterações em uma planilha do **Google Sheets** e enviar notificações automáticas em tempo real para o **Telegram** sempre que uma nova linha é adicionada ou atualizada.

A solução foi criada com foco em **produtividade**, **confiabilidade** e **redução de tarefas manuais**, sendo ideal para cenários como:

* Recebimento de leads
* Formulários de contato
* Registros operacionais
* Monitoramento de dados críticos

---

## 🎯 Problema Resolvido

Antes da automação, o acompanhamento das informações dependia de verificação manual da planilha, o que gerava atrasos e risco de falhas humanas.

Com este fluxo automatizado:

* Toda nova informação é detectada automaticamente
* A notificação é enviada instantaneamente
* O responsável é avisado sem precisar acessar a planilha

---

## ⚙️ Funcionamento do Fluxo

```
Google Sheets Trigger
        ↓
Tratamento e formatação dos dados
        ↓
Envio automático da mensagem via Telegram
```

O fluxo permanece ativo em produção e executa verificações periódicas para identificar novas linhas ou atualizações.

---

## 🛠️ Tecnologias Utilizadas

* **n8n** – Plataforma de automação e integração de workflows
* **Google Sheets API** – Monitoramento de dados da planilha
* **Telegram Bot API** – Envio de notificações em tempo real
* **JavaScript Expressions (n8n)** – Tratamento e formatação de dados
* **APIs REST** – Comunicação entre serviços

---

## ✨ Principais Funcionalidades

* 📥 Detecção automática de novas linhas no Google Sheets
* 🕒 Conversão correta de data/hora numérica do Sheets para formato brasileiro
* 📲 Envio de mensagens estruturadas via Telegram
* 🔁 Execução contínua em ambiente de produção
* 🔐 Uso seguro de credenciais (não versionadas)

---

## 📄 Estrutura da Planilha

A planilha utilizada contém os seguintes campos:

* Data/Hora
* Nome
* Email
* Interesse
* Mensagem

Esses dados são capturados dinamicamente e inseridos na mensagem enviada ao Telegram.

---

## 📩 Exemplo de Mensagem Enviada

```
🕒 Data/Hora: 24/12/2025 14:58
👤 Nome: João Silva
📧 Email: joao@email.com
📌 Interesse: Orçamento
💬 Mensagem: Gostaria de mais informações
```

---

## 🔐 Segurança

Este repositório **não contém**:

* Tokens do Telegram
* Client Secret do Google
* IDs sensíveis

As credenciais devem ser configuradas diretamente no n8n ou por variáveis de ambiente.

Um arquivo `.env.example` pode ser utilizado como referência.

---

## 🚀 Como Utilizar (Alto Nível)

1. Criar um bot no Telegram via **@BotFather**
2. Obter o **BOT TOKEN** e o **chat_id**
3. Criar credenciais do Google no **Google Cloud Console**
4. Importar o workflow JSON no n8n
5. Configurar as credenciais
6. Publicar o workflow

---

## 📦 Conteúdo do Repositório

* `workflow.json` – Exportação do workflow do n8n
* `README.md` – Documentação do projeto
* `.env.example` – Exemplo de variáveis de ambiente

---

## 📈 Possíveis Evoluções

* Filtros condicionais por tipo de interesse
* Envio para múltiplos chats ou grupos
* Logs de execução em planilha ou banco de dados
* Dashboard de monitoramento
* Deploy em servidor 24/7

---

## 👨‍💻 Autor

**Samuel**
Desenvolvedor com foco em automação, integração de APIs e soluções orientadas a produtividade.

---

## ⭐ Considerações Finais

Este projeto demonstra a aplicação prática de automação de processos utilizando ferramentas modernas e gratuitas, com foco em soluções reais de negócio. É um case ideal para portfólio técnico e profissional.
