# 🤖 AI-Powered Employee Onboarding Setup

This system automatically generates personalized onboarding tasks based on your employee handbook content using Claude AI.

## 🚀 Quick Start

### 1. Add Required GitHub Secret

You need to add your Anthropic API key to your repository secrets:

1. Go to your repository **Settings** → **Secrets and variables** → **Actions**
2. Click **New repository secret**
3. Name: `ANTHROPIC_API_KEY`
4. Value: Your Claude API key from [Anthropic Console](https://console.anthropic.com/)

### 2. Enable GitHub Actions

Ensure GitHub Actions are enabled in your repository:
- Go to **Settings** → **Actions** → **General**
- Allow all actions and reusable workflows

### 3. Test the System

1. Go to **Issues** → **New Issue**
2. Select **🤖 AI-Powered Employee Onboarding** template
3. Fill out the employee details
4. Submit the issue
5. Watch as the workflow automatically generates personalized onboarding tasks!

## 📋 How It Works

### The Process

1. **Issue Creation**: Someone creates a new onboarding issue using the template
2. **Context Collection**: Workflow reads all handbook markdown files
3. **AI Analysis**: Claude analyzes handbook content and employee details
4. **Task Generation**: AI creates 8-12 personalized onboarding tasks
5. **Issue Creation**: Each task becomes a separate GitHub issue
6. **Progress Tracking**: Teams can track progress through GitHub issues

### What Gets Generated

The AI creates tasks that are:

- **📚 Policy-Specific**: References actual handbook sections
- **👤 Role-Appropriate**: Different for programmers vs designers vs support
- **📅 Timeline-Based**: Structured across Week 1 → Month 1 → Month 3
- **🌍 Location-Aware**: Accounts for US vs international employees
- **🎯 Experience-Level Appropriate**: Adjusted for junior vs senior roles
- **🏢 Culture-Integrated**: Includes 37signals-specific practices

### Example Generated Tasks

**For a Senior Programmer:**
- 🔧 Set up Kandji and Shipshape device management (Week 1)
- 📋 Review L3 Senior Programmer expectations and discuss growth path with tech lead
- 🚨 Begin on-call rotation preparation with shadowing current team members
- 💬 Set up async communication practices per how-we-work.md guidelines

**For an International Employee:**
- 🏥 Set up health insurance reimbursement process (75% coverage up to US plan limits)
- 💰 Configure international retirement plan matching (up to 6% of salary)
- 📍 Notify People Ops of location for tax compliance

## 🔧 Customization

### Modifying the Employee Roles

Edit `.github/ISSUE_TEMPLATE/ai-onboarding.yml` to add/remove role options:

```yaml
- type: dropdown
  id: role
  attributes:
    label: Primary Role
    options: 
      - "Your Custom Role Here"
      # ... existing roles
```

### Adjusting Task Generation

The AI prompt in `.github/workflows/ai-onboarding.yml` can be customized to:
- Change the number of tasks generated
- Modify the focus areas
- Adjust the task format
- Add company-specific requirements

### Adding Custom Labels

Tasks are automatically labeled with:
- `onboarding-task` (all tasks)
- Priority level (`high-priority`, `medium-priority`, `low-priority`)
- Custom labels from the AI (like `technical`, `benefits`, `culture`)

## 📊 Tracking and Management

### Finding Generated Tasks

All onboarding tasks can be found by filtering issues:
- Label: `onboarding-task`
- Use GitHub's issue filters: `is:issue label:onboarding-task`

### Progress Tracking

- ✅ **Completed**: Close the issue when task is done
- 🔄 **In Progress**: Add comments and updates
- 👥 **Assignments**: Assign tasks to appropriate team members
- 📅 **Milestones**: Group tasks by timeline (Week 1, Month 1, etc.)

### Team Management

The system generates tasks that should be assigned to:
- **New Employee**: Self-guided tasks like reading policies
- **Manager**: 1:1 scheduling, goal setting
- **Ops Team**: Account setup, access provisioning
- **Buddy/Mentor**: Introduction and cultural integration

## 🎯 Benefits

### For HR/People Operations
- ✅ Consistent onboarding experience
- ✅ No missed steps or forgotten tasks
- ✅ Automatic policy compliance
- ✅ Easy progress tracking

### For Managers
- ✅ Role-specific guidance
- ✅ Clear expectations and timelines
- ✅ Reduced planning overhead
- ✅ Handbook-driven consistency

### For New Employees
- ✅ Personalized experience
- ✅ Clear next steps
- ✅ Policy context and references
- ✅ Cultural integration

### For the Organization
- ✅ Scales with company growth
- ✅ Always up-to-date with handbook changes
- ✅ Data-driven onboarding insights
- ✅ Reduced manual coordination

## 🔍 Troubleshooting

### Workflow Not Triggering
- Check that the issue has the `onboarding` label
- Verify GitHub Actions are enabled
- Check the Actions tab for error logs

### API Key Issues
- Ensure `ANTHROPIC_API_KEY` secret is set correctly
- Verify your Claude API key has sufficient credits
- Check API key permissions

### No Tasks Generated
- Check the Actions logs for Claude API errors
- Verify the handbook markdown files are readable
- Ensure the issue template data is being parsed correctly

### Tasks Not Created as Issues
- Check GitHub token permissions
- Verify the repository allows issue creation
- Review the task parsing logic in workflow logs

## 🔮 Future Enhancements

Potential improvements to consider:

- **📧 Email Notifications**: Send task summaries to managers
- **📊 Analytics Dashboard**: Track onboarding completion rates
- **🔄 Continuous Updates**: Regenerate tasks when handbook changes
- **🎯 Progress Milestones**: Automatic milestone creation and tracking
- **💬 Slack Integration**: Post task updates to team channels
- **📅 Calendar Integration**: Add task due dates to calendars

## 🆘 Support

If you encounter issues:

1. Check the **Actions** tab for workflow execution logs
2. Review the **Issues** for any error reports
3. Verify your API key and permissions
4. Test with a simple onboarding issue first

---

**Ready to transform your onboarding process?** 🚀

Create your first AI-powered onboarding issue and watch the magic happen!