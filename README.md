# Reproduction of issue https://github.com/github/docs/issues/33389

In a Github Workflow when runs-on is dynamically set via an environment variable the workflow fails with and error like "Error when evaluating 'runs-on' for job 'hello-world-job'. .github/workflows/runner-env-var-repro.yml (Line: 10, Col: 14): Unexpected value ''" as can be seen here: https://github.com/withakay/runner-env-var-repro/actions/runs/10021021920



The workflow code is here: https://github.com/withakay/runner-env-var-repro/blob/main/.github/workflows/runner-env-var-repro.yml

The image below shows the configuration for the 'dev' environment in this repository where a variable called 'RUNNER' has been set to 'ubuntu-latest'

![Repo Dev Environment vars](repo_dev_environment_vars.png?raw=true "Repo Dev Environment vars")

NOTE: Use of a repository variable (not an environment variable) works as expected.