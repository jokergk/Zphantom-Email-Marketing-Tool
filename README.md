📦 About This Release
This is a standalone Windows executable built with PyInstaller. No Python installation required - just download and run!

🚀 Quick Start Guide
1. Download & Extract
Download the latest release ZIP file

Extract to any folder on your Windows PC

No installation needed - just run the executable!

2. Required Files
Create these files in the same folder as the executable:

📄 smtp_server.txt (Your email servers)
text
username@domain.com:password@smtp.server.com:587
username2@domain.com:password2@smtp2.server.com:465
One server per line. Multiple formats supported.

📄 emails.txt (Recipients)
text
recipient1@example.com
recipient2@example.com
recipient3@example.com
One email per line

📄 subject.txt (Email subject)
text
Important Update for {firstname}
Use {tags} for personalization

📄 body.txt (Email content)
text
Hello {firstname},

This is your important update...

Best regards,
The Team
Can be plain text or HTML

📄 config.json (Auto-created on first run)
The tool creates this automatically with default settings

3. Optional Files
cc_emails.txt - CC recipients (one per line)

bcc_emails.txt - BCC recipients (one per line)

proxies.xlsx - Proxy list (Excel format)

attachments/ folder - For email attachments

🎯 How to Use
Step 1: Prepare Your Files
text
C:\EmailTool\
├── ProfessionalEmailTool.exe
├── smtp_server.txt
├── emails.txt
├── subject.txt
├── body.txt
└── (other optional files)
Step 2: Run the Tool
Double-click ProfessionalEmailTool.exe

Select mode:

1. FAST - Built-in optimizations (recommended)

2. AI - DeepSeek AI optimization (requires API key)

Step 3: Watch It Work!
The tool will:

Load and validate your SMTP servers

Process email lists

Send emails with smart optimization

Show real-time progress and statistics

⚙️ Configuration Options
Edit config.json (after first run):
json
{
  "mode": "fast",
  "email_config": {
    "recipients_per_batch": 10,
    "max_to_per_email": 10,
    "max_cc_per_email": 50,
    "max_bcc_per_email": 50
  },
  "sending_config": {
    "min_delay": 1.0,
    "max_delay": 3.0,
    "max_workers": 15
  }
}
🔧 Advanced Features
Dynamic Tags in Emails
Use these tags in subject.txt and body.txt:

{firstname}, {lastname}, {company}

{date}, {datetime}, {invoiceid}

{amount}, {coupon}, {weburl}

#TAG# format also supported

Attachment Support
Create an attachments folder

Place files inside

Files will be attached with random names

Proxy Support
Create proxies.xlsx Excel file

Add proxies in format: socks5://user:pass@proxy.com:1080

The tool will automatically rotate proxies

⚠️ Important Notes
System Requirements
Windows 10/11 (64-bit recommended)

4GB RAM minimum

Internet connection

Administrative rights (for some proxy configurations)

Security Features
✅ Credentials encrypted at rest

✅ No credential caching

✅ Secure proxy connections

✅ One server per worker (no hopping)

Legal Compliance
✅ Include unsubscribe links in emails

✅ Only send to permission-based lists

✅ Comply with CAN-SPAM/GDPR

✅ Respect email sending limits

🚨 Troubleshooting
Common Issues & Solutions
❌ "No SMTP servers available"
Check smtp_server.txt format

Verify username:password format

Ensure servers are active

❌ "Authentication failed"
Check username/password

Verify SMTP port (587, 465, 25)

Try app passwords if 2FA enabled

❌ "Connection timeout"
Check internet connection

Try different proxy

Verify firewall settings

❌ "No recipients found"
Check emails.txt file exists

Verify file is not empty

Ensure emails are one per line

Log Files
Check these for detailed errors:

professional_mailer.log - Main application log

Console output for real-time debugging

📊 Performance Tips
For Best Results:
Start Small: Test with 10 emails first

Use Proxies: For large campaigns (>1000 emails)

Monitor Stats: Watch success rates in console

Adjust Delays: Increase delays if errors occur

Clean Lists: Remove invalid emails regularly

Recommended Settings:
Small lists (<1000): 5-10 workers

Medium lists (1000-5000): 10-15 workers

Large lists (>5000): 15-20 workers (with proxies)

🔄 Updates & Maintenance
To Update:
Download new release

Copy your configuration files

Replace executable

Test with small batch first

Regular Maintenance:
Weekly: Check and update proxy lists

Monthly: Rotate SMTP credentials

Quarterly: Review configuration settings

📝 File Format Reference
SMTP Server Formats Accepted:
text
Format 1: username:password@server:port
Format 2: username|password|server|port  
Format 3: server|username|password (port defaults to 587)
Proxy Excel Format:
Create Excel with column named "proxy":

text
A1: proxy
A2: socks5://user:pass@proxy1.com:1080
A3: http://proxy2.com:8080
Email List Format:
One email per line

No commas, semicolons, or quotes

Blank lines ignored

Duplicates automatically filtered

⚠️ Disclaimer & Legal
IMPORTANT: USE RESPONSIBLY

This tool is for legitimate email marketing only:

✅ Permission-based lists only

✅ Include unsubscribe links

✅ Respect all applicable laws

✅ Monitor sender reputation

The developers are not responsible for:

❌ Spam or unsolicited emails

❌ Legal violations

❌ Account suspensions

❌ Misuse of the tool

🤝 Support & Community
Getting Help:
Check console output for errors

Review log files for details

Search for similar issues

Contact support with detailed information

Need to Report a Bug?
Include this information:

Tool version

Windows version

Error message

Steps to reproduce

Log file snippets

📈 Success Checklist
Before sending large campaigns:

Test with 10 emails first

Verify deliverability to inbox

Check spam score

Confirm unsubscribe link works

Validate sender reputation

Monitor success rates

🎉 Ready to Start?
Prepare your files

Test with small batch

Monitor performance

Scale up gradually

Happy Emailing! 🚀

Last Updated: Version 2.0 | Windows Executable | Professional Edition
<img width="365" height="290" alt="Screenshot 2025-12-22 225517" src="https://github.com/user-attachments/assets/01551797-c4d6-4aa8-ae04-8779a2195c62" />

