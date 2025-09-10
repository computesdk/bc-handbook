# 🤖 AI-Powered Employee Onboarding

## What This Does

This repository now includes an intelligent onboarding system that automatically generates personalized employee onboarding tasks based on your actual handbook content using Claude AI.

## Quick Demo

1. **Create Issue**: Go to Issues → New Issue → Select "🤖 AI-Powered Employee Onboarding"
2. **Fill Details**: Enter employee name, role, start date, etc.
3. **Submit**: The AI will analyze the handbook and create 8-12 personalized onboarding tasks
4. **Track Progress**: Each task becomes a separate GitHub issue for easy tracking

## Setup Required

⚠️ **Important**: You need to add your Anthropic API key as a repository secret named `ANTHROPIC_API_KEY`

## Example Generated Tasks

For a **Senior Programmer** starting next week, the AI might generate:

- 🔧 **Set up Kandji and Shipshape**: Complete device management setup per getting-started.md
- 📋 **Review L3 Senior Programmer Expectations**: Study titles-for-programmers.md requirements 
- 🚨 **Begin On-Call Preparation**: Shadow current team members per L3 responsibilities
- 💰 **Enroll in 401k**: Set up retirement plan with 6% company match
- 👥 **Meet Your 37signals Buddy**: Schedule introduction call within first week
- 📅 **Join 6-Week Cycle Process**: Learn cycle structure and join next kickoff
- 💬 **Set Up Async Communication**: Configure daily/weekly check-ins per how-we-work.md

## Benefits

✅ **Always Current**: Tasks reflect actual handbook policies  
✅ **Role-Specific**: Different tasks for different positions  
✅ **Experience-Aware**: Adjusted for junior vs senior roles  
✅ **Zero Manual Work**: Fully automated task generation  
✅ **Easy Tracking**: Progress visible through GitHub issues  

## Files Added

- `.github/ISSUE_TEMPLATE/ai-onboarding.yml` - Issue template for creating onboarding requests
- `.github/workflows/ai-onboarding.yml` - GitHub Action that generates tasks
- `AI_ONBOARDING_SETUP.md` - Detailed setup and customization guide

Ready to try it? Create your first onboarding issue! 🚀