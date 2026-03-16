# API Services Setup Guide

## 🎯 Quick Setup Options

You have **TWO options** for AI services:

### Option 1: OpenAI (Recommended - Easier Setup)
- **Get API Key:** https://platform.openai.com/api-keys
- **Cost:** Pay-as-you-go (~$0.002 per 1K tokens for GPT-4o-mini)
- **Setup Time:** 5 minutes

### Option 2: OpenRouter (Alternative)
- **Get API Key:** https://openrouter.ai/keys
- **Cost:** Requires credits (minimum $5)
- **Setup Time:** 10 minutes

---

## 🚀 Option 1: OpenAI Setup (RECOMMENDED)

### Step 1: Get OpenAI API Key

1. **Go to:** https://platform.openai.com/signup
2. **Create account** or sign in
3. **Navigate to:** https://platform.openai.com/api-keys
4. **Click:** "Create new secret key"
5. **Copy the key** (starts with `sk-proj-...`)

### Step 2: Add Credits (Required)

1. **Go to:** https://platform.openai.com/account/billing
2. **Add payment method**
3. **Add credits** (minimum $5 recommended)

### Step 3: Update .env.local

Open `.env.local` and add/update:
```env
OPENAI_API_KEY=sk-proj-YOUR_ACTUAL_KEY_HERE
OPENAI_MODEL=gpt-4o-mini
```

**Comment out or remove OpenRouter lines:**
```env
# OPENROUTER_API_KEY=sk-or-v1-...
# OPENROUTER_MODEL=openai/gpt-4o-mini
```

### Step 4: Restart Server

```bash
npm run dev:8080
```

---

## 🔄 Option 2: OpenRouter Setup

### Step 1: Get OpenRouter API Key

1. **Go to:** https://openrouter.ai/
2. **Sign up** or log in
3. **Navigate to:** https://openrouter.ai/keys
4. **Create new key** (starts with `sk-or-v1-...`)

### Step 2: Add Credits (REQUIRED)

1. **Go to:** https://openrouter.ai/settings/credits
2. **Add credits** (minimum $5 required)
3. **Without credits, API calls will fail!**

### Step 3: Update .env.local

Open `.env.local` and ensure:
```env
OPENROUTER_API_KEY=sk-or-v1-YOUR_NEW_VALID_KEY_HERE
OPENROUTER_MODEL=openai/gpt-4o-mini
```

### Step 4: Restart Server

```bash
npm run dev:8080
```

---

## ✅ Verify It's Working

After setup, check server logs. You should see:
- `[AI Config] ✅ SUCCESS: Using OPENAI provider` OR
- `[AI Config] ✅ SUCCESS: Using OPENROUTER provider`

Then test at: `http://localhost:8080/chat`

---

## 💡 Which Should You Choose?

**Choose OpenAI if:**
- ✅ You want simpler setup
- ✅ You want direct access to GPT models
- ✅ You're okay with pay-as-you-go pricing

**Choose OpenRouter if:**
- ✅ You want access to multiple AI models
- ✅ You want to switch between models easily
- ✅ You prefer prepaid credits

---

## 🆘 Troubleshooting

### "401 Unauthorized" Error
- **Cause:** Invalid or expired API key
- **Fix:** Get a new API key and update `.env.local`

### "Insufficient Credits" Error
- **Cause:** No credits in account
- **Fix:** Add credits to your account

### "API service not configured"
- **Cause:** No valid API keys found
- **Fix:** Add either `OPENAI_API_KEY` or `OPENROUTER_API_KEY` to `.env.local`

---

## 📞 Support Links

- **OpenAI:** https://help.openai.com/
- **OpenRouter:** https://openrouter.ai/docs
- **Check API Status:** Both services have status pages
