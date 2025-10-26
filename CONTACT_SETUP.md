# Contact Form Setup Guide

## Current Status
The contact form is currently configured for **Formspree** integration but needs setup to work properly.

## Option 1: Formspree (Recommended - Free & Easy)

### Setup Steps:
1. **Visit**: https://formspree.io
2. **Sign up** with your email: `ait.mhend.dna@gmail.com`
3. **Create a new form**
4. **Copy your form ID** (looks like: `xpzgkqyw`)
5. **Replace** `YOUR_FORM_ID` in `contact.html` with your actual ID:
   ```html
   <form action="https://formspree.io/f/xpzgkqyw" method="POST">
   ```

### Benefits:
- ✅ Works immediately after setup
- ✅ Free tier: 50 submissions/month
- ✅ Emails delivered to your Gmail
- ✅ No coding required
- ✅ Mobile-friendly
- ✅ Spam protection included

## Option 2: Netlify Forms (Alternative)

If you deploy to Netlify instead of GitHub Pages:

1. **Deploy** your site to Netlify
2. **Add** `netlify` attribute to form:
   ```html
   <form netlify method="POST" class="contact-form">
   ```
3. Forms automatically work

## Option 3: EmailJS (More Complex)

For advanced users who want more control:

1. **Sign up**: https://emailjs.com
2. **Get API keys**
3. **Add JavaScript** to handle form submission
4. **Configure** email templates

## Testing Locally

### Current mailto: approach
- **Limitation**: Only works if user has email client configured
- **Test**: Click submit → Should open email app
- **Reality**: Many users don't complete this step

### After Formspree setup
- **Test locally**: Forms won't submit (localhost not allowed)
- **Test online**: Deploy to GitHub Pages, then test
- **Verification**: Check your Gmail for submissions

## Quick Fix for Immediate Testing

If you want to test right now without setup:

1. **Keep current mailto: approach** for now
2. **Test** by clicking submit button
3. **Verify** it opens your email client
4. **Note**: This requires visitors to have email configured

## Recommended Action

**For best user experience**:
1. Set up Formspree (takes 5 minutes)
2. Update the form action URL
3. Test on live GitHub Pages site
4. Forms will work for all visitors!

## Form Field Mapping

The form is already configured with proper field names:
- `name` → Visitor's name
- `_replyto` → Visitor's email (for your replies)
- `subject` → Message category
- `message` → Main message content
- `_subject` → Hidden field (sets email subject)

## Troubleshooting

**Form not working?**
1. Check if you replaced `YOUR_FORM_ID`
2. Verify Formspree account is active
3. Check spam folder for submissions
4. Test on live site (not localhost)

**Still having issues?**
- The direct email link always works as backup
- Users can always email you directly at: `ait.mhend.dna@gmail.com`