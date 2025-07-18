# EmailJS Setup Guide

## Configuration Details
**Public Key**: 84RrI4uYEZ72RmStk  
**Private Key**: Nm6xVszthFP6mb_ZKawhw  
**Service ID**: service_84rri4uy  
**Template ID**: template_ez72rmst  

## Step 1: EmailJS Account Setup
1. Go to [EmailJS.com](https://www.emailjs.com/)
2. Sign up for a free account
3. Verify your email address

## Step 2: Configure Email Service
1. In your EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose your email provider (Gmail recommended)
4. Follow the setup instructions for your email provider
5. Your **Service ID** is: `service_84rri4uy`

## Step 3: Create Email Template
1. Go to "Email Templates" in your dashboard
2. Click "Create New Template"
3. Use this template structure:

**Subject**: `New Contact Form Message - {{subject}}`

**Email Body**:
```
Hello Ahsan,

You have received a new message from your portfolio website:

Name: {{from_name}}
Email: {{from_email}}
Subject: {{subject}}

Message:
{{message}}

---
This message was sent from your portfolio contact form.
Reply directly to {{from_email}} to respond.
```

4. Save the template with ID: `template_ez72rmst`

## Step 4: API Keys Configuration
Your EmailJS configuration is already set up in the Contact.tsx component:
- **Public Key**: `84RrI4uYEZ72RmStk`
- **Service ID**: `service_84rri4uy`
- **Template ID**: `template_ez72rmst`

## Step 5: Install EmailJS Package
Run this command in your project directory:
```bash
npm install @emailjs/browser
```

## Step 6: Test the Contact Form
1. Start your development server: `npm run dev`
2. Navigate to the contact section
3. Fill out and submit the contact form
4. Check your configured email for the message

## Template Variables
The following variables are used in the email template:
- `{{from_name}}` - Sender's name
- `{{from_email}}` - Sender's email address
- `{{subject}}` - Message subject
- `{{message}}` - Message content

## Troubleshooting
- Ensure your email service is properly configured and verified
- Check the browser console for any JavaScript errors
- Verify all Service ID and Template ID match your EmailJS dashboard
- Make sure your EmailJS account email is verified
- Test with different email addresses to ensure delivery

## Monthly Limits
- **Free tier**: 200 emails per month
- **Perfect for portfolio websites**
- Upgrade to paid plans for higher limits if needed

## Security Notes
- Public key is safe to expose in client-side code
- Private key should only be used server-side (not included in frontend)
- EmailJS handles the secure email sending process
