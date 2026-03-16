# 🔑 How to Generate API Keys - Step by Step Guide

## 🎯 Choose Your Service

You have **TWO options**. I recommend **OpenAI** (easier and more reliable).

---

## 🚀 Option 1: OpenAI API Key (RECOMMENDED)

### Step-by-Step Instructions:

#### Step 1: Create Account
1. **Go to:** https://platform.openai.com/signup
2. **Click:** "Sign up" button
3. **Enter:** Your email address and create a password
4. **Verify:** Your email address (check your inbox)

#### Step 2: Add Payment Method
1. **Go to:** https://platform.openai.com/account/billing
2. **Click:** "Add payment method"
3. **Enter:** Your credit card details
4. **Note:** You need to add a payment method to use the API (even for free tier)

#### Step 3: Add Credits
1. **Still on billing page:** https://platform.openai.com/account/billing
2. **Click:** "Add credits" or "Add funds"
3. **Enter amount:** Minimum $5 recommended
4. **Complete payment**

#### Step 4: Generate API Key
1. **Go to:** https://platform.openai.com/api-keys
2. **Click:** "Create new secret key" button (top right)
3. **Enter name:** Give it a name like "AI Astrologer App"
4. **Click:** "Create secret key"
5. **IMPORTANT:** Copy the key immediately! It starts with `sk-proj-` and looks like:
   ```
   sk-proj-abc123xyz789def456ghi012jkl345mno678pqr901stu234vwx567
   ```
6. **Save it:** Paste it somewhere safe (you won't see it again!)

#### Step 5: Add to Your Project
1. **Open:** `.env.local` file in your project
2. **Find line 9:** `OPENAI_API_KEY=`
3. **Replace with:** `OPENAI_API_KEY=sk-proj-YOUR_ACTUAL_KEY_HERE`
4. **Save the file**

#### Step 6: Restart Server
```bash
npm run dev:8080
```

**Done!** ✅

---

## 🔄 Option 2: OpenRouter API Key

### Step-by-Step Instructions:

#### Step 1: Create Account
1. **Go to:** https://openrouter.ai/
2. **Click:** "Sign up" or "Get Started"
3. **Enter:** Your email address and create a password
4. **Verify:** Your email address

#### Step 2: Add Credits (REQUIRED)
1. **Go to:** https://openrouter.ai/settings/credits
2. **Click:** "Add Credits" or "Top Up"
3. **Enter amount:** Minimum $5 required
4. **Complete payment**
5. **Important:** Without credits, API calls will fail!

#### Step 3: Generate API Key
1. **Go to:** https://openrouter.ai/keys
2. **Click:** "Create Key" or "New Key" button
3. **Enter name:** Give it a name like "AI Astrologer"
4. **Click:** "Create" or "Generate"
5. **Copy the key:** It starts with `sk-or-v1-` and looks like:
   ```
   sk-or-v1-abc123xyz789def456ghi012jkl345mno678pqr901stu234vwx567
   ```
6. **Save it:** Paste it somewhere safe!

#### Step 4: Add to Your Project
1. **Open:** `.env.local` file in your project
2. **Find line 41:** `OPENROUTER_API_KEY=...`
3. **Replace with:** `OPENROUTER_API_KEY=sk-or-v1-YOUR_NEW_KEY_HERE`
4. **Save the file**

#### Step 5: Restart Server
```bash
npm run dev:8080
```

**Done!** ✅

---

## 📋 Quick Comparison

| Feature | OpenAI | OpenRouter |
|---------|--------|------------|
| **Setup Time** | 5 minutes | 10 minutes |
| **Payment** | Pay-as-you-go | Prepaid credits |
| **Minimum** | $5 recommended | $5 required |
| **Ease** | ⭐⭐⭐⭐⭐ Easy | ⭐⭐⭐⭐ Moderate |
| **Reliability** | ⭐⭐⭐⭐⭐ High | ⭐⭐⭐⭐ Good |

---

## ✅ Verify Your API Key Works

After adding the key and restarting:

1. **Check server logs** - You should see:
   ```
   [AI Config] ✅ SUCCESS: Using OPENAI provider
   ```
   OR
   ```
   [AI Config] ✅ SUCCESS: Using OPENROUTER provider
   ```

2. **Test the chat:**
   - Go to: `http://localhost:8080/chat`
   - Send a message
   - You should get an AI response (not an error!)

---

## 🆘 Troubleshooting

### "Invalid API Key" Error
- **Check:** Make sure you copied the ENTIRE key (no spaces before/after)
- **Check:** Key starts with `sk-proj-` (OpenAI) or `sk-or-v1-` (OpenRouter)
- **Fix:** Get a new key and try again

### "Insufficient Credits" Error
- **OpenAI:** Add more credits at https://platform.openai.com/account/billing
- **OpenRouter:** Add credits at https://openrouter.ai/settings/credits

### "API service not configured"
- **Check:** `.env.local` file exists
- **Check:** API key is on the correct line
- **Check:** No extra spaces around `=`
- **Fix:** Restart the server after making changes

---

## 💡 Pro Tips

1. **Never share your API key** - Keep it secret!
2. **Save it securely** - Use a password manager
3. **Start with $5** - Test it works, then add more
4. **Monitor usage** - Check your billing dashboard regularly
5. **Use OpenAI first** - It's simpler and more reliable

---

## 📞 Need Help?

- **OpenAI Support:** https://help.openai.com/
- **OpenRouter Docs:** https://openrouter.ai/docs
- **Check Status:** Both services have status pages

---

## 🎯 Recommended: Start with OpenAI

**Why OpenAI?**
- ✅ Easier setup
- ✅ More reliable
- ✅ Better documentation
- ✅ Direct access to GPT models
- ✅ Pay-as-you-go (no prepaid credits)

**Get started:** https://platform.openai.com/api-keys
