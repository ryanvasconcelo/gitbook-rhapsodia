# Compliance e Segurança de Dados

O Rhapsodia foi construído sob o princípio de "Security by Design". Entendemos que dados corporativos são o ativo mais valioso de uma empresa e devem ser protegidos com os mais altos padrões de compliance.

---

## 🛡️ Pilares de Segurança

### 1. Processamento On-Premise (Local)
Diferente de IAs puramente cloud, o Rhapsodia pode ser instalado dentro dos seus próprios servidores. Isso garante que informações sensíveis nunca saiam da sua rede interna, atendendo aos requisitos mais rígidos de **LGPD**.

### 2. Anonimização via Filtros
Utilizamos **Filters** automáticos que detectam e mascaram dados sensíveis (PII - Personally Identifiable Information) como CPFs, nomes e dados bancários antes que eles sejam processados pelos modelos de linguagem.

### 3. Logs de Auditoria Completos
Cada interação com a plataforma é registrada. O time de compliance pode auditar:
- Quem acessou.
- Quando acessou.
- Qual prompt foi enviado.
- Quais documentos foram carregados.

---

## ⚖️ Conformidade LGPD

O Rhapsodia auxilia sua empresa na conformidade com a Lei Geral de Proteção de Dados:

- **Controle de Acesso (RBAC)**: Garante que apenas pessoas autorizadas acessem bases de conhecimento específicas.
- **Direito ao Esquecimento**: Facilidade para deletar históricos de conversa e documentos indexados de forma definitiva.
- **Transparência**: Relatórios claros sobre como os dados estão sendo utilizados para alimentar os modelos de IA.

---

## 🔒 Infraestrutura e Criptografia

- **Dados em Repouso**: Criptografia AES-256 no banco de dados local.
- **Dados em Trânsito**: Conexão segura via TLS 1.3.
- **Isolamento de Redes**: Possibilidade de rodar em redes "Air-Gapped" (sem internet).

![Editor de Funções de Segurança](../assets/images/function-editor.png)

> [!CAUTION]
> A segurança é uma responsabilidade compartilhada. Mantenha os Filtros de Governança ativos e revise periodicamente as chaves de API e permissões de usuários.
