# Visão Geral de Integrações

O poder real do Rhapsodia reside na sua capacidade de se conectar com os ecossistemas de software já existentes na sua empresa, atuando como o "cérebro" que orquestra informações de múltiplas fontes.

---

## 🔌 Conectividade Universal

Existem três formas principais de integrar o Rhapsodia aos seus sistemas:

### 1. Conectores de Dados (RAG)
O Rhapsodia pode ingerir dados de:
- **Arquivos**: PDF, Word, Excel, CSV.
- **Bancos de Dados**: SQL Server, PostgreSQL, MySQL, Oracle.
- **Sistemas Cloud**: SharePoint, Google Drive, Notion.

### 2. Ferramentas de Ação (API/Tools)
Permitem que a IA realize ações em outros sistemas, como criar um pedido no ERP ou disparar um email no CRM.
- **Protocolo**: REST API / Webhooks.
- **Customização**: Scripts Python via [Manual do Desenvolvedor](../manuais/desenvolvedor.md).

### 3. Integrações de IA (Pipes)
Conexão com diversos provedores de modelos, permitindo que você escolha o melhor custo-benefício para cada tarefa.

---

## 🏢 Integrações Específicas com ERPs

Desenvolvemos conectores otimizados para os principais ERPs do mercado:

- [**TOTVS Protheus**](erp-totvs.md): Consultas de faturamento, vendas e estoque em tempo real.
- [**SAP**](erp-sap.md): Automação de lançamentos, auditoria de NFe e gestão de supply chain.

---

## 🏗️ Arquitetura de Integração

A integração segue um fluxo de segurança rigoroso:
1. **Solicitação do Usuário**: A IA entende a intenção.
2. **Chamada de Tool**: A IA decide qual API chamar.
3. **Validação via Filter**: O Rhapsodia valida se o usuário tem permissão para os dados solicitados.
4. **Execução**: O código Python executa a consulta ao sistema externo via `Valves` seguras.

> [!NOTE]
> Para desenvolvedores que desejam criar novas integrações, consulte a nossa [Referência de API](api-reference.md).
