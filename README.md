# About

[<img align="right" width="200px" src="https://planview-media.s3.us-west-2.amazonaws.com/wp-content/uploads/2022/10/azure_devops_-_new_logo.png" />](https://azure.microsoft.com/en-us/products/devops/pipelines)

This repository contains real life examples of Azure DevOps pipelines for running automated tests.

# Contents

`templates` - templates of jobs and reusable steps.
`variables.yml` - template containing variables and constants.
`on-demand.yml` - pipeline definition for manual test run. Contains all possible filters.
`all-qa.yml` - pipeline definition to run all test on qa environment. Triggered by push to main.
`scheduled` - pipeline definitions for scheduled test runs.

# What it does
All workflows more or less go through the same flow:
1. Pulls the repo
2. Calculates the variables
3. Installs required version of dotnet
4. Restores the solution
5. Runs test with *dotnet test*
6. Publishes test results
7. Sends email report with run highlights
8. Publishes html test report as a run artifact

# Information
More information about [Azure DevOps Pipelines](https://azure.microsoft.com/en-us/products/devops/pipelines).