# User Onboarding Automation

This Python project automates the creation of user accounts and sends welcome emails using data from a CSV file. It’s designed to simplify the Identity and Access Management (IAM) onboarding process.

## Features

- Reads user details (name, email, department, title) from a CSV file.
- Sends personalized welcome emails via Gmail SMTP.
- Easily extensible to integrate with account creation APIs or PowerShell scripts.

## Prerequisites

- Python 3.6 or higher installed.
- A Gmail account with [2-Step Verification enabled](https://myaccount.google.com/security) and an [App Password generated](https://support.google.com/accounts/answer/185833).
- `users.csv` file formatted correctly (see below).

## Setup Instructions

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/user-onboarding-automation.git
   cd user-onboarding-automation
2. Create your users.csv file with the following headers:

first_name,last_name,email
John,Doe,johndoe@example.com
Jane,Smith,janesmith@example.com

3. Edit the onboard.py file:

Replace 'your_email@gmail.com' with your actual Gmail address.

Replace the app password with your generated app password in the script.

4. Run the script:

python onboard.py

How It Works
- The script reads users.csv.

- For each user, it prints a creation message and sends a welcome email.

- Email sending uses Gmail’s SMTP server with TLS encryption.

Security Notes
- Never hardcode your real Gmail password.

- Always use an App Password for SMTP authentication.

- Consider using environment variables or a .env file with python-dotenv for managing secrets securely.

Future Improvements
- Integration with Active Directory or cloud IAM systems.

- Add HTML email templates.

- Log sent emails to a file or database.

- Error handling and retry mechanisms.

License
This project is licensed under the MIT License.


