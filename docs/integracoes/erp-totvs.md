# Integração com TOTVS Protheus

A integração entre o Rhapsodia e o TOTVS Protheus permite que sua equipe consulte dados de faturamento, pedidos e estoque diretamente via chat, eliminando a dependência de relatórios manuais e BI complexos.

---

## 🏗️ Como Funciona

A integração utiliza uma **Tool de Conexão SQL** dedicada que se comunica de forma segura com o Banco de Dados do Protheus (SQL Server/Oracle).

### Fluxo de Dados:
1. **Intenção**: O usuário digita: "Quais foram as maiores vendas de ontem?"
2. **Processamento**: A IA traduz a intenção em parâmetros de consulta.
3. **Execução**: O Rhapsodia executa uma query segura nas tabelas do ERP (ex: `SD2`, `SF2`, `SA1`).
4. **Visualização**: O resultado retorna em formato de texto analítico ou gráficos dinâmicos.

---

## 🛠️ Configuração Técnica (Exemplo Generalista)

Para habilitar esta integração, o desenvolvedor deve criar uma Tool que use as **Valves** para gerenciar as credenciais do banco.

```python
class Tools:
    class Valves(BaseModel):
        DB_HOST: str = Field(default="10.0.0.1", description="IP do SQL Server Protheus")
        DB_USER: str = Field(default="user_rhapsodia", description="Usuário de Leitura")
        DB_PASS: str = Field(default="senha_segura", description="Senha")
        DB_NAME: str = Field(default="p12_prod", description="Noma do Banco de Dados")

    def _get_connection(self):
        # Implementa a conexão usando pymssql ou pyodbc
        pass
```

### Consultas Suportadas:
- **Faturamento**: Tabela `SD2010` (Itens de Nota Fiscal).
- **Vendas**: Tabela `SC5010` (Pedidos de Venda).
- **Clientes**: Tabela `SA1010`.
- **Produtos**: Tabela `SB1010`.

---

## 📊 Visualização de Dados

![Gráfico de Vendas ERP](../assets/images/agent-settings.png)

O Rhapsodia pode gerar gráficos de barras, linhas ou pizza baseados nos dados do Protheus em tempo real. Basta o Agente de Vendas estar configurado com os scripts de visualização (ex: `matplotlib`).

---

## 🛡️ Segurança e Performance

- **Acesso Read-Only**: Utilize sempre um usuário de banco com permissões apenas de leitura (`SELECT`).
- **NOLOCK**: Todas as queries enviadas pelo Rhapsodia devem utilizar `WITH (NOLOCK)` para não impactar a performance do ERP em produção.
- **Filtros de Filial**: O Rhapsodia pode ser configurado para que usuários de uma filial específica vejam apenas dados da sua própria unidade.

> [!IMPORTANT]
> A integração via SQL direto é a mais rápida, mas também é possível integrar via **REST API do Protheus** caso sua infraestrutura exija um barramento de integração.
