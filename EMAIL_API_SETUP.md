# Email API Setup Instructions

## Quick Setup

Your portfolio now has a custom email API that sends contact form submissions directly to your Gmail.

### Steps to Deploy:

1. **Install nodemailer**:
   ```bash
   npm install
   ```

2. **Set up Gmail App Password**:
   - Go to https://myaccount.google.com/apppasswords
   - Sign in with `anirudhvartak33@gmail.com`
   - Create a new App Password for "Mail"
   - Copy the 16-character password

3. **Deploy to Vercel** (Free):
   - Go to https://vercel.com
   - Sign up/Login with GitHub
   - Import your `anirudh-portfolio-react` repository
   - Add Environment Variables in Vercel dashboard:
     * `EMAIL_USER` = `anirudhvartak33@gmail.com`
     * `EMAIL_PASS` = `your_16_character_app_password`
   - Deploy!

### How It Works:

- Contact form → `/api/send-email` (Vercel serverless function)
- Function uses Gmail SMTP to send email to you
- Email arrives at `anirudhvartak33@gmail.com`
- Sender's email is set as Reply-To

### Testing Locally:

1. Create `.env` file (copy from `.env.example`)
2. Add your Gmail App Password
3. Run: `npm run dev`

### Vercel vs GitHub Pages:

- **GitHub Pages**: Static only (no API)
- **Vercel**: Supports both React app + API endpoints
- Your app will work the same, just hosted on Vercel instead

The form will work instantly after deployment!
