# OpenRouter API Key Setup Guide

## ⚠️ Current Issue: API Key Authentication Failed

Your API key is being loaded correctly, but OpenRouter is returning:
- **Error:** `401 Unauthorized - User not found`
- **Meaning:** The API key is invalid, expired, or the account doesn't exist

## 🔧 How to Fix:

### Step 1: Get a New OpenRouter API Key

1. **Go to OpenRouter:** https://openrouter.ai/
2. **Sign up or Log in:**
   - If you don't have an account, create one
   - If you have an account, log in
3. **Get Your API Key:**
   - Go to: https://openrouter.ai/keys
   - Click "Create Key" or copy your existing key
   - The key should start with `sk-or-v1-...`

### Step 2: Add Credits (Required)

OpenRouter requires credits to use their API:
1. Go to: https://openrouter.ai/settings/credits
2. Add credits to your account (minimum $5 recommended)
3. Without credits, API calls will fail

### Step 3: Update .env.local

1. Open `.env.local` file in your project root
2. Replace the `OPENROUTER_API_KEY` line with your new key:
   ```
   OPENROUTER_API_KEY=sk-or-v1-YOUR_NEW_KEY_HERE
   ```
3. Save the file

### Step 4: Restart Server

1. Stop the server (Ctrl+C in terminal)
2. Start it again: `npm run dev:8080`
3. Wait 30 seconds for startup
4. Try the chat again

## ✅ Verify It's Working

After updating the API key, check the server logs. You should see:
- `[AI Config] ✅ SUCCESS: Using OPENROUTER provider`
- `[OpenRouter] 📥 Response status: 200 OK` (not 401!)

## 🔍 Alternative: Use OpenAI Directly

If OpenRouter continues to have issues, you can use OpenAI directly:

1. Get an OpenAI API key from: https://platform.openai.com/api-keys
2. Add to `.env.local`:
   ```
   OPENAI_API_KEY=sk-proj-YOUR_OPENAI_KEY_HERE
   ```
3. Remove or comment out the `OPENROUTER_API_KEY` line
4. Restart the server

## 📞 Need Help?

- OpenRouter Support: https://openrouter.ai/docs
- Check your OpenRouter account status: https://openrouter.ai/settings
