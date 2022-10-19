###
 # This file configures the project "Piper" pipeline of your project.
 # For a reference of the configuration concept and available options, please have a look into its documentation. 
# 
# The documentation for the most recent pipeline version can always be found at:
# https://sap.github.io/jenkins-library/ 
# 
# This is a YAML-file. YAML is an indentation-sensitive file format. Please make sure to properly indent changes to it. 
### 

### General project setup
---
 general:
    pipeline: "sap-cloud-sdk" 
    buildTool: "mta"
 stages:
    Build:
       mavenExecuteStaticCodeChecks: false
       npmExecuteLint: false
    Additional Unit Tests:
       npmExecuteScripts: false
       karmaExecuteTests: false
    Release:
       cloudFoundryDeploy: true
       tmsUpload: false
    steps:
      cloudFoundryDeploy:
        cloudFoundry: 
          apiEndpoint: "https://api.cf.us10.hana.ondemand.com"
          org: "aa208c5ftrial"
          space: "dev"
          credentialsId: "cfdeploy"
          appName: ""
        mtaDeployParameters: "-f --version-rule ALL"
     artifactPrepareVersion:
        versioningType: "cloud_noTag"