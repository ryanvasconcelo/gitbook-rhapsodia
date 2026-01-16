# Jornada do Administrador - Rhapsodia

## Dia 1: Setup Inicial (4-6 horas)

### Manhã - Primeiro Acesso como Admin

**08:00 - Acesso ao Sistema**
1. Receba as credenciais da sua conta de administrador
2. Acesse https://rhapsodia.suaempresa.com
3. Faça login com email corporativo e senha

**08:30 - Navegação pelo Admin Panel**
Acesse: Admin Panel (ícone de engrenagem no canto superior)
- Settings: Configurações gerais
- Users: Gestão de usuários
- Models: Configuração de modelos
- Knowledge: Base de conhecimento
- Analytics: Métricas e consumo

### Tarde - Configurações Essenciais

**14:00 -  Limites e Quotas**
Admin Panel > Settings > Interface
Token Limit per Request: 4096 (recomendado)
Max Requests per Minute: 60
Enable Rate Limiting: Sim

## Dia 2: Gestão de Usuários
**Criação de Usuários e Roles**
Roles Padrão Disponíveis:

Admin (Administrador)
Acesso total ao sistema
Gestão de usuários e permissões
Configuração de modelos e integrações
Acesso a logs e auditoria
Gestão de billing e custos

User (Usuário Padrão)
Criar e gerenciar conversas próprias
Acessar base de conhecimento autorizada
Usar modelos permitidos
Compartilhar conversas
Visualizar próprio consumo

Pending (Pendente)
Sem acesso até aprovação
Apenas visualização de página de espera

**Processo de Criação de Usuários**
Criação Manual:
Admin Panel > Users > Create

Preencher:
Nome completo
Email corporativo
Senha
Role
Departamento (tags)

**Configuração de Permissões Granulares**
Por usuário ou grupo:
Modelos permitidos (Chat-GPT, Claude, etc.)
Upload de documentos (Sim/Não)
Compartilhar conversas (Sim/Não)
Acessar analytics (Sim/Não)
Functions específicas
Limite de tokens/mês

## Dia 3-5: Base de Conhecimento
**Criação de Collections**
Passo 1: Estruturar Collections
Admin Panel > Knowledge > Create Collection

Sugestões de organização:
"Políticas Internas"
"Manuais e Procedimentos"
"Base de Produtos"
"Documentação Técnica"
"Templates Corporativos"

Passo 2: Upload de Documentos
Formatos suportados:
PDF (preferencial)
DOCX, TXT, MD
CSV (dados tabulares)

Limites:
Tamanho máximo: 50MB por arquivo
Indexação: ~1 min por MB
Armazenamento: ~2x tamanho original

Passo 3: Configurar Permissões
Por Collection:
Grupos com acesso
Visibilidade (Pública/Privada)
Permitir edição (Sim/Não)
Teste de Recuperação
Acesse como usuário teste
No chat, use: "@conhecimento [pergunta]"
Verifique se retorna informações corretas
Ajuste embeddings se necessário

## Semana 2: Customização Avançada
**System Prompts Corporativos**
Configurar Mensagem Global
Admin Panel > Prompts > System Prompts
Você é o assistente de IA corporativo da [NOME DA EMPRESA].
Seu objetivo é aumentar a produtividade e auxiliar nas operações diárias.

Diretrizes:
- Sempre mantenha tom profissional
- Priorize segurança da informação
- Cite fontes quando usar documentos internos
- Não compartilhe informações sensíveis

**Templates por Departamento**
Criar templates específicos:
Financeiro: Análises e relatórios
RH: Políticas e procedimentos
Vendas: Propostas e follow-ups
TI: Suporte e documentação
Jurídico: Contratos e pareceres

**Configuração de Workspaces**
Criar Workspace Departamental
Admin Panel > Workspaces > Create
Definir:
Nome: "[Departamento] - [Projeto]"
Membros: Adicionar
Permissões: Read/Write por membro
Retenção: Período de histórico

Configurar Isolamento
Conversas privadas por workspace
Knowledge base específica
Modelos permitidos
Budget separado

## Semana 3: Integrações
**API e Webhooks**
Gerar API Keys
Admin Panel > Settings > API Keys

Create New Key
Definir nome descritivo
Selecionar permissões
Copiar e armazenar com segurança
Endpoints Principais

/api/chat - Enviar mensagens
/api/models - Listar modelos
/api/knowledge - Gestão de documentos
/api/users - Gestão de usuários
/api/analytics - Métricas

**Integração com Sistemas**
Configuração Básica:

Admin Panel > Integrations
Selecionar sistema
Inserir credenciais
Mapear campos
Testar conexão
Monitoramento Contínuo
Dashboard de Métricas

**KPIs Principais:**
Usuários ativos/dia
Tokens consumidos/modelo
Custo estimado/mês
Taxa de adoção por depto
Queries mais frequentes
Relatórios Semanais

Gerar Relatório:
Admin Panel > Analytics > Reports
Selecionar período
Escolher métricas
Exportar PDF ou planilha

Análise de Custos:
Consumo por usuário
Consumo por modelo
Projeção mensal
Alertas de quota
Manutenção Preventiva

**Checklist Semanal:**
Revisar logs de erro
Verificar espaço em disco
Atualizar base de conhecimento
Aprovar usuários pendentes
Backup de configurações

**Checklist Mensal:**
Análise de performance
Revisão de permissões
Atualização de modelos
Limpeza de conversas antigas

Relatório executivo
Troubleshooting Comum
Problemas Frequentes
"Modelo não responde"

Verificar API key válida
Checar limites de rate
Reiniciar container se local
"Usuário sem acesso"

Confirmar role atribuída
Verificar status (ativo/pendente)
Checar quotas de tokens
"Documento não indexado"

Verificar formato suportado
Checar tamanho < 50MB
Aguardar processamento completo
Canais de Suporte

Email técnico: suporte@pktech.com.br

**Métricas de sucesso**
Após completar a jornada:
10+ usuários cadastrados
3+ collections de conheimento
5+ templates configurados
Integrações testadas

Parabéns! Você agora é um Administrador Certificado Rhapsodia.