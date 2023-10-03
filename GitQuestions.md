## Assumptions
- authorized in a trailhead org
- version control is being handled in Github
- components
  - code on github
  - code on local computer
  - salesforce org

## Observations
- The act of saving a file in VS code only locks in any changes locally
  - the git timeline (local or remote) is not impacted
  - can be modified in settings to deploy to salesforce org automatically
- `Deploy to source` in VS Code as described by developer.salesforce.com: "Deploy metadata to an org from your local project"
  - files *saved* locally are deployed to Authorized Org
  - no impact to git timelines (local or remote)
- Running test classes
  - ensure saves have been deployed to org as tests are run on org, not on local data