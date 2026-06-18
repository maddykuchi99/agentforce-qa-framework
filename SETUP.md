# Setup Guide

## Creating the GitHub Repository

### Step 1: Initialize Git Repository

```bash
cd /Users/mkuchimanchi/Documents/agentforce-qa-framework
git init
git add .
git commit -m "Initial commit: Agentforce QA Test Automation Framework"
```

### Step 2: Create GitHub Repository

1. Go to https://github.com/new
2. Repository name: `agentforce-qa-framework`
3. Description: `Automated testing framework for Salesforce Agentforce agents with intelligent failure analysis`
4. Choose "Public"
5. **Do NOT initialize with README, .gitignore, or license** (we already have these)
6. Click "Create repository"

### Step 3: Push to GitHub

```bash
# Replace maddykuchi99 with your GitHub username
git remote add origin https://github.com/maddykuchi99/agentforce-qa-framework.git
git branch -M main
git push -u origin main
```

### Step 4: Configure Repository Settings

1. Go to repository Settings → General
2. Under "Features", enable:
   - ✅ Issues
   - ✅ Discussions
   - ✅ Wikis (optional)
3. Under "Social preview", add:
   - Image: Upload a screenshot of a digest report
   - Description: Same as repo description

### Step 5: Add Topics/Tags

In your repository main page:
1. Click the gear icon next to "About"
2. Add topics:
   - `salesforce`
   - `agentforce`
   - `qa-automation`
   - `testing`
   - `claude-code`
   - `test-framework`

---

## For New Users (After Repo is Public)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/maddykuchi99/agentforce-qa-framework.git
   cd agentforce-qa-framework
   ```

2. **Copy to your Salesforce project**
   ```bash
   # Copy framework files to your project
   cp -r .claude /path/to/your/salesforce/project/
   
   # Create qa-digests directory
   mkdir -p /path/to/your/salesforce/project/qa-digests
   ```

3. **Configure your agents**
   ```bash
   cd /path/to/your/salesforce/project
   cp .claude/agents-registry.yml.example .claude/agents-registry.yml
   ```

4. **Edit the registry**
   ```bash
   # Edit with your preferred editor
   nano .claude/agents-registry.yml
   ```

5. **Retrieve your agent metadata**
   ```bash
   sf project retrieve start \
     --metadata "GenAiPlannerBundle:Your_Agent_Bundle_Name" \
     --target-org your-org-alias
   ```

6. **Run your first test**
   ```bash
   claude -p "Use the qa-test-agent for your-agent-name"
   ```

---

## Troubleshooting Installation

### "Claude Code not found"
Install Claude Code:
- **CLI**: https://claude.ai/code
- **Desktop**: https://claude.ai/download
- **VS Code Extension**: Search "Claude Code" in Extensions

### "Salesforce CLI not authenticated"
```bash
# Authenticate to your org
sf org login web --alias your-org-alias

# Verify authentication
sf org list
```

### "Agent not in registry"
- Check `.claude/agents-registry.yml` exists
- Verify agent name matches exactly (case-sensitive)
- Ensure YAML syntax is correct (no tabs, proper indentation)

---

## Next Steps After Installation

1. **Run baseline tests** for all your agents
2. **Review sample digests** in `examples/sample-digests/`
3. **Set up daily testing** routine
4. **Customize** test-set-builder for your use cases
5. **Share results** with your team

---

## Support

- **Issues**: https://github.com/maddykuchi99/agentforce-qa-framework/issues
- **Discussions**: https://github.com/maddykuchi99/agentforce-qa-framework/discussions
