# Resolução de Problemas (Troubleshooting)

Guia prático para identificar e resolver os erros mais comuns encontrados no Rhapsodia.

---

## 🌐 Conectividade e Acesso

### Erro: "Não foi possível conectar ao servidor"
- **Causa**: Problema de rede ou container do Rhapsodia offline.
- **Solução**:
  1. Verifique sua conexão com a internet ou VPN corporativa.
  2. Administradores: Executem `docker ps` no servidor para checar se o container está em execução.

### Login Rejeitado ou Conta Pendente
- **Causa**: Sua conta ainda não foi aprovada pelo administrador ou as credenciais estão incorretas.
- **Solução**: Contate o time de TI/RH para verificar o status do seu convite.

---

## 🤖 Modelos e Respostas

### A IA parou de responder no meio da frase
- **Causa**: Time-out de rede ou limite de `max_tokens` atingido.
- **Solução**: Digite "Continue" no chat ou aumente o limite de tokens nas configurações da conversa.

### Erro: "API Key Invalid or Expired"
- **Causa**: A chave de integração (OpenAI, Anthropic) configurada no admin expirou ou não tem saldo.
- **Solução**: O administrador deve atualizar a chave em **Settings** > **Connections**.

---

## 📁 Documentos e RAG

### "Erro ao processar o arquivo"
- **Causa**: Arquivo corrompido, formato não suportado ou OCR de baixa qualidade.
- **Solução**:
  1. Tente converter o arquivo para PDF texto (não imagem).
  2. Verifique se o arquivo possui proteção por senha.

### A IA diz que não encontrou informações no documento subido
- **Causa**: Fragmentação de texto (chunking) ineficiente ou documento muito grande.
- **Solução**: Refine sua pergunta ou tente fazer o upload novamente do arquivo. Se for um documento técnico longo, use o modelo **Gemini 1.5 Pro** que possui uma janela de contexto maior.

---

## ⚙️ Backend e Performance

### Interface lenta ou travando
- **Causa**: Baixa memória no servidor ou muitos usuários simultâneos no mesmo modelo local.
- **Solução**:
  1. No On-Premise, verifique o uso de VRAM (`nvidia-smi`).
  2. Considere adicionar um servidor de cache ou balanceamento de carga.

### Erro "Database is Locked" (SQLite)
- **Causa**: Muitas escritas simultâneas no banco de dados.
- **Solução**: Reinicie o container. Para ambientes com muitos usuários, recomendamos migrar o banco de dados para **PostgreSQL**.

---

## 📞 Suporte Especializado

Se o problema persistir após estas verificações, colete os seguintes dados e envie para o suporte:
1. Print da tela com o erro.
2. Logs do sistema (Admin Panel > Logs).
3. Modelo de IA e navegador que estava utilizando.

**Email**: `suporte@pktech.com.br`
