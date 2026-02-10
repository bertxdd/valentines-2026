# 📧 Email Setup Guide - Valentine's Website

This guide will help you set up email notifications so that when she selects a date, you'll receive it in your Gmail.

## 🚀 Quick Setup with EmailJS (FREE)

EmailJS is a free service that lets you send emails directly from your website without a backend server.

---

## Step 1: Create EmailJS Account

1. Go to [https://www.emailjs.com/](https://www.emailjs.com/)
2. Click **"Sign Up"** (top right)
3. Sign up using your Google account or email
4. Verify your email address

---

## Step 2: Add Email Service (Gmail)

1. Once logged in, click **"Add New Service"**
2. Select **"Gmail"**
3. Click **"Connect Account"**
4. Sign in with your Gmail account
5. Grant EmailJS permission to send emails on your behalf
6. Give your service a name (e.g., "Valentine Gmail")
7. Copy the **Service ID** (looks like: `service_abc123`)

---

## Step 3: Create Email Template

1. Go to **"Email Templates"** in the sidebar
2. Click **"Create New Template"**
3. Set up your template:

**Subject:**
```
💕 Valentine Date Selected!
```

**Content:**
```
Hello!

Your Valentine has chosen a date for your special day! 🥰

📅 Date: {{date}}
⏰ Time: {{time}}

Get ready for an amazing time together! 💖

---
This is an automated message from your Valentine's website
```

4. Save the template
5. Copy the **Template ID** (looks like: `template_xyz789`)

---

## Step 4: Get Your Public Key

1. Go to **"Account"** → **"General"**
2. Find your **Public Key** (looks like: `aBcDeFgHiJkLmNoPqR`)
3. Copy it

---

## Step 5: Update Your Website Code

Open `date.html` and find these three places to update:

### Line 12: Replace YOUR_PUBLIC_KEY
```javascript
emailjs.init('YOUR_PUBLIC_KEY');
```
Replace with:
```javascript
emailjs.init('aBcDeFgHiJkLmNoPqR'); // Your actual public key
```

### Line 447: Replace YOUR_EMAIL@gmail.com
```javascript
to_email: 'YOUR_EMAIL@gmail.com',
```
Replace with:
```javascript
to_email: 'youractual@gmail.com', // Your Gmail address
```

### Line 454: Replace YOUR_SERVICE_ID and YOUR_TEMPLATE_ID
```javascript
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams)
```
Replace with:
```javascript
emailjs.send('service_abc123', 'template_xyz789', templateParams)
```

---

## Step 6: Test It!

1. Save the `date.html` file
2. Open it in your browser
3. Select a date and time
4. Click "Save Our Date 💕"
5. Check your Gmail inbox!

---

## ✅ What You'll Receive

When she selects a date, you'll get an email like this:

**Subject:** 💕 Valentine Date Selected!

**Body:**
```
Hello!

Your Valentine has chosen a date for your special day! 🥰

📅 Date: Saturday, February 14, 2026
⏰ Time: 7:00 PM

Get ready for an amazing time together! 💖
```

---

## 🔧 Troubleshooting

### Email not arriving?

1. **Check spam folder** - First email might go to spam
2. **Verify Service ID and Template ID** - Make sure they match exactly
3. **Check Public Key** - Must be correct
4. **Check browser console** - Press F12, look for errors in Console tab
5. **EmailJS Free Tier Limit** - Free plan allows 200 emails/month

### Service connection issues?

- Make sure you completed Gmail OAuth authorization
- Try disconnecting and reconnecting the service
- Check that "Less secure app access" is enabled in Gmail (if using older method)

---

## 💡 Alternative: Formspree (Even Simpler)

If you prefer, you can use Formspree instead:

1. Go to [https://formspree.io/](https://formspree.io/)
2. Sign up (free)
3. Create a new form
4. Get your form endpoint
5. I can help you update the code to use Formspree instead

---

## 📱 Alternative: Simple mailto Link

If you want the absolute simplest solution (but requires her email client to work):

I can update the code to open her email client with a pre-filled message. Just let me know!

---

## 🎯 Summary

1. ✅ Create EmailJS account
2. ✅ Connect Gmail service → Get Service ID
3. ✅ Create email template → Get Template ID
4. ✅ Copy Public Key
5. ✅ Update 3 places in `date.html`:
   - Public Key (line 12)
   - Your Gmail (line 447)
   - Service ID & Template ID (line 454)
6. ✅ Test and enjoy!

**Total time:** 5-10 minutes
**Cost:** FREE (up to 200 emails/month)

---

Need help? Let me know which step you're stuck on! 💕
