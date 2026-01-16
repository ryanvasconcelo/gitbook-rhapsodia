# Biblioteca de Casos de Uso - Rhapsodia

Esta biblioteca contém casos de uso práticos e testados para acelerar a adoção do Rhapsodia na sua empresa. Cada caso inclui o prompt exato, resultado esperado e ROI estimado.

## Visão Geral

| Caso | Departamento | Tempo Antes | Tempo Depois | ROI |
|------|--------------|-------------|--------------|-----|
| Análise de DRE | Financeiro | 4 horas | 5 minutos | 98% |
| Triagem de Currículos | RH | 2 dias | 10 minutos | 99% |
| Proposta Comercial | Vendas | 2 horas | 5 minutos | 96% |
| Análise de Contrato | Jurídico | 3 horas | 15 minutos | 92% |
| Relatório Gerencial | Operações | 4 horas/semana | Automático | 100% |
| Kit de Onboarding | RH | 1 dia | 15 minutos | 97% |

---

## Caso 1: Análise de DRE em 30 Segundos

### Departamento
Financeiro

### Contexto do Problema
Analistas financeiros gastam horas interpretando Demonstrativos de Resultado, cruzando dados e identificando variações significativas para reportar à diretoria.

### Antes vs Depois
- **Antes**: 4 horas de análise manual por DRE
- **Depois**: 5 minutos com análise completa e insights

### Passo a Passo

1. Acesse o Rhapsodia e inicie nova conversa
2. Clique no ícone de clip para upload [3]
3. Anexe o arquivo da DRE (PDF ou Excel)
4. Cole o prompt abaixo
5. Revise e ajuste conforme necessário

### Prompt Exato


Analise esta DRE (Demonstração do Resultado do Exercício) e forneça:

1. RESUMO EXECUTIVO
   - Resultado líquido e margem
   - Principais destaques (positivos e negativos)

2. ANÁLISE DE VARIAÇÕES
   - Compare com período anterior (se disponível)
   - Identifique variações acima de 10%
   - Explique possíveis causas

3. INDICADORES-CHAVE
   - Margem bruta
   - Margem operacional
   - Margem líquida
   - EBITDA (se possível calcular)

4. PONTOS DE ATENÇÃO
   - Custos que cresceram acima da receita
   - Despesas atípicas
   - Riscos identificados

5. RECOMENDAÇÕES
   - 3 ações prioritárias baseadas nos dados

Formato: Use tabelas para comparativos e bullets para insights.
Tom: Executivo, direto ao ponto.


### Resultado Esperado

O Rhapsodia retornará uma análise estruturada contendo:
- Resumo executivo de 3-5 linhas
- Tabela comparativa de variações
- Lista de indicadores calculados
- Alertas de pontos críticos
- Recomendações acionáveis

### Variações do Prompt

**Para comparativo mensal:**

Adicione ao prompt: "Compare os últimos 3 meses e identifique tendências"


**Para apresentação à diretoria:**

Adicione ao prompt: "Formate como slides executivos com no máximo 5 bullets por seção"


**Para foco em custos:**

Adicione ao prompt: "Foque especialmente na análise de custos e despesas operacionais"


---

## Caso 2: Triagem de 100 Currículos em 10 Minutos

### Departamento
RH / Recrutamento

### Contexto do Problema
Processos seletivos com alto volume de candidatos consomem dias de trabalho manual do RH para triagem inicial, muitas vezes com critérios inconsistentes entre avaliadores.

### Antes vs Depois
- **Antes**: 2 dias para triar 100 currículos
- **Depois**: 10 minutos com ranking e justificativas

### Passo a Passo

1. Compile os currículos em uma pasta ou arquivo consolidado
2. Inicie nova conversa no Rhapsodia
3. Faça upload dos currículos (suporta múltiplos arquivos) [3]
4. Cole o prompt com os requisitos da vaga
5. Receba ranking ordenado por aderência

### Prompt Exato


Você é um especialista em recrutamento e seleção. Analise os currículos anexados para a seguinte vaga:

REQUISITOS DA VAGA:
- Cargo: [INSERIR CARGO]
- Experiência mínima: [X] anos em [ÁREA]
- Formação: [REQUISITOS DE FORMAÇÃO]
- Competências técnicas obrigatórias: [LISTAR]
- Competências técnicas desejáveis: [LISTAR]
- Soft skills importantes: [LISTAR]
- Idiomas: [SE APLICÁVEL]

TAREFA:
1. Analise cada currículo contra os requisitos
2. Atribua uma nota de 0-100 para aderência
3. Classifique em: APROVADO / TALVEZ / REPROVADO

FORMATO DE SAÍDA:
Para cada candidato, forneça:

| Candidato | Nota | Status | Pontos Fortes | Gaps | Recomendação |
|-----------|------|--------|---------------|------|--------------|

Ao final, liste:
- TOP 5 candidatos para entrevista imediata
- Candidatos para banco de talentos
- Principais motivos de reprovação (para feedback)

Seja objetivo e baseie-se apenas nas informações dos currículos.


### Resultado Esperado

- Tabela rankeada de todos os candidatos
- Nota de aderência objetiva (0-100)
- Justificativa para cada classificação
- Lista priorizada para próxima fase
- Insights sobre o pool de candidatos

### Variações do Prompt

**Para vaga técnica:**

Adicione: "Dê peso extra para certificações e projetos práticos na área"


**Para vaga de liderança:**

Adicione: "Priorize experiência em gestão de equipes e resultados mensuráveis"


**Com fit cultural:**

Adicione: "Considere também aderência aos nossos valores: [LISTAR VALORES]"


---

## Caso 3: Proposta Comercial Personalizada em 5 Minutos

### Departamento
Vendas / Comercial

### Contexto do Problema
Vendedores gastam horas montando propostas do zero ou adaptando templates genéricos que não refletem as necessidades específicas de cada cliente.

### Antes vs Depois
- **Antes**: 2 horas por proposta personalizada
- **Depois**: 5 minutos com proposta completa e argumentação

### Passo a Passo

1. Reúna informações do cliente (briefing, site, conversas anteriores)
2. Inicie nova conversa no Rhapsodia
3. Se tiver documentos do cliente, faça upload [3]
4. Cole o prompt com contexto completo
5. Revise, ajuste valores e envie

### Prompt Exato


Crie uma proposta comercial profissional com as seguintes informações:

DADOS DO CLIENTE:
- Empresa: [NOME]
- Segmento: [SEGMENTO]
- Porte: [PEQUENO/MÉDIO/GRANDE]
- Contato: [NOME DO DECISOR]
- Cargo: [CARGO]
- Dor principal: [PROBLEMA QUE QUER RESOLVER]
- Orçamento estimado: [SE SOUBER]

NOSSA SOLUÇÃO:
- Produto/Serviço: [DESCREVER]
- Diferencial: [O QUE NOS DESTACA]
- Investimento: [VALOR OU RANGE]
- Prazo de entrega/implantação: [TEMPO]

ESTRUTURA DA PROPOSTA:

1. CAPA
   - Título impactante
   - Logo placeholder
   - Data

2. ENTENDIMENTO DO CENÁRIO
   - Resumo da situação atual do cliente
   - Desafios identificados
   - Impacto de não resolver

3. SOLUÇÃO PROPOSTA
   - O que entregaremos
   - Como resolve cada dor
   - Metodologia/abordagem

4. BENEFÍCIOS ESPERADOS
   - ROI estimado
   - Ganhos tangíveis
   - Ganhos intangíveis

5. INVESTIMENTO
   - Tabela de preços
   - Condições de pagamento
   - Validade da proposta

6. CRONOGRAMA
   - Fases de implementação
   - Marcos principais

7. PRÓXIMOS PASSOS
   - CTA claro
   - Contatos

Tom: Profissional, consultivo, focado em valor.
Tamanho: Máximo 5 páginas.


### Resultado Esperado

- Proposta completa e estruturada
- Argumentação personalizada para o cliente
- Seção de ROI com números
- CTA claro para fechamento
- Pronta para diagramação

### Variações do Prompt

**Para proposta técnica:**

Adicione: "Inclua seção de especificações técnicas e requisitos de infraestrutura"


**Para renovação de contrato:**

Adicione: "Destaque resultados já alcançados e melhorias propostas para renovação"


**Para upsell:**

Adicione: "Foque em complementaridade com serviços já contratados"


---

## Caso 4: Análise de Contrato com Identificação de Riscos

### Departamento
Jurídico / Compliance

### Contexto do Problema
Revisão de contratos exige leitura minuciosa de dezenas de páginas para identificar cláusulas de risco, prazos críticos e condições desfavoráveis, consumindo horas do time jurídico.

### Antes vs Depois
- **Antes**: 3 horas por contrato de média complexidade
- **Depois**: 15 minutos com mapeamento completo de riscos

### Passo a Passo

1. Acesse o Rhapsodia e inicie nova conversa
2. Faça upload do contrato em PDF [3]
3. Cole o prompt de análise
4. Receba mapeamento estruturado de riscos
5. Aprofunde pontos específicos com follow-ups

### Prompt Exato


Você é um advogado corporativo experiente. Analise este contrato e forneça um parecer estruturado:

TIPO DE ANÁLISE:
- [ ] Contrato novo (estamos recebendo)
- [ ] Contrato nosso (estamos enviando)
- [ ] Renovação
- [ ] Aditivo

FOCO DA ANÁLISE:

1. DADOS GERAIS
   - Partes envolvidas
   - Objeto do contrato
   - Valor total
   - Vigência
   - Foro

2. CLÁUSULAS CRÍTICAS
   Para cada cláusula relevante, indique:
   - Número/Seção
   - Resumo do conteúdo
   - Nível de risco: ALTO / MÉDIO / BAIXO
   - Justificativa do risco
   - Sugestão de alteração

3. PONTOS DE ATENÇÃO
   - Multas e penalidades
   - Cláusulas de rescisão
   - Limitação de responsabilidade
   - Confidencialidade
   - Propriedade intelectual
   - Exclusividade
   - Renovação automática
   - Reajuste de valores

4. PRAZOS IMPORTANTES
   - Listar todos os prazos mencionados
   - Alertar sobre prazos curtos ou desfavoráveis

5. CLÁUSULAS AUSENTES
   - Identificar proteções que deveriam constar
   - Sugerir inclusões

6. PARECER FINAL
   - Recomendação: APROVAR / APROVAR COM RESSALVAS / REJEITAR
   - Resumo executivo em 5 linhas
   - Lista priorizada de alterações necessárias

Formato: Use tabelas para cláusulas e riscos.
Tom: Técnico-jurídico mas acessível para não-advogados.


### Resultado Esperado

- Mapa completo de cláusulas e riscos
- Classificação por nível de criticidade
- Sugestões de redação alternativa
- Parecer executivo para tomada de decisão
- Lista de ações para negociação

### Variações do Prompt

**Para contrato de tecnologia:**

Adicione: "Atenção especial para SLA, LGPD, backup de dados e propriedade de código"


**Para contrato de trabalho:**

Adicione: "Verificar aderência à CLT e convenção coletiva do setor"


**Para contrato internacional:**

Adicione: "Analisar jurisdição, câmbio, e compatibilidade com lei brasileira"


---

## Caso 5: Relatório Gerencial Semanal Automatizado

### Departamento
Operações / Gestão

### Contexto do Problema
Gestores gastam horas toda semana compilando dados de diferentes fontes para montar relatórios de acompanhamento, muitas vezes com formato inconsistente.

### Antes vs Depois
- **Antes**: 4 horas toda semana compilando manualmente
- **Depois**: Automático, recebido por email toda segunda às 8h

### Passo a Passo

1. Prepare a base de dados semanal (Excel/CSV)
2. Faça upload no Rhapsodia [3]
3. Cole o prompt de relatório
4. Para automatizar: salve como template e configure recorrência
5. Defina destinatários do email [5]

### Prompt Exato


Gere um relatório gerencial semanal executivo com os dados fornecidos.

ESTRUTURA DO RELATÓRIO:

1. RESUMO EXECUTIVO (máximo 5 bullets)
   - Destaque do período
   - Principal conquista
   - Principal desafio
   - Número mais importante
   - Tendência geral

2. KPIs DA SEMANA
   | Indicador | Meta | Realizado | % Atingimento | Variação vs Semana Anterior |
   
   Incluir:
   - Faturamento
   - Unidades vendidas/produzidas
   - Ticket médio
   - Conversão
   - NPS/Satisfação (se disponível)

3. DESTAQUES POSITIVOS
   - Top 3 resultados acima da meta
   - Reconhecimentos de equipe
   - Novos clientes/contratos

4. PONTOS DE ATENÇÃO
   - Indicadores abaixo da meta
   - Riscos identificados
   - Ações corretivas em andamento

5. COMPARATIVO MENSAL
   - Acumulado do mês vs meta mensal
   - Projeção de fechamento

6. PRIORIDADES PRÓXIMA SEMANA
   - Top 3 focos
   - Decisões pendentes
   - Recursos necessários

7. ANEXO: DADOS DETALHADOS
   - Tabela completa para referência

Formato: 
- Use emojis para status (verde/amarelo/vermelho)
- Máximo 2 páginas
- Pronto para envio por email

Tom: Direto, focado em ação, sem floreios.


### Resultado Esperado

- Relatório executivo de 2 páginas
- KPIs com indicação visual de status
- Análise de tendências
- Recomendações acionáveis
- Formato pronto para distribuição

### Variações do Prompt

**Para relatório diário:**

Simplifique: "Foque apenas em Resumo Executivo, KPIs e Pontos de Atenção"


**Para relatório mensal:**

Expanda: "Adicione análise de tendência trimestral e comparativo com ano anterior"


**Para board/diretoria:**

Adicione: "Inclua visão estratégica, market share e posição competitiva"


---

## Caso 6: Kit de Onboarding Completo em 15 Minutos

### Departamento
RH / Gestão de Pessoas

### Contexto do Problema
Preparar materiais de onboarding para novos colaboradores é trabalhoso e muitas vezes inconsistente, resultando em experiências de integração desiguais.

### Antes vs Depois
- **Antes**: 1 dia inteiro preparando materiais
- **Depois**: 15 minutos com kit completo personalizado

### Passo a Passo

1. Reúna informações do novo colaborador e da vaga
2. Acesse o Rhapsodia e inicie nova conversa
3. Se tiver documentos de referência (políticas, organograma), faça upload [3]
4. Cole o prompt com dados específicos
5. Revise e personalize detalhes finais

### Prompt Exato


Crie um kit completo de onboarding para novo colaborador com as seguintes informações:

DADOS DO COLABORADOR:
- Nome: [NOME COMPLETO]
- Cargo: [CARGO]
- Departamento: [ÁREA]
- Gestor direto: [NOME DO GESTOR]
- Data de início: [DATA]
- Modelo de trabalho: [PRESENCIAL/HÍBRIDO/REMOTO]

DADOS DA EMPRESA:
- Nome da empresa: [EMPRESA]
- Cultura/Valores: [LISTAR VALORES]
- Dress code: [SE APLICÁVEL]
- Horário de trabalho: [HORÁRIO]

GERAR OS SEGUINTES DOCUMENTOS:

1. EMAIL DE BOAS-VINDAS
   - Tom acolhedor e entusiasmado
   - Informações práticas do primeiro dia
   - Contato do RH e gestor
   - O que trazer/preparar

2. AGENDA DA PRIMEIRA SEMANA
   | Dia | Horário | Atividade | Responsável | Local |
   
   Incluir:
   - Recepção e tour
   - Reunião com gestor
   - Apresentação à equipe
   - Treinamentos essenciais
   - Configuração de acessos
   - Almoços de integração

3. CHECKLIST DE PRIMEIRO DIA
   - [ ] Itens para o colaborador
   - [ ] Itens para o RH
   - [ ] Itens para TI
   - [ ] Itens para o gestor

4. GUIA DE SOBREVIVÊNCIA
   - Onde fica o quê (banheiros, copa, salas)
   - Sistemas que vai usar (login inicial)
   - Contatos importantes
   - Canais de comunicação (Slack, Teams, email)
   - Dicas práticas do dia a dia

5. RESUMO DE BENEFÍCIOS
   - Lista de benefícios com detalhes básicos
   - Como acessar cada um
   - Prazos de carência se houver

6. FAQ DO NOVO COLABORADOR
   - 10 perguntas mais comuns
   - Respostas objetivas

7. MENSAGEM DO GESTOR (TEMPLATE)
   - Boas-vindas personalizada
   - Expectativas iniciais
   - Disponibilidade para dúvidas

Formato: 
- Documentos separados e prontos para uso
- Tom acolhedor mas profissional
- Visual limpo com bullets e tabelas



### Resultado Esperado

- Email de boas-vindas pronto para envio
- Agenda completa da primeira semana
- Checklists para todos os envolvidos
- Guia prático do novo colaborador
- Templates para gestor utilizar

### Variações do Prompt

**Para onboarding remoto:**

Adicione: "Inclua guia de setup do home office e etiqueta para reuniões virtuais"


**Para cargo de liderança:**

Adicione: "Inclua apresentação dos pares, rituais de gestão e principais stakeholders"


**Para estagiário:**

Adapte: "Simplifique a linguagem e inclua seção sobre programa de estágio e mentoria"


---

## Como Expandir Esta Biblioteca

### Sugerindo Novos Casos

1. Identifique uma tarefa repetitiva no seu departamento
2. Documente o tempo gasto atualmente
3. Teste prompts no Rhapsodia
4. Meça o tempo com a nova abordagem
5. Envie para o time de CX para inclusão na biblioteca

### Critérios para Inclusão

- ROI mínimo de 50% de economia de tempo
- Aplicável a múltiplas empresas/contextos
- Prompt testado e validado
- Resultado consistente e confiável

### Contato

Para sugestões de novos casos de uso:
- Email: suporte@pktech.com.br [1]
- Chat interno: canal casos-de-uso

---