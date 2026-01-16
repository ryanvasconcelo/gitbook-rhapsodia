# Manual do Administrador - Rhapsodia

## 1. Visão Geral do Papel do Administrador

Como administrador do Rhapsodia, você é responsável por:

- Configurar e manter a plataforma operacional
- Gerenciar usuários e permissões
- Configurar modelos de IA e integrações
- Monitorar custos e uso
- Garantir governança e compliance
- Manter a base de conhecimento atualizada

## 2. Primeiro Acesso e Setup Inicial

### 2.1 Configuração do Administrador Master [4]

Acesse a URL de configuração inicial:

https://rhapsodia.suaempresa.com/auth?setup-configure=true


Este primeiro cadastro criará o usuário administrador master com acesso total ao sistema.

### 2.2 Acessando o Admin Panel

1. Faça login com suas credenciais de admin
2. Clique no ícone de engrenagem no canto superior direito
3. Selecione "Admin Panel"

Principais seções:
- **Settings**: Configurações gerais do sistema
- **Users**: Gestão de usuários
- **Models**: Configuração de modelos de IA
- **Knowledge**: Base de conhecimento
- **Analytics**: Métricas e relatórios

## 3. Configuração de Modelos de IA

### 3.1 Configurando Modelos Cloud [4]

**Admin Panel > Settings > Connections**

#### OpenRouter (Recomendado para Cloud)
yaml
API Key: [sua-chave-openrouter]
API Base URL: https://openrouter.ai/api/v1


Modelos disponíveis após configuração:
- GPT-4o (OpenAI)
- Claude 3.5 Sonnet (Anthropic)
- Gemini 1.5 Pro (Google)
- Llama 3.1 70B (Meta)

#### Testando a Conexão
1. Clique em "Test Connection"
2. Aguarde confirmação verde
3. Selecione modelos para habilitar

### 3.2 Configurando Modelos Locais (On-Premise) [6]

**Para instalações com GPU local:**

#### Download de Modelos Recomendados
bash
# Modelos básicos
ollama pull llama3.1:8b     # 4.7GB - Uso geral
ollama pull mistral:7b      # 4.1GB - Chatbot rápido
ollama pull qwen2.5:14b     # 8.5GB - Análises complexas


#### Performance por Modelo [6]
| Modelo | VRAM | RAM | Qualidade | Velocidade |
|--------|------|-----|-----------|------------|
| llama3.1:8b | 8GB | 16GB | ⭐⭐⭐ | Rápida |
| llama3.1:70b | 40GB | 48GB | ⭐⭐⭐⭐⭐ | Moderada |
| mistral:7b | 6GB | 12GB | ⭐⭐⭐ | Muito rápida |

### 3.3 Configuração de Parâmetros [6]

**Admin Panel > Models > [Modelo] > Parameters**

yaml
num_ctx: 4096          # Contexto máximo
temperature: 0.7       # Criatividade (0-1)
top_p: 0.9            # Nucleus sampling
repeat_penalty: 1.1    # Evita repetições


## 4. Gestão de Usuários e Permissões

### 4.1 Roles Disponíveis [5]

**Admin (Administrador)**
- Acesso total ao sistema
- Gestão de usuários e permissões
- Configuração de modelos e integrações
- Acesso a logs e auditoria
- Gestão de billing e custos

**User (Usuário Padrão)**
- Criar e gerenciar conversas próprias
- Acessar knowledge base autorizada
- Usar modelos permitidos
- Compartilhar conversas
- Visualizar próprio consumo

**Pending (Pendente)**
- Sem acesso até aprovação
- Apenas visualização de página de espera

### 4.2 Criando Usuários [5]

**Método 1: Convite por Email**
1. Admin Panel > Users > Invite
2. Inserir email corporativo
3. Selecionar role
4. Definir quota de tokens (opcional)
5. Enviar convite

**Método 2: Criação Manual**
1. Admin Panel > Users > Create
2. Preencher dados:
   - Nome completo
   - Email corporativo  
   - Senha temporária
   - Role
   - Departamento (tags)

**Método 3: Import em Massa**
1. Preparar arquivo CSV:
csv
nome,email,role,departamento
João Silva,joao@empresa.com,user,financeiro
Maria Santos,maria@empresa.com,user,rh

2. Admin Panel > Users > Import
3. Upload do arquivo
4. Confirmar importação

### 4.3 Configurando Permissões Granulares [5]

Por usuário ou grupo:
- **Modelos permitidos**: Selecionar quais modelos pode usar
- **Upload de documentos**: Sim/Não
- **Compartilhar conversas**: Sim/Não
- **Acessar analytics**: Sim/Não
- **Functions específicas**: Habilitar/Desabilitar
- **Limite de tokens/mês**: Definir quota

## 5. Governança e Compliance

### 5.1 Configuração de Governança [4]

**Admin Panel > Settings > General**

yaml
ENABLE_SIGNUP: false           # Desabilita registro público
DEFAULT_USER_ROLE: user        # Role padrão
USER_PERMISSIONS_ENABLED: true # Aprovação manual
CONTENT_FILTERING: true        # Filtro de conteúdo


### 5.2 System Prompt Corporativo [4][5]

**Admin Panel > Prompts > System Prompts**

Exemplo de system prompt para governança:

Você é o assistente de IA corporativo da [NOME DA EMPRESA].
Seu objetivo é aumentar a produtividade e auxiliar nas operações diárias do negócio.

Diretrizes:
- Mantenha foco em questões profissionais e relacionadas ao negócio
- Solicite esclarecimentos quando necessário
- Forneça respostas estruturadas e acionáveis
- Cite fontes quando utilizar informações específicas da empresa


### 5.3 Políticas de Retenção de Dados

**Admin Panel > Settings > Data**

- Histórico de conversas: 90 dias (padrão)
- Logs de sistema: 30 dias
- Backups: 7 dias
- Analytics: 12 meses

## 6. Base de Conhecimento (RAG)

### 6.1 Criando Collections [6]

**Admin Panel > Knowledge > Create Collection**

Estrutura recomendada:
- "Políticas Internas"
- "Manuais e Procedimentos"
- "Base de Produtos"
- "Documentação Técnica"
- "Templates Corporativos"

### 6.2 Upload e Indexação [6]

**Formatos suportados:**
- PDF (preferencial)
- DOCX, TXT, MD
- CSV (dados tabulares)

**Limitações:**
- Tamanho máximo: 50MB por arquivo
- Tempo de indexação: ~1 min por MB
- Armazenamento vetorial: ~2x tamanho original

### 6.3 Configurando Permissões por Collection

1. Selecione a collection
2. Clique em "Permissions"
3. Defina:
   - Grupos com acesso
   - Visibilidade (Pública/Privada)
   - Permitir edição (Sim/Não)

## 7. Monitoramento e Analytics

### 7.1 Dashboard Principal

**Admin Panel > Analytics**

Métricas disponíveis:
- Usuários ativos (diário/mensal)
- Tokens consumidos por modelo
- Custo estimado em tempo real
- Taxa de adoção por departamento
- Queries mais frequentes
- Tempo médio de resposta

### 7.2 Relatórios Customizados

**Criar Relatório:**
1. Admin Panel > Analytics > Reports
2. Selecionar período
3. Escolher métricas:
   - Uso por usuário
   - Consumo por modelo
   - Documentos processados
   - Workspaces ativos
4. Exportar (PDF/Excel)

### 7.3 Alertas e Notificações

Configurar alertas para:
- Quota de tokens excedida
- Erro de modelo
- Novo usuário pendente
- Backup concluído
- Atualização disponível

## 8. Integrações e APIs

### 8.1 Gerando API Keys [5]

**Admin Panel > Settings > API Keys**

1. Click "Create New Key"
2. Nome descritivo
3. Selecionar permissões:
   - Read (leitura)
   - Write (escrita)
   - Admin (total)
4. Copiar e armazenar com segurança

### 8.2 Endpoints Principais [5]


GET  /api/models       # Listar modelos
POST /api/chat         # Enviar mensagem
GET  /api/knowledge    # Buscar documentos
GET  /api/users        # Listar usuários
GET  /api/analytics    # Obter métricas


### 8.3 Webhooks para Eventos

Configurar webhooks para:
- Nova conversa criada
- Documento processado
- Limite de quota atingido
- Erro de sistema

## 9. Backup e Recuperação

### 9.1 Backup Manual [6]

bash
# Estrutura de backup
/opt/rhapsodia/backups/
├── database/
├── knowledge/
├── configs/
└── logs/


**Não incluir no backup:** pasta `models/` (podem ser baixados novamente)

### 9.2 Backup Automatizado

**Admin Panel > Settings > Backup**

Configurar:
- Frequência: Diária/Semanal
- Horário: 02:00 (fora do expediente)
- Retenção: 7 dias
- Destino: Local/S3/Azure

### 9.3 Procedimento de Recuperação

1. Parar serviços
2. Restaurar backup
3. Verificar integridade
4. Reiniciar serviços
5. Testar funcionalidades

## 10. Manutenção e Troubleshooting

### 10.1 Checklist de Manutenção

**Diário:**
- [ ] Verificar logs de erro
- [ ] Monitorar uso de recursos
- [ ] Aprovar usuários pendentes

**Semanal:**
- [ ] Revisar métricas de uso
- [ ] Atualizar base de conhecimento
- [ ] Verificar espaço em disco
- [ ] Testar backups

**Mensal:**
- [ ] Análise de performance
- [ ] Revisão de permissões
- [ ] Atualização de modelos
- [ ] Relatório executivo
- [ ] Limpeza de dados antigos

### 10.2 Problemas Comuns

**"Modelo não responde"**
1. Verificar API key válida
2. Checar limites de rate
3. Verificar logs: `/var/logs/rhapsodia/`
4. Reiniciar container se necessário

**"Usuário não consegue acessar"**
1. Verificar status do usuário (ativo/pendente)
2. Confirmar role atribuída
3. Checar quotas de tokens
4. Verificar permissões do workspace

**"Documento não é indexado"**
1. Verificar formato suportado
2. Checar tamanho < 50MB
3. Aguardar processamento completo
4. Verificar logs de indexação

### 10.3 Logs e Diagnóstico

**Localização dos logs:**

/var/logs/rhapsodia/
├── access.log      # Acessos
├── error.log       # Erros
├── models.log      # Uso de modelos
└── system.log      # Sistema geral


**Comandos úteis:**
bash
# Últimos erros
tail -f /var/logs/rhapsodia/error.log

# Uso de recursos
docker stats rhapsodia

# Status dos serviços
docker-compose ps


## 11. Segurança

### 11.1 Configurações de Segurança

**Admin Panel > Settings > Security**

- Força de senha mínima
- 2FA obrigatório para admins
- Timeout de sessão: 30 minutos
- Rate limiting: 60 req/min
- IP whitelist (opcional)

### 11.2 Auditoria

Todos os eventos são registrados:
- Login/Logout
- Criação/Modificação de usuários
- Upload de documentos
- Mudanças de configuração
- Acesso a dados sensíveis

### 11.3 Compliance LGPD

- Anonimização de dados
- Direito ao esquecimento
- Exportação de dados pessoais
- Consentimento documentado
- Relatórios de compliance

## 12. Suporte e Recursos

### 12.1 Canais de Suporte [7]

- **Email técnico**: suporte@pktech.com.br
- **Documentação**: `/suporte/`
- **FAQ**: `/suporte/faq.md`
- **SLA**: 
  - Crítico: 2 horas
  - Alto: 6 horas
  - Médio: 24 horas
  - Baixo: 72 horas

### 12.2 Recursos Adicionais

- [Guia de Integrações](../integracoes/visao-geral.md)
- [Biblioteca de Automações](../automacoes/biblioteca.md)
- [Manual do Desenvolvedor](desenvolvedor.md)
- [Troubleshooting Avançado](../suporte/troubleshooting.md)

---