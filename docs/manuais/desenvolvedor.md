# Manual do Desenvolvedor - Construindo o Rhapsodia

O Rhapsodia é uma plataforma extensível projetada para permitir que desenvolvedores criem fluxos de IA personalizados, integrem sistemas corporativos e apliquem regras de governança estritas. Este manual detalha como estender a plataforma usando **Filtros**, **Ferramentas (Tools)** e **Agentes (Pipes)**.

---

## 🚀 Visão Geral da Arquitetura

A extensibilidade do Rhapsodia baseia-se no framework do Open WebUI, utilizando Python para a lógica de backend e uma interface rica para configuração no frontend.

![Painel de Funções no Admin](../assets/images/admin-functions.png)

### Os Três Pilares de Extensão:

1. **Agentes (Agents/Pipes)**: Definem "modelos" inteiros com lógica própria.
2. **Filtros (Filters)**: Atuam como middlewares de entrada (`inlet`) e saída (`outlet`).
3. **Ferramentas (Tools)**: Funções que o modelo pode decidir chamar (Function Calling).

---

## 🤖 1. Criando Agentes Personalizados (Pipes)

Um Agente no Rhapsodia pode ser um modelo simples com um System Prompt específico ou um "Pipe" complexo que orquestra múltiplas chamadas de API.

![Configuração de Agente](../assets/images/agent-settings.png)

### Como criar:
1. Vá em **Espaço de Trabalho** > **Agentes**.
2. Clique em **+ Novo Agente**.
3. Defina o **Prompt do Sistema**: Aqui você define a "personalidade" e as instruções básicas.
4. Associe **Conhecimento**: Adicione documentos ou bases de dados.
5. Habilite **Capacidades**: Decida se o agente pode pesquisar na web, gerar imagens ou interpretar código.

---

## 🧰 2. Desenvolvendo Ferramentas (Tools)

As Tools permitem que a IA interaja com o mundo real (ERPs, bancos de dados, APIs externas).

### Estrutura de uma Tool:
Uma Tool é uma classe Python que define as variáveis de configuração (**Valves**) e os métodos públicos que a IA pode chamar.

```python
from pydantic import BaseModel, Field

class Tools:
    class Valves(BaseModel):
        API_KEY: str = Field(default="", description="Chave de acesso ao sistema")

    def __init__(self):
        self.valves = self.Valves()

    def buscar_informacao(self, termo: str) -> str:
        """
        Busca informações específicas em um sistema externo.
        :param termo: O termo de busca enviado pela IA.
        """
        # Lógica de integração aqui
        return f"Resultado para {termo} processado com sucesso."
```

---

## 🛡️ 3. Implementando Filtros (Governança)

Filtros são essenciais para segurança e compliance. Eles permitem interceptar mensagens antes que cheguem ao modelo ou antes que a resposta chegue ao usuário.

![Editor de Funções](../assets/images/function-editor.png)

### Hook de Entrada (`inlet`)
Use para:
- Bloquear requisições não autorizadas.
- Injetar contexto corporativo ou avisos de segurança.
- Validar permissões de acesso a dados.

### Hook de Saída (`outlet`)
Use para:
- Auditar o consumo de tokens.
- Adicionar rodapés automáticos ou avisos de confidencialidade.
- Mascarar dados sensíveis na resposta da IA.

---

## 🛠️ Melhores Práticas

- **Segurança**: Nunca hardcode credenciais. Use as `Valves` para que as senhas sejam configuradas na interface administrativa.
- **UX**: Use o parâmetro `__event_emitter__` em funções assíncronas para enviar status em tempo real ou gráficos para o usuário.
- **Documentação**: A IA decide qual ferramenta usar baseada no seu *docstring*. Escreva descrições claras e detalhadas para cada parâmetro.
