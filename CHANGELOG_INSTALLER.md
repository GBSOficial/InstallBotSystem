# 📋 **CHANGELOG - INSTALADOR BOTSYSTEM**

## **V2.5 - Integração Facebook Messenger, Instagram Direct e OAuth 2.0**

### 🆕 **NOVAS FUNCIONALIDADES:**

#### **1. Suporte Completo Facebook Messenger e Instagram Direct**
- ✅ Integração nativa com Facebook Messenger
- ✅ Integração nativa com Instagram Direct
- ✅ Webhooks automáticos para recebimento de mensagens
- ✅ Envio de mensagens, mídia e botões interativos
- ✅ Gestão unificada de múltiplos canais (WhatsApp + Facebook + Instagram)

#### **2. OAuth 2.0 - Login Social**
- ✅ Login com Google (OAuth 2.0)
- ✅ Login com Facebook (OAuth 2.0)
- ✅ Passport.js configurado automaticamente
- ✅ Session management seguro
- ✅ Integração com usuários existentes

#### **3. Novas Dependências**
- ✅ `passport` - Autenticação OAuth
- ✅ `passport-google-oauth20` - Google OAuth
- ✅ `passport-facebook` - Facebook OAuth
- ✅ `express-session` - Gerenciamento de sessões
- ✅ TypeScript types para todas as dependências

#### **4. Backend Aprimorado**
- ✅ MetaWebhookController - Webhooks Facebook/Instagram
- ✅ OAuthController - Autenticação social
- ✅ SendUniversalMessageService - Envio multicanal
- ✅ ProcessFacebookWebhookService - Processamento FB
- ✅ ProcessInstagramWebhookService - Processamento IG
- ✅ Libs facebook-messenger.ts e instagram-direct.ts

#### **5. Frontend Modernizado**
- ✅ MetaConnectionModal - Modal unificado para FB/IG
- ✅ OAuthCallback page - Callback OAuth
- ✅ ConnectionsManager atualizado - Múltiplos canais
- ✅ Ícones dinâmicos por tipo de conexão
- ✅ Interface responsiva e intuitiva

#### **6. Database**
- ✅ Migration OAuth (googleId, facebookId)
- ✅ Migration campos Meta (type, pageId, pageAccessToken, instagramAccountId)
- ✅ Migration showGroupNotification
- ✅ Remoção de constraints desnecessárias

### 🔧 **MELHORIAS:**

#### **Sistema Multi-Canal:**
- ✅ Suporte simultâneo WhatsApp + Facebook + Instagram
- ✅ Tickets unificados independente do canal
- ✅ Contatos sincronizados entre canais
- ✅ Histórico de conversas centralizado

#### **Segurança:**
- ✅ OAuth 2.0 padrão da indústria
- ✅ Tokens JWT seguros
- ✅ Session secrets configuráveis
- ✅ HTTPS obrigatório para webhooks

#### **Performance:**
- ✅ SendWebSocketEvent helper - Eventos otimizados
- ✅ BaileysOptimizer - Gestão de sessões WhatsApp
- ✅ GC Manager - Gerenciamento de memória
- ✅ Rate limiting aprimorado

### 📋 **VARIÁVEIS DE AMBIENTE (V2.5):**

#### **Novas variáveis adicionadas:**
```bash
# OAuth Google
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
GOOGLE_CALLBACK_URL=https://seu-backend.com/oauth/google/callback

# OAuth Facebook  
FACEBOOK_APP_ID=
FACEBOOK_APP_SECRET=
FACEBOOK_CALLBACK_URL=https://seu-backend.com/oauth/facebook/callback

# Session
SESSION_SECRET=chave-secreta-gerada
```

### 🚀 **INSTRUÇÕES DE ATUALIZAÇÃO:**

#### **Para Instalações Novas:**
```bash
# O instalador agora configura automaticamente:
# 1. Dependências OAuth (passport, passport-google-oauth20, passport-facebook)
# 2. Variáveis de ambiente Facebook/Instagram/OAuth
# 3. Webhooks Meta (Facebook + Instagram)
# 4. Sistema multi-canal completo

# Após instalação:
# 1. Configure credenciais OAuth no .env
# 2. Configure webhook no Facebook Developers
# 3. Conecte páginas Facebook e contas Instagram Business
```

#### **Para Atualizações de V2.4 ou Anterior:**
```bash
cd /home/deploy/botsystem/backend

# 1. Instalar novas dependências OAuth
npm install passport passport-google-oauth20 passport-facebook express-session
npm install --save-dev @types/passport @types/passport-google-oauth20 @types/passport-facebook @types/express-session

# 2. Adicionar novas variáveis ao .env
# (Copie do .env.example as seções OAuth)

# 3. Executar novas migrations
npx sequelize db:migrate

# 4. Recompilar e reiniciar
npm run build
pm2 restart botsystem-backend
pm2 restart botsystem-frontend
```

### ⚠️ **NOTAS IMPORTANTES:**

1. **OAuth Credentials:** Configure após instalação no Google Cloud Console e Facebook Developers
2. **Webhooks Meta:** HTTPS obrigatório - Configure após obter SSL
3. **Página Facebook:** Necessário ter página Facebook e Instagram Business conectado
4. **Permissões:** App Facebook precisa permissões: pages_messaging, instagram_basic, instagram_manage_messages
5. **Compatibilidade:** 100% compatível com instalações V2.4 e anteriores

### 🔧 **CONFIGURAÇÃO FACEBOOK DEVELOPERS:**

```bash
# 1. Criar app em https://developers.facebook.com
# 2. Adicionar produtos: Messenger, Instagram
# 3. Configurar webhook:
#    URL: https://seu-backend.com/api/webhooks/meta
#    Verify Token: qualquer-string-secreta
# 4. Subscribir eventos:
#    - messages
#    - messaging_postbacks  
#    - messaging_optins
#    - message_deliveries
#    - message_reads
```

### 📊 **PRÓXIMAS VERSÕES:**

- V2.6: Telegram Integration
- V2.7: Twitter/X Direct Messages
- V2.8: Email Integration (SMTP/IMAP)

---

## **V2.4 - Suporte à Versão v1 do BotSystem**

### 🆕 **NOVAS FUNCIONALIDADES:**

#### **1. Suporte Completo à Versão v1**
- ✅ Atualização automática para nova estrutura v1
- ✅ Compatibilidade com novos serviços (BaileysButtonService)
- ✅ Suporte a novas integrações e webhooks
- ✅ Flow builder aprimorado
- ✅ Melhorias na interface do usuário

#### **2. Novas Dependências e Configurações**
- ✅ `craco.config.js` - Configuração customizada do React
- ✅ Novos arquivos de deploy automatizado
- ✅ Estrutura aprimorada de pastas públicas
- ✅ Sistema de tipos aprimorado

#### **3. Melhorias de Performance**
- ✅ Otimizações no processamento de mensagens
- ✅ Cache aprimorado para melhor desempenho
- ✅ Sistema de logs mais eficiente
- ✅ Gerenciamento de memória otimizado

### 🔧 **MELHORIAS:**

#### **Sistema de Deploy:**
- ✅ Deploy package automatizado
- ✅ Backup automático antes da atualização
- ✅ Validação de integridade pós-instalação
- ✅ Rollback automático em caso de falha

#### **Interface e Experiência:**
- ✅ Componentes React atualizados
- ✅ Nova estrutura de assets
- ✅ Melhorias na responsividade
- ✅ Novos recursos de acessibilidade

### 📋 **COMPATIBILIDADE:**

#### **✅ Mantém compatibilidade com:**
- Instalações existentes V2.3 e anteriores
- Todas as configurações de banco de dados
- Estrutura de usuários e permissões
- APIs existentes

#### **🆕 Adiciona suporte para:**
- Nova arquitetura v1 do BotSystem
- Componentes React aprimorados
- Sistema de flow builder avançado
- Integrações expandidas

### 🚀 **INSTRUÇÕES DE ATUALIZAÇÃO:**

#### **Para Atualizações da v0 para v1:**
```bash
# Backup automático será criado
# O instalador irá:
# 1. Fazer backup da versão atual
# 2. Atualizar dependências
# 3. Migrar configurações
# 4. Aplicar novos recursos
# 5. Validar funcionamento

# Após atualização, novos recursos estarão disponíveis
```

### ⚠️ **NOTAS IMPORTANTES:**

1. **Backup Automático:** Sempre criado antes da atualização
2. **Migração:** Dados existentes são preservados
3. **Downtime:** Mínimo durante a atualização
4. **Rollback:** Disponível em caso de problemas

---

## **V2.3 - Compatibilidade com Swagger e Melhorias de Segurança**

### 🆕 **NOVAS FUNCIONALIDADES:**

#### **1. Dependências Swagger Automáticas**
- ✅ `swagger-jsdoc` - Geração automática da documentação
- ✅ `swagger-ui-express` - Interface web interativa  
- ✅ TypeScript types para desenvolvimento

#### **2. Variáveis de Ambiente Expandidas**
- ✅ `REDIS_URI_ACK` - Redis ACK separado
- ✅ `REDIS_SECRET_KEY` - Chave secreta Redis
- ✅ `DB_POOL_*` - Configurações de pool de conexões
- ✅ `BULL_BOARD` - Monitoramento de filas
- ✅ `BULL_USER/BULL_PASS` - Autenticação Bull Board
- ✅ `OPENAI_API_KEY` - Integração OpenAI (placeholder)
- ✅ `MASTER_KEY` - Chave mestra de emergência

#### **3. Nova Função de Validação**
- ✅ `backend_validate_env()` - Valida configurações críticas
- ✅ Verificação automática de variáveis obrigatórias
- ✅ Alertas para configurações faltantes
- ✅ Copy automático do .env.example

### 🔧 **MELHORIAS:**

#### **Instalação Mais Robusta:**
- ✅ Validação de ambiente após configuração
- ✅ Feedback visual para o usuário
- ✅ Detecção de problemas antes da compilação
- ✅ Compatibilidade com versões antigas

#### **Configurações de Performance:**
- ✅ Pool de conexões otimizado para produção
- ✅ Redis configurado para alta disponibilidade
- ✅ Bull Board habilitado por padrão

### 📋 **COMPATIBILIDADE:**

#### **✅ Mantém compatibilidade com:**
- Instalações existentes V2.2 e anteriores
- Todas as configurações de rede atuais
- Estrutura de pastas existente
- Scripts de deploy atuais

#### **🆕 Adiciona suporte para:**
- Documentação Swagger automática em `/api-docs`
- Monitoramento de filas em `/admin/queues`
- Validação automática de configurações críticas

### 🚀 **INSTRUÇÕES DE USO:**

#### **Para Novas Instalações:**
```bash
# O instalador agora configura automaticamente:
# 1. Dependências Swagger
# 2. Variáveis de ambiente completas  
# 3. Validação de configurações
# 4. Monitoramento de filas

# Após instalação, acesse:
# - Documentação: https://seu-dominio.com/api-docs
# - Filas: https://seu-dominio.com/admin/queues
```

#### **Para Atualizações Manuais:**
```bash
# Se você tem uma instalação existente:
cd /home/deploy/botsystem/backend

# 1. Instalar dependências Swagger
npm install swagger-jsdoc swagger-ui-express
npm install --save-dev @types/swagger-jsdoc @types/swagger-ui-express

# 2. Adicionar variáveis ao .env (veja env.example)
# 3. Recompilar e reiniciar
npm run build
pm2 restart botsystem-backend
```

### ⚠️ **NOTAS IMPORTANTES:**

1. **OpenAI API Key:** Deixada vazia por padrão - configure após instalação
2. **Bull Board:** Senha usa a mesma do MySQL por segurança
3. **Validação:** Não bloqueia instalação, apenas alerta
4. **Compatibilidade:** 100% compatível com versões anteriores

### 🔧 **PRÓXIMAS VERSÕES:**

- V2.4: Testes automatizados durante instalação
- V2.5: Backup automático na instalação
- V2.6: Monitoramento e alertas integrados
