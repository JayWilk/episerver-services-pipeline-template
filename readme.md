# Azure Pipeline template compatible with Episerver DXP deployments

This repository contains a YAML file that can be plugged into an Azure DevOps pipeline to trigger a build upon changes being comitted into a specific branch, and output an artifact in a compatiable format that is recognised by the Episerver DXP deployment pipeline
# Configuration
The YAML file contains the following variables which can be amended as necessary. 
- **developmentBranchName**: default value is `develop` - based on the assumption that GitFlow is being used. When changes are checked into this branch, a build is triggered.
- **solution**: path to the .sln file. Default is a wildcard to search for the solution file automatically. In instances with multiple solutions, feel free to configure this appropriately.
- **buildPlatform**: default value is `Any CPU`
- **buildConfiguration**: defaults to `Release`
- **npmDirectory**: this is the directory which contains the package.json file
