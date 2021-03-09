# Resource Snapshot Demo

This demo contains a snapshot split into multiple JSON files that together create a query pipeline with many rules and machine learning models. The query pipeline also comes with an A/B that is configured in a separate JSON file.

A GitHub Action is also available 

## Fork the repo

## Create an API Key
An API key will be used to communicate with the Coveo platform and deploy your snapshots. If you need help, this documentation is a good starting place https://docs.coveo.com/en/1718/manage-an-organization/manage-api-keys. When is comes to deciding which privilege to assign to your API key, you'll need to add Edit All for every type of resources that you want to deploy with your snapshot.

> For this example, you'll need: Edit fields, Edit all Query Pipelines; Edit all Machine Learning Models; View Organization

## Store the API key as a GitHub secret
You should follow this documentation to add a new secret named API_KEY that will take the key that you just created as its value. https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository

## Update the GitHub Action
In deploy_snapshot.yml, you'll need to update the ORG_ID variable to be the one of your own Coveo organization.