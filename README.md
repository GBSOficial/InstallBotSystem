# 🚀 **INSTALADOR BOTSYSTEM V2.5**

## **✨ Multi-Canal: WhatsApp + Facebook Messenger + Instagram Direct**

Esta versão do instalador inclui suporte completo à **versão v2.5** do BotSystem com:
- ✅ **Facebook Messenger** - Integração nativa completa
- ✅ **Instagram Direct** - Mensagens diretas do Instagram
- ✅ **OAuth 2.0** - Login com Google e Facebook
- ✅ **Sistema Multi-Canal** - Gestão unificada de todos os canais
- ✅ **Webhooks Meta** - Recebimento automático de mensagens FB/IG
- ✅ **BaileysButtonService** - Botões interativos otimizados
- ✅ **Flow Builder Aprimorado** - Construtor de fluxos avançado
- ✅ **Performance Otimizada** - Gerenciamento de memória e sessões

## **📋 INSTALAÇÃO**

### **PRIMEIRA INSTALAÇÃO (Download + Instalação):**

```bash
sudo apt install -y git && git clone https://github.com/GBSOficial/InstallBotSystem && sudo chmod -R 777 InstallBotSystem && cd InstallBotSystem && sudo ./install_primaria
```

### **INSTALAÇÕES ADICIONAIS (Diretório Existente):**
```bash
cd ./InstallBotSystem && sudo ./install_primaria
```

## **🆕 Novidades da V2.5**

### **Multi-Canal:**
- ✅ **Facebook Messenger** - Mensagens, mídia e botões interativos
- ✅ **Instagram Direct** - Integração completa com Instagram Business
- ✅ **WhatsApp** - Baileys otimizado com botões funcionais
- ✅ **Gestão Unificada** - Todos os canais em um único painel

### **OAuth 2.0:**
- ✅ **Login com Google** - Autenticação Google OAuth 2.0
- ✅ **Login com Facebook** - Autenticação Facebook OAuth 2.0
- ✅ **Passport.js** - Configurado automaticamente
- ✅ **Sessões Seguras** - Express session com secrets seguros

### **Backend:**
- ✅ **MetaWebhookController** - Webhooks Facebook/Instagram
- ✅ **OAuthController** - Autenticação social
- ✅ **SendUniversalMessageService** - Envio multicanal unificado
- ✅ **BaileysButtonService** - Botões interativos funcionais (headerType fix)
- ✅ **Libs FB/IG** - facebook-messenger.ts e instagram-direct.ts
- ✅ **Otimizações** - BaileysOptimizer, GC Manager, WebSocket events

### **Frontend:**
- ✅ **MetaConnectionModal** - Modal unificado FB/IG
- ✅ **OAuthCallback** - Página de callback OAuth
- ✅ **ConnectionsManager** - Gestão de múltiplos canais
- ✅ **Ícones Dinâmicos** - WhatsApp, Facebook, Instagram
- ✅ **UI Moderna** - Interface responsiva e intuitiva

### **Database:**
- ✅ **Migrations OAuth** - Campos googleId, facebookId
- ✅ **Migrations Meta** - Campos type, pageId, pageAccessToken, instagramAccountId
- ✅ **Migrations UX** - showGroupNotification e otimizações
- ✅ **Constraints** - Remoção de unique desnecessárias

### **Sistema:**
- ✅ Backup automático antes da instalação
- ✅ Validação de integridade pós-instalação
- ✅ Rollback automático em caso de falha
- ✅ Logs aprimorados para debugging
- ✅ Dependências OAuth instaladas automaticamente

## **⚠️ Compatibilidade**

✅ **Totalmente compatível** com instalações existentes
✅ **Migração automática** de configurações
✅ **Preservação** de dados existentes
✅ **Rollback** disponível se necessário

