# Manual do Usuário - Rhapsodia

## 1. Introdução

O Rhapsodia é sua plataforma corporativa de IA que combina os melhores modelos de linguagem do mundo (GPT-4, Claude, Gemini) com a segurança de uma infraestrutura privada [5].

### O que você pode fazer

- Conversar com múltiplos modelos de IA
- Analisar documentos e planilhas
- Gerar conteúdos profissionais
- Automatizar tarefas repetitivas
- Acessar a base de conhecimento corporativa
- Colaborar em workspaces compartilhados

## 2. Interface Principal

### 2.1 Áreas da Interface [5]

**Barra Lateral Esquerda**
- Histórico de conversas (organizado por data)
- Workspaces (projetos compartilhados)
- Prompts salvos
- Documentos recentes

**Área Central**
- Campo de entrada de mensagem
- Área de visualização de respostas
- Indicador de modelo ativo
- Status de processamento

**Barra Superior**
- Seletor de modelos de IA
- Configurações de conversa
- Menu do usuário
- Indicador de tokens usados

### 2.2 Atalhos de Teclado [3]

| Atalho | Função |
|--------|---------|
| `Ctrl + /` | Nova conversa |
| `Ctrl + K` | Buscar conversas |
| `Ctrl + B` | Mostrar/ocultar barra lateral |
| `Ctrl + Enter` | Enviar mensagem |
| `Ctrl + Shift + C` | Copiar última resposta |
| `Ctrl + Shift + E` | Exportar conversa |

## 3. Conversando com a IA

### 3.1 Iniciando uma Conversa

1. Clique em "Nova Conversa" ou use `Ctrl + /`
2. Digite sua pergunta ou comando
3. Pressione Enter ou clique em Enviar
4. Aguarde a resposta (indicador de digitação aparece)

### 3.2 Modos de Conversa [5]

**Modo Assistente** (Padrão)
- Conversação natural e livre
- Ideal para perguntas gerais e brainstorming

**Modo Consulta**
- Respostas objetivas e diretas
- Melhor para busca de informações específicas

**Modo Criativo**
- Máxima liberdade de geração
- Usado para conteúdo criativo e inovador

**Modo Preciso**
- Respostas determinísticas e consistentes
- Recomendado para análises técnicas

### 3.3 Selecionando Modelos

**GPT-4o** 
- Uso: Tarefas gerais, redação, análise
- Velocidade: Rápida
- Custo: Médio

**Claude 3.5 Sonnet**
- Uso: Análises complexas, código, raciocínio
- Velocidade: Moderada  
- Custo: Alto

**Gemini 1.5 Pro**
- Uso: Documentos longos (até 1M tokens)
- Velocidade: Rápida
- Custo: Baixo

**Llama 3.1** (se local) [6]
- Uso: Processamento 100% privado
- Velocidade: Depende da GPU
- Custo: Zero (após setup)

## 4. Trabalhando com Documentos

### 4.1 Upload de Arquivos

**Formatos Suportados**
- PDF (recomendado)
- Word (.docx)
- Excel (.xlsx, .csv)
- PowerPoint (.pptx)
- Texto (.txt, .md)
- Código (múltiplas linguagens)

**Processo de Upload**
1. Clique no ícone de clip 📎
2. Selecione o arquivo (máx. 50MB)
3. Aguarde processamento
4. Arquivo aparece anexado à conversa

### 4.2 Comandos para Documentos


"Resuma este documento em 5 pontos principais"
"Extraia todas as datas e valores mencionados"
"Compare este contrato com o modelo padrão"
"Crie uma apresentação baseada neste relatório"
"Identifique riscos e oportunidades neste documento"


### 4.3 Análise de Planilhas


"Calcule o total por categoria"
"Identifique tendências nos últimos 12 meses"
"Crie um gráfico com estes dados"
"Encontre anomalias ou valores discrepantes"
"Gere um relatório executivo desta planilha"


## 5. Base de Conhecimento (RAG) [5]

### 5.1 Acessando Conhecimento Corporativo

Use o prefixo `@conhecimento` para buscar em documentos internos:


@conhecimento qual é nossa política de férias?
@conhecimento procedimento para compras acima de R$ 10.000
@conhecimento lista de fornecedores homologados


### 5.2 Collections Disponíveis

- Políticas e Procedimentos
- Manuais Técnicos
- Contratos e Templates
- Base de Produtos
- Documentação de Sistemas

## 6. Prompts e Templates

### 6.1 Biblioteca de Prompts

**Acessar Templates**
1. Menu lateral > Prompts
2. Escolha categoria (Financeiro, RH, Vendas, etc.)
3. Clique para usar
4. Personalize conforme necessário

### 6.2 Criando Seus Próprios Templates

1. Escreva e teste seu prompt
2. Clique nos três pontos > "Salvar como Template"
3. Nomeie e categorize
4. Adicione variáveis com `{{variavel}}`

**Exemplo de Template com Variáveis**

Escreva um email de follow-up para {{nome_cliente}} sobre 
{{produto/servico}}. Última interação foi há {{dias}} dias. 
Tom: {{formal/casual}}. Incluir CTA para {{acao_desejada}}.


## 7. Workspaces e Colaboração

### 7.1 Criando um Workspace

1. Barra lateral > Workspaces > "+"
2. Nome: "[Projeto] - [Departamento]"
3. Descrição do objetivo
4. Adicionar membros por email

### 7.2 Permissões

- **Visualizar**: Apenas leitura
- **Contribuir**: Adicionar mensagens
- **Editar**: Modificar configurações
- **Admin**: Controle total

### 7.3 Compartilhando Conversas

1. Abra a conversa
2. Clique em "Compartilhar"
3. Escolha:
   - Link público (qualquer um com link)
   - Específico (escolher usuários)
   - Workspace (todos os membros)

## 8. Automações

### 8.1 Automações Disponíveis

**Financeiro**
- Análise automática de DRE
- Conciliação bancária assistida
- Previsão de fluxo de caixa

**RH**
- Triagem de currículos
- Geração de descrições de cargo
- Respostas a dúvidas frequentes

**Vendas**
- Qualificação de leads
- Geração de propostas
- Follow-ups automatizados

### 8.2 Configurando uma Automação

1. Admin Panel > Automações
2. Escolher template
3. Configurar:
   - Gatilho (horário, evento, webhook)
   - Dados de entrada
   - Modelo de IA
   - Ação de saída (email, API, arquivo)
4. Testar antes de ativar

## 9. Functions e Ferramentas [5]

### 9.1 Functions Disponíveis

- **Web Search**: Busca informações atualizadas
- **Calculator**: Cálculos complexos
- **Code Interpreter**: Execução de código
- **Image Generator**: Criação de imagens
- **API Caller**: Integração com sistemas externos

### 9.2 Ativando Functions


/search notícias sobre [tópico] última semana
/calculate ROI com investimento 100000 e retorno 150000
/image logo minimalista para empresa de tecnologia

## 10. Exportação e Relatórios

### 10.1 Formatos de Exportação

- **PDF**: Formatação preservada
- **Word**: Editável
- **TXT**: Texto puro
- **JSON**: Para integração
- **Markdown**: Documentação técnica

### 10.2 Gerando Relatórios

1. Menu > Relatórios
2. Selecionar período
3. Escolher métricas:
   - Conversas criadas
   - Tokens consumidos
   - Tempo economizado
   - Documentos processados
4. Exportar ou agendar envio

## 11. Configurações Pessoais

### 11.1 Preferências

**Interface**
- Tema: Claro/Escuro/Auto
- Idioma: Português/Inglês
- Tamanho da fonte
- Densidade da interface

**Comportamento**
- Modelo padrão
- Temperatura (criatividade)
- Máximo de tokens
- Auto-save

### 11.2 Notificações

- Respostas concluídas
- Menções em workspaces
- Limites de quota
- Atualizações do sistema

## 12. Boas Práticas

### 12.1 Escrevendo Prompts Efetivos

**Estrutura CLEAR**
- **C**ontexto: Forneça background
- **L**inguagem: Especifique tom e estilo
- **E**xemplos: Mostre o que espera
- **A**ção: Seja claro sobre o resultado
- **R**estrições: Defina limites

### 12.2 Segurança da Informação

**FAZER**
- Use workspaces para projetos sensíveis
- Verifique permissões antes de compartilhar
- Remova dados pessoais de documentos
- Use senhas fortes

**NÃO FAZER**
- Compartilhar credenciais
- Upload de dados sem autorização
- Ignorar classificação de dados
- Usar para fins pessoais

### 12.3 Otimização de Custos

- Use o modelo adequado para cada tarefa
- Evite conversas desnecessariamente longas
- Reutilize templates e prompts
- Monitore consumo regularmente
- Delete conversas antigas

## 13. Resolução de Problemas

### 13.1 Problemas Comuns

**"Resposta muito lenta"**
- Verifique modelo selecionado
- Reduza tamanho do contexto
- Tente em horário alternativo

**"Erro ao processar documento"**
- Confirme formato suportado
- Verifique tamanho < 50MB
- Tente converter para PDF

**"Não encontra informação na base"**
- Verifique se tem acesso à collection
- Refine os termos de busca
- Contate admin para indexação

### 13.2 Onde Buscar Ajuda

1. **No sistema**: Digite `/help`
2. **FAQ**: [Perguntas Frequentes](../suporte/faq.md)
3. **Admin local**: Seu administrador Rhapsodia
4. **Suporte**: suporte@pktech.com.br [4]

## 14. Atualizações e Novidades

### 14.1 Próximas Features [5]

- Agentes autônomos com memória
- Integração Microsoft 365
- Suporte a vídeos
- Analytics preditivo
- Marketplace de functions

### 14.2 Como se Manter Atualizado

- Leia notas de release mensais
- Participe de webinars
- Teste features em beta
- Sugira melhorias

## Anexo: Referência Rápida

### Comandos Slash

| Comando | Função |
|---------|---------|
| `/help` | Ajuda geral |
| `/clear` | Limpar conversa |
| `/search` | Buscar na web |
| `/image` | Gerar imagem |
| `/export` | Exportar conversa |
| `/models` | Listar modelos |
| `/usage` | Ver consumo |

### Limites do Sistema

- Upload: 50MB por arquivo
- Contexto: 128k tokens (GPT-4)
- Conversas: Ilimitadas
- Histórico: 90 dias
- Workspaces: 10 por usuário

---