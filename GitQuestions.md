# Github studies
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

## Take aways
- source of truth on version control timeline lives in Github
- someone viewing the salesforce org isn't necessarily viewing the main branch of code

## questions
- in a production org, what location is the source of truth?
- what is the process of 'deploying to production' when developer/sandbox orgs aren't necessarily the same thing as developer branches in Github (different tracking systems)
- process for aligning VCS Audit Trail of an org vs VCS in Github

# github practice
*approach for workflow*
> "Edit, stage, commit"
- clone homework from github to local machine
- create branch for homework assignment
  - create sub-branch for problem sets
    - make edits
    - save locally
    - deploy to authorized org
    - execute test classes
    - repeat until tests pass
    - `add` & `restore` can be used to stage & rollback changes to files
    - git commit to branch
  - once a number of commits (units) are satisfactory, test collective batch and merge into parent branch
  - clean up working branch (delete)
  - create new branch for next problem sets
  - once all work is completed and merged, run full test suite, repeat sub steps until pass
- merge back into `main` branch for submitting homework
- clean out any unneeded branches
- deploy main branch to org again so org is sync'd with github