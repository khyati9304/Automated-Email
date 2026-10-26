An automated weekly email system that curates personalized tech content including articles, GitHub repositories, YouTube videos, project suggestions, and certification opportunities - delivered straight to your inbox every Thursday at 7 PM. 
so a little update on this project- its working...!! if you have any kind of suggestions please let me know!

 
##  Features
 
- **Curated Tech Articles** - Latest articles from Dev.to on your topics
- **YouTube Videos** - Trending tutorials and tech talks
- **GitHub Repositories** - Trending repos in your tech stack
- **Project of the Week** - Hands-on project suggestions with tech stack breakdown
- **Certification Opportunities** - Latest certifications with cost transparency
- **Cost Analysis** - Clear indication if projects used FREE resources or paid
 
## Tech Focus Areas
 
- Docker & Containerization
- Automation Testing (Playwright, Selenium, Cypress)
- CI/CD Pipelines (GitHub Actions, Jenkins)
- LangChain & LLM Development
- DevOps & Infrastructure
- Quantum Technologies
- Neuromorphic Computing
- Technical Certifications
 
##  Tech Stack
 
- **Python** - Core scripting language
- **GitHub Actions** - Free CI/CD automation & scheduling
- **Gmail SMTP** - Email delivery
- **APIs Used:**
  - GitHub API (trending repositories)
  - Dev.to API (tech articles)
  - YouTube Data API v3 (video recommendations)
 
##  Cost
 
**Used only free resources**
-  GitHub Actions: FREE (2,000 minutes/month)
-  Gmail SMTP: FREE (500 emails/day)
-  All APIs: FREE tier
-  **Total: $0/month**
 
##  Schedule
 
Emails are automatically sent every **Thursday at 7 PM UTC** via GitHub Actions cron job.
 
##  Setup Instructions
 
### Prerequisites
 
- Gmail account with App Password enabled
- GitHub account
- YouTube Data API key (optional but recommended)
 
### Installation
 
1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR-USERNAME/tech-email-agent.git
   cd tech-email-agent
Set up GitHub Secrets
Go to: Settings → Secrets and variables → Actions
Add these secrets:
SENDER_EMAIL - Your Gmail address
SENDER_PASSWORD - Gmail App Password (16-character)
RECIPIENT_EMAIL - Email to receive updates
YOUTUBE_API_KEY - YouTube Data API key
Enable GitHub Actions
Go to Actions tab
Enable workflows if prompted
Manual Test Run
Go to Actions tab
Click "Weekly Tech Email"
Click "Run workflow"
Check your inbox! 
Getting Gmail App Password
Go to Google App Passwords
Select app: Mail
Select device: Other (Custom name)
Generate and copy the 16-character password
Getting YouTube API Key
Go to Google Cloud Console
Create a new project
Enable "YouTube Data API v3"
Create credentials → API Key
Copy the API key

## Email Content Structure
### Each weekly email includes:
Trending Tech Articles - 3 latest articles on your topics
YouTube Videos - 3 recommended tutorials/talks
Project of the Week - Detailed project with:
Tech stack breakdown
Time estimation
Difficulty level
Cost transparency
Learning outcomes
Certification Opportunities - 2 relevant certifications with free resources
Trending GitHub Repos - 3 popular repositories
 Customization
Modify Email Schedule
Edit .github/workflows/tech-email.yml:
schedule:
  - cron: '0 19 * * 4'  # Thursday 7 PM UTC
Cron schedule syntax
Change Tech Topics
Edit send_tech_update.py and modify the TOPICS dictionary:
TOPICS = {
    'your_topic': ['keyword1', 'keyword2'],
     }
    # Add your custom topics here
    
Project Structure

tech-email-agent/
├── .github/
│   └── workflows/
│       └── tech-email.yml      # GitHub Actions workflow
├── send_tech_update.py         # Main Python script
├── requirements.txt            # Python dependencies
├── .gitignore                  # Git ignore rules
└── README.md                   # This file
contributing
Contributions are welcome! Feel free to:
Report bugs
Suggest new features
Submit pull requests
License
- This project is open source and available under the MIT License.
Acknowledgments
- Built with Claude (Anthropic)
APIs: GitHub, Dev.to, YouTube
Hosting: GitHub Actions (free tier)
Contact
- Created by Methily Johri - feel free to reach out!

 If you find this useful, please star the repository!
---
 
## this is how the email looks like - 
<img width="1123" height="665" alt="Screenshot 2026-05-02 133008" src="https://github.com/user-attachments/assets/f9e68920-0331-492b-b4ce-576a2c6138db" />

 
### **Step 4: Push README to GitHub**
 
In VS Code terminal:
 
```bash
git add README.md
git commit -m "Add comprehensive README documentation"
git push
