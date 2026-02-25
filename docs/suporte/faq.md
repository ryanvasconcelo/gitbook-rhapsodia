# Perguntas Frequentes (FAQ)

Encontre aqui as respostas para as dúvidas mais comuns sobre o uso, configuração e segurança do Rhapsodia.

---

## 👤 Para Usuários

### Meus dados de chat são usados para treinar a IA?
**Não.** No Rhapsodia Corporativo, as chaves de API e a infraestrutura On-Premise garantem que seus prompts e documentos sejam processados apenas para gerar sua resposta e não sejam integrados ao treinamento público de modelos como o GPT-4.

### Posso subir qualquer tipo de arquivo?
O Rhapsodia suporta PDF, Word, Excel, CSV, PowerPoint e diversos formatos de texto e imagem. O limite padrão é de 50MB por arquivo, mas pode ser ajustado pelo seu administrador.

### Por que a IA às vezes comete erros?
A IA utiliza processamento de linguagem natural e pode ocasionalmente sofrer de "alucinações". Sempre revise informações críticas, especialmente cálculos e referências legais.

---

## ⚙️ Para Administradores

### Como aprovo novos usuários?
Vá em **Painel do Admin** > **Usuários**. Filtre por status "Pendente" e utilize o botão de aprovação. Você também pode configurar o login via SSO (Microsoft/Google) para aprovação automática.

### O que acontece se a quota de tokens acabar?
O usuário verá um aviso informando que o limite mensal foi atingido. Você pode resetar a quota individualmente ou aumentar o limite do departamento no Painel do Admin.

---

## 👨‍💻 Para Desenvolvedores

### Como crio uma nova integração com meu ERP?
Você deve seguir o [Manual do Desenvolvedor](../manuais/desenvolvedor.md) e criar uma **Tool** em Python. A ferramenta precisará das credenciais do sistema e docstrings claros para que a IA saiba como usá-la.

### Existe um limite de requisições na API?
Sim, o rate limit padrão é de 60 requisições por minuto por API Key, configurável nas opções de segurança do sistema.

---

## 🛡️ Segurança e Privacidade

### Onde os arquivos que eu subo ficam armazenados?
Se o seu deploy for On-Premise, os arquivos ficam em um diretório seguro dentro do servidor da sua empresa. Se for via VPS, ficam no volume Docker persistente do seu servidor.

### O Rhapsodia é compatível com a LGPD?
**Sim.** A plataforma oferece ferramentas de anonimização, logs de auditoria e exclusão definitiva de dados para garantir conformidade total com a legislação brasileira.

---

## 🆘 Ainda precisa de ajuda?

Se você não encontrou sua resposta aqui:
1. Digite `/help` no chat para comandos rápidos.
2. Consulte o guia de [Resolução de Problemas](troubleshooting.md).
3. Abra um chamado com o suporte: `suporte@pktech.com.br`.
