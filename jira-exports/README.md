# jira-exports/

Place locally downloaded JIRA CSV exports in this folder.

This folder is excluded from git (.gitignore) so CSV files 
will never be committed to the repo.

## How to get the CSV
1. Go to your JIRA board
2. Filter by the relevant label (e.g. sfproserv_cc_voice, email)
3. Export to CSV
4. Save the file here with a clear name (e.g. Email Stories.csv)

## Files referenced in agents-registry.yml
- Email Stories.csv — used by ac-test-builder for email agents
- sfproserv_cc_voice.csv — used by ac-test-builder for voice agents
