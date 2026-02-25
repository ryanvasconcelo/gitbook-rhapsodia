# Integração com SAP

A integração do Rhapsodia com o ecossistema SAP (S/4HANA ou ECC) permite automatizar auditorias de notas fiscais, consultas de estoque e gestão de mestre de materiais através de uma interface de chat intuitiva.

---

## 🏗️ Modelos de Integração

O Rhapsodia suporta três caminhos principais para conectar-se ao SAP:

### 1. SAP OData Services (Recomendado)
Uso de serviços RESTful nativos do SAP Gateway. É a forma mais moderna e segura de integrar.
- **Vantagem**: Segue as regras de negócio e permissões configuradas no SAP.
- **Segurança**: Autenticação via OAuth2 ou Basic Auth.

### 2. SAP RFC (Remote Function Call)
Conexão direta via protocolos proprietários SAP.
- **Vantagem**: Acesso a BAPIs e funções legadas sem necessidade de Gateway.
- **Requisito**: Instalação do conector `pyrfc` no ambiente do Rhapsodia.

### 3. Conector de Banco de Dados (HANA)
Consulta direta ao banco de dados SAP HANA.
- **Vantagem**: Performance extrema para grandes volumes de dados.
- **Filtro**: Recomenda-se o uso de Views de Cálculo (Calculation Views).

---

## 🎯 Casos de Uso Comuns

- **Auditoria de NFe**: Verificação automática de inconsistências entre o recebimento físico e o lançamento no SAP.
- **Status de Ordem de Compra**: Consulta instantânea do status de pedidos para fornecedores.
- **Inventory Check**: Consulta de níveis de estoque por depósito e planta.
- **Mestre de Materiais**: Criação ou enriquecimento de dados de materiais usando IA.

---

## 🛠️ Exemplo de Fluxo

1. **Usuário**: "SAP, qual é o status da ordem de compra 4500123?"
2. **Agente SAP**: Chama a BAPI `BAPI_PO_GETDETAIL`.
3. **Processamento**: A IA interpreta o retorno do SAP, verifica se houve atrasos e responde: "A ordem está com status 'Liberada', com entrega prevista para amanhã."

---

## 🔒 Segurança e Compliance

- **Mapeamento de Usuário**: O Rhapsodia pode mapear o usuário atual para um usuário específico do SAP para respeitar a trilha de auditoria.
- **Data Hardening**: Filtros para ocultar informações confidenciais de precificação ou dados sensíveis de RH.

> [!NOTE]
> A implementação da integração SAP exige o envolvimento do time de Basis e Desenvolvedores ABAP para garantir a abertura correta das portas de comunicação.
