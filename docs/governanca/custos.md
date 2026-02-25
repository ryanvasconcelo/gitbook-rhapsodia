# Gestão de Custos e Tokens

Otimizar o uso de recursos de IA é fundamental para manter o ROI da plataforma. No Rhapsodia, você tem controle total sobre quem consome o quê, permitindo uma gestão financeira transparente e eficiente.

---

## 📈 Como os Custos são Calculados

Os custos no Rhapsodia baseiam-se no consumo de **Tokens** (fragmentos de palavras). O valor varia conforme o modelo utilizado:

- **Modelos Cloud (GPT-4, Claude)**: Cobrados por milhão de tokens (input/output).
- **Modelos Locais (Llama, Mistral)**: Custo zero de tokens, consumindo apenas recursos de infraestrutura (GPU/Energia).

---

## ⚙️ Ferramentas de Controle

![Painel de Governança e Custos](../assets/images/admin-menu.png)

### 1. Quotas por Usuário e Departamento
O administrador pode definir limites mensais ou diários de tokens para cada usuário ou grupo. Ao atingir o limite, a plataforma pode disparar um aviso ou bloquear novas consultas até o próximo ciclo.

### 2. Filtros de "Guardian"
O **Rhapsodia Guardian** atua como uma trava de segurança. Ele monitora o consumo em tempo real e pode injetar avisos de "limite próximo" diretamente na interface do usuário.

### 3. Analytics em Tempo Real
Visualize o gasto estimado por:
- **Modelo**: Descubra quais modelos são mais eficientes para suas tarefas.
- **Departamento**: Facilite o rateio de custos internos entre áreas.
- **Top Users**: Identifique os "heavy users" e ofereça treinamento de otimização de prompts.

---

## 💡 Dicas de Economia

- **Uso de Modelos Locais**: Use o Llama 3 para tarefas simples de síntese ou chat e reserve o GPT-4o apenas para análises críticas.
- **Limitação de Contexto**: Configure Agentes para lerem apenas as partes necessárias dos documentos, reduzindo o tráfego de tokens.
- **Cache de Respostas**: O Rhapsodia pode armazenar respostas para perguntas idênticas, evitando gastos duplicados.

> [!TIP]
> Um prompt bem escrito consome menos tokens para chegar ao mesmo resultado. Consulte nosso [Guia de Engenharia de Prompts](../manuais/usuario.md).
