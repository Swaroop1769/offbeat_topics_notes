Application Lifecycle Management (ALM)

events --triggers--> Workflows --contains--> Jobs --use--> Actions

1. on
2. workflow_dispatch
3. repository_dispatch
4. runs-on
5. needs - for job dependency
6. jobs
7. GitHub hosted runners & Self-Hosted Runners
8. using workflow_run_logs - more debugging
9. Matrix(allows running jobs with multiple configs)
10. environment variables: env: in workflows
11. composite action: bundle mutiple workflow steps together into a reusable unit.
	--> uses multiple run or uses steps
	regular workflow -- lives in .github/workflows/
	composite action --> stored in .github/actions/
12. default job timeout: 360 min/6 hours
	if custom timeout how? timeout-minutes: ----
13. continue on error: true or false  to continue the job 
14. GITHUB_TOKEN --> auto-generated token for authentication
------------------------------------------------------------

workflows - are automated processes
step      - individual task within a job
github actions workflows are stored at? - .github/workflows

actions/upload-artifact
actions/download-artifact
default shell in Github actions - BASH
can we use powershell - by specifying - shell: pwsh
run: ./script.sh --> to run specific script in a step
reusable workflow: a workflow that can be called in another workflow (to call it uses: path to workflow)
status of previous step: if:success() or if: failure()
cache dependencies? actions/cache

------------------------------------------
How do you debug a failing GitHub Action?
enable ACTIONS_STEP_DEBUG secret.

How do you rollback a failed deployment?
use previous release or redeploy a stable version

how do you pass data between jobs?
using artifacts or o/p

GitHub Actions:

ALM -> Application Lifecycle Management tool to manage entire application

Allows us to create workflows, that can act as CI/CD pipelines and get app code from Git repos and deploy it to environments (Cloud etc)


Actions are a feature enabling GitHub to run pipelines:

On --> trigger for workflow (like on the command of push or pull do this work)

Workflow_dispatch --> we can manually run the workflow with this command

Runs-on --> command for runner name 
Eg: runs-on: ubuntu:latest

Events triggers Workflows, Workflows contains Jobs, Jobs use Actions 