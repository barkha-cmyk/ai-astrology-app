# ✅ PERFECT API KEY SETUP GUIDE

## 🎯 EXACTLY What You Need to Do

### **Line 45 in .env.local** - Update OpenRouter API Key

**Current line (INVALID):**
```
OPENROUTER_API_KEY=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
```

**Replace with (YOUR NEW KEY):**
```
OPENROUTER_API_KEY=sk-or-v1-YOUR_ACTUAL_NEW_KEY_HERE
```

### **Line 10 in .env.local** - Update OpenAI API Key (OPTIONAL - Alternative)

**Current line (EMPTY):**
```
OPENAI_API_KEY=
```

**Replace with (YOUR OPENAI KEY - if you prefer OpenAI):**
```
OPENAI_API_KEY=sk-proj-YOUR_ACTUAL_OPENAI_KEY_HERE
```

---

## 📋 STEP-BY-STEP INSTRUCTIONS

### Option 1: Use OpenRouter (Current Setup)

1. **Get Your API Key:**
   - Visit: **https://openrouter.ai/keys**
   - Sign up/Login
   - Click "Create Key"
   - Copy the key (starts with `sk-or-v1-`)

2. **Add Credits (REQUIRED):**
   - Visit: **https://openrouter.ai/settings/credits**
   - Add minimum $5 credits
   - **Without credits, it won't work!**

3. **Update Line 45 in .env.local:**
   - Open `.env.local` (already open in your editor)
   - Find line 45: `OPENROUTER_API_KEY=YOUR_NEW_KEY_HERE`
   - Replace `YOUR_NEW_KEY_HERE` with your actual key
   - **NO SPACES** around the `=`
   - Save the file (Ctrl+S)

4. **Restart Server:**
   ```bash
   npm run dev:8080
   ```

### Option 2: Use OpenAI (Easier Alternative)

1. **Get Your API Key:**
   - Visit: **https://platform.openai.com/api-keys**
   - Sign up/Login
   - Click "Create new secret key"
   - Copy the key (starts with `sk-proj-`)

2. **Add Credits:**
   - Visit: **https://platform.openai.com/account/billing**
   - Add payment method
   - Add credits ($5 minimum)

3. **Update Line 10 in .env.local:**
   - Find line 10: `OPENAI_API_KEY=YOUR_OPENAI_KEY_HERE`
   - Replace `YOUR_OPENAI_KEY_HERE` with your actual key
   - Save the file (Ctrl+S)

4. **Comment Out OpenRouter (Optional):**
   - Add `#` before line 45: `#OPENROUTER_API_KEY=...`

5. **Restart Server:**
   ```bash
   npm run dev:8080
   ```

---

## ✅ VERIFICATION CHECKLIST

After updating, check server logs for:

**✅ SUCCESS:**
```
[AI Config] ✅ Force-loaded OPENROUTER_API_KEY from .env.local: sk-or-v1-...
[AI Config] ✅ SUCCESS: Using OPENROUTER provider
[OpenRouter] ✅ Response received, length: XXX
```

**❌ FAILURE (Invalid Key):**
```
[OpenRouter] 📥 Response status: 401 Unauthorized
AI Service Error: Error: User not found.
```

**❌ FAILURE (No Credits):**
```
Insufficient OpenRouter credits
```

---

## 🔧 PERFECT FORMAT EXAMPLES

### OpenRouter Key Format:
```
OPENROUTER_API_KEY=sk-or-v1-abc123xyz789def456ghi012jkl345mno678pqr901stu234vwx567
```
- Starts with: `sk-or-v1-`
- Length: ~70-80 characters
- No spaces, no quotes

### OpenAI Key Format:
```
OPENAI_API_KEY=sk-proj-abc123xyz789def456ghi012jkl345mno678pqr901stu234vwx567
```
- Starts with: `sk-proj-`
- Length: ~50-60 characters
- No spaces, no quotes

---

## 🎯 RECOMMENDATION

**Use OpenAI** - It's simpler and more reliable:
1. Easier setup
2. More reliable
3. Better documentation
4. Direct access to GPT models

**Get started:** https://platform.openai.com/api-keys

---

## 🆘 QUICK FIX

**If you have a new OpenRouter key RIGHT NOW:**

1. Open `.env.local` (line 45)
2. Replace: `OPENROUTER_API_KEY=YOUR_NEW_KEY_HERE`
3. With: `OPENROUTER_API_KEY=sk-or-v1-PASTE_YOUR_KEY_HERE`
4. Save (Ctrl+S)
5. Restart: `npm run dev:8080`

**Done!** ✅
