# Start with a minimal pipeline that you can customize to build and deploy your code.
# Add steps that build, run tests, deploy, and more:
# https://aka.ms/yaml

trigger:
- main

pool:
  santosh

steps:
# Starter pipeline
- task: UiPathRunJob@3
  inputs:
    orchestratorConnection: 'DevOpsSC'
    processName: 'CICD-UiPathProcess'
    folderName: 'Shared'
    jobType: 'TestAutomation'
    user: 'alizabista755d\alizabista'
