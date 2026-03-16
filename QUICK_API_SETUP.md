# 🚀 Quick API Setup - Choose One Option

## ⚡ FASTEST: Use OpenAI (5 minutes)

### 1. Get API Key
- Visit: https://platform.openai.com/api-keys
- Click "Create new secret key"
- Copy the key (starts with `sk-proj-`)

### 2. Add Credits
- Visit: https://platform.openai.com/account/billing
- Add payment method and credits ($5 minimum)

### 3. Update .env.local
Open `.env.local` and change line 9:
```
OPENAI_API_KEY=sk-proj-PASTE_YOUR_KEY_HERE
```

### 4. Restart Server
```bash
npm run dev:8080
```

**Done!** ✅

---

## 🔄 Alternative: Use OpenRouter

### 1. Get API Key
- Visit: https://openrouter.ai/keys
- Create account and get key (starts with `sk-or-v1-`)

### 2. Add Credits (REQUIRED)
- Visit: https://openrouter.ai/settings/credits
- Add credits ($5 minimum)

### 3. Update .env.local
Open `.env.local` and change line 41:
```
OPENROUTER_API_KEY=sk-or-v1-PASTE_YOUR_NEW_KEY_HERE
```

### 4. Restart Server
```bash
npm run dev:8080
```

**Done!** ✅

---

## 🎯 Which One?

**OpenAI:** Easier, direct access, pay-as-you-go
**OpenRouter:** More models, prepaid credits

**Recommendation:** Start with OpenAI (simpler setup)

---

## ✅ Test It

After setup, visit: `http://localhost:8080/chat`

You should see AI responses instead of error messages!
