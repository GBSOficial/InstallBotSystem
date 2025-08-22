# 📋 **CHANGELOG - INSTALADOR BOTSYSTEM**

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
