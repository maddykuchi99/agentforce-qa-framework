# Sanitization Checklist

This file confirms all org-specific and proprietary details have been removed from the public repository.

## ✅ Sanitized Files

### Configuration
- [x] `.claude/agents-registry.yml.example` - Replaced with generic example config
  - Removed: `full2` org alias
  - Removed: `ACC_Footwear_Email_Agent`, `ACC_Sweaty_Betty_Email_Agent`
  - Removed: Specific topic lists and action names
  - Added: Generic `my-service-agent` example

### Examples
- [x] `examples/sample-digests/sample-agent-digest.md` - Created generic example
  - Removed: `acc-footwear-email-agent`, `full2`, `FW_Email_Regression`
  - Removed: Specific test utterances with company data
  - Added: Generic `my-service-agent`, `qa-sandbox` examples

- [x] `examples/sample-digests/sample-fleet-rollup.md` - Created generic example
  - Removed: Specific agent names and org details
  - Added: Generic `service-agent-1`, `service-agent-2`, `email-agent-1`

## 🔍 Verified Clean

### Subagent Definitions
- [x] `.claude/agents/qa-test-agent.md` - No org-specific details (generic framework code)
- [x] `.claude/agents/qa-fleet-rollup.md` - No org-specific details (generic framework code)
- [x] `.claude/agents/test-set-builder.md` - No org-specific details (generic framework code)

### Documentation
- [x] `README.md` - Generic examples only
- [x] `SETUP.md` - Generic instructions (local path reference is OK)
- [x] `CONTRIBUTING.md` - Generic guidelines
- [x] `LICENSE` - Generic MIT license

## 🚫 What's NOT in the Repo

The following are intentionally excluded (via .gitignore):
- Actual agent registry with real agents (`.claude/agents-registry.yml`)
- Generated test reports (`qa-digests/`)
- Salesforce metadata from specific orgs (`force-app/`)
- Any `.env` or environment-specific configs

## ✅ Ready for Public Release

This repository contains:
- Generic framework code
- Example configurations (with placeholder values)
- Sample reports (with generic/sanitized data)
- Comprehensive documentation

No proprietary information, company names, or org-specific details are exposed.

---

**Last verified:** 2024-01-15
**Verified by:** Framework maintainer
