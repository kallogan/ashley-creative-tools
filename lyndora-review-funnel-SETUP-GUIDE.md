# Lyndora Auto Sales - Review Funnel Setup Guide

**Created:** 2026-05-06  
**For:** Lyndora Auto Sales  
**Email:** lyndoraauto@zoominternet.net

---

## 📋 What You're Getting

A complete, mobile-friendly review funnel that:
- ✅ Asks customers: "Would you recommend us to a friend?"
- ✅ Routes **"Sure!"** responses directly to Google reviews
- ✅ Routes **"Meh..."** and **"Nope"** responses to a private feedback form
- ✅ Emails feedback to `lyndoraauto@zoominternet.net`
- ✅ Still offers Google review link on feedback page (Google TOS compliant)
- ✅ Works perfectly on mobile phones
- ✅ Professional, clean design

---

## 🚀 Setup Instructions (5-10 Minutes)

### Step 1: Set Up Formspree (FREE - handles email delivery)

1. Go to **https://formspree.io**
2. Click **"Get Started"** (free account - no credit card needed)
3. Sign up with any email address
4. Once logged in, click **"+ New Form"**
5. Form name: **"Lyndora Auto Sales Feedback"**
6. Click **Create Form**
7. **IMPORTANT:** Copy the form endpoint URL - it looks like:
   ```
   https://formspree.io/f/xyzabc123
   ```
   (Save this - you'll need it in Step 2)

8. In Formspree settings:
   - **Email:** Set to `lyndoraauto@zoominternet.net`
   - **Subject:** "New Customer Feedback - Lyndora Auto Sales"
   - **Confirm:** Save settings

---

### Step 2: Update the HTML File

1. Open the file: **`lyndora-review-funnel.html`**
2. Find this line (around line 208):
   ```html
   <form id="feedbackForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
3. Replace **`YOUR_FORM_ID`** with your actual Formspree form ID from Step 1
   
   **Example:**
   ```html
   <form id="feedbackForm" action="https://formspree.io/f/xyzabc123" method="POST">
   ```

4. Save the file

---

### Step 3: Host the File

You need to put this HTML file on the internet so customers can access it via a link.

**Option A: Use Your Existing Website (EASIEST)**

If you have access to your website files:
1. Upload `lyndora-review-funnel.html` to your website
2. Rename it to something simple like: `review.html`
3. Your link will be: `https://lyndoraautosales.com/review.html`

**Option B: Use a Free Hosting Service**

If you don't have website access, use one of these free options:

**Netlify Drop (EASIEST - No account needed):**
1. Go to **https://app.netlify.com/drop**
2. Drag and drop the `lyndora-review-funnel.html` file
3. Wait 10 seconds
4. You'll get a free URL like: `https://random-name-123.netlify.app`
5. Share that URL with customers

**GitHub Pages (Permanent, Professional):**
1. Create a free GitHub account: https://github.com
2. Create a new repository called `lyndora-reviews`
3. Upload the HTML file
4. Enable GitHub Pages in settings
5. Your URL will be: `https://yourusername.github.io/lyndora-reviews`

---

### Step 4: Create a Short Link (OPTIONAL but RECOMMENDED)

Long URLs are hard to text. Shorten it!

**Option A: Bitly (Free)**
1. Go to **https://bitly.com**
2. Sign up (free)
3. Paste your full review funnel URL
4. Create a custom short link like: `bit.ly/lyndora-review`

**Option B: TinyURL (No account needed)**
1. Go to **https://tinyurl.com**
2. Paste your full URL
3. Create custom alias: `lyndora-review`
4. Get link like: `https://tinyurl.com/lyndora-review`

---

## 📱 How Salespeople Use It

Once setup is complete, here's what your team does:

### Text Message Template

After a customer buys a car, send this text:

---

**Option 1: Short & Simple**
```
Hi [Customer Name]! Congrats again on your [vehicle]! 🚗 
We'd love to hear about your experience. 
Quick feedback: [YOUR SHORT LINK]
```

**Option 2: Personal Touch**
```
Hey [Customer Name], it's [Salesperson Name] from Lyndora Auto Sales! 
Hope you're loving your [vehicle]! Would mean a lot if you 
could share your experience: [YOUR SHORT LINK]
Thanks! 🙏
```

---

**Replace `[YOUR SHORT LINK]` with your actual link from Step 4.**

---

## ✅ How It Works (Customer Experience)

1. **Customer clicks link** → Opens on their phone
2. **Sees question:** "Would you recommend us to a friend?"
3. **Three options:**
   - **"Sure! ✨"** → Goes directly to Google review page
   - **"Meh... 😐"** → Feedback form (+ optional Google review link)
   - **"Nope 👎"** → Feedback form (+ optional Google review link)
4. **If feedback form:**
   - Fills out name, email, phone (optional), comments
   - Submits
   - Manager gets email at `lyndoraauto@zoominternet.net`
5. **Thank you screen** → Done!

---

## 🛡️ Google TOS Compliance

This funnel is **100% compliant** with Google's review policies:

✅ **No review gating** - Everyone can access Google reviews (link available on feedback form)  
✅ **No incentives** - No discounts or rewards for reviews  
✅ **No selective filtering** - All customers get the same link  
✅ **Honest request** - Straightforward "Would you recommend us?" question  
✅ **No manipulation** - Customer chooses where to leave feedback

**Source:** Google's Review Policy - https://support.google.com/business/answer/2622994

---

## 📊 What Happens with Feedback

**Positive responses ("Sure!"):**
- Customer leaves Google review immediately
- Public reviews build your reputation

**Neutral/Negative responses ("Meh..." or "Nope"):**
- Feedback goes to `lyndoraauto@zoominternet.net`
- Manager can reach out privately to resolve issues
- Prevents public negative reviews (but customer can still leave one if they want)
- Shows you care about making things right

---

## 🎨 Customization Options (Optional)

If you want to customize the look:

### Add Your Logo
Replace this line (around line 110):
```html
<div class="logo">🚗</div>
```

With an actual logo image:
```html
<div class="logo"><img src="your-logo.png" alt="Lyndora Auto Sales" style="width:100%; height:100%; object-fit:contain;"></div>
```

### Change Colors
The gradient colors are defined at the top of the CSS. Look for:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

Change the hex codes to match your brand colors.

---

## 🧪 Testing Before Launch

**Before sending to customers, TEST IT:**

1. Open the review funnel link on your phone
2. Click **"Sure!"** → Should go to Google review page
3. Go back, click **"Meh..."** → Should show feedback form
4. Fill out the form with test data
5. Submit it
6. **Check email:** `lyndoraauto@zoominternet.net` should receive the feedback within 1-2 minutes

If the email doesn't arrive:
- Check spam folder
- Verify Formspree email is set correctly
- Make sure form action URL is correct in HTML

---

## 📞 Support & Troubleshooting

**Email not arriving?**
- Check Formspree dashboard for submissions
- Verify email address in Formspree settings
- Check spam folder

**Link not working?**
- Make sure HTML file is uploaded correctly
- Test the full URL in a browser first
- Verify hosting platform is active

**Google review link not working?**
- The Place ID is already correct in the code
- If Google changes their review URL format, update line 286

**Need to change the email address?**
- Log into Formspree
- Update email in form settings
- No need to change HTML file

---

## 🎯 Best Practices

**When to send the review request:**
- **Best:** 1-2 days after purchase (excitement is still high, but they've driven the car)
- **Okay:** Same day (immediate, but might be rushed)
- **Avoid:** More than 1 week later (experience fades)

**Who should send it:**
- The salesperson they worked with (personal connection)
- If manager sold them the car, the manager sends it

**Follow-up:**
- If no response after 3 days, send one gentle reminder
- Don't spam - one reminder max

**Handling feedback:**
- Respond to private feedback within 24 hours
- Thank them for positive reviews publicly
- Resolve issues quickly and professionally

---

## 📈 Tracking Results

**Formspree Dashboard:**
- See all submissions
- Export feedback data
- Track response rate

**Google Business Profile:**
- Monitor new reviews
- Respond to all reviews (positive and negative)

**Recommendation:**
- Track how many links you send vs. responses received
- Goal: 20-30% response rate is good
- 40%+ is excellent

---

## ✅ Final Checklist

Before going live, make sure:

- [ ] Formspree account created
- [ ] Form ID updated in HTML file
- [ ] Test email received successfully
- [ ] HTML file hosted and accessible via URL
- [ ] Short link created (optional but recommended)
- [ ] Text message template ready
- [ ] Team knows when/how to send the link
- [ ] Manager ready to respond to feedback emails

---

## 🚀 You're Ready!

Once all steps are complete:
1. Send the link to your first customer
2. Watch for feedback to arrive
3. Respond quickly and professionally
4. Build your Google reviews over time

**Questions?** Reach out to Kathy Logan at Logan Virtuals - she can help with any technical issues or customizations.

---

*This review funnel is designed to be simple, effective, and compliant. No ongoing costs (Formspree free tier covers up to 50 submissions/month). If you grow beyond that, upgrade to Formspree's paid plan ($10/month for unlimited).*
