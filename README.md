# Dotnet Core CodeDeploy Demo Repo

This repository is intended to demonstrate the ability to deploy a sample ASP .NET app to AWS using **GitHub Actions**. The process is as such

1. Changes are made to the repo and pushed onto the `main` branch
2. `deploy.yml` workflow will be executed doing a simple _CI_ job (building) followed by a _CD_ job (deploying).
3. The deployment is made to AWS CodeDeploy, which then sends this information to a VM instance where the application is hosted
4. You can access this application via the IP [3.219.63.62](http://3.219.63.62)

### Resetting to go through the exercise yourself

- [ ] Copy this repository template if you haven't already
- [ ] If you want to deploy to AWS, make sure you have your appropriate `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` stored as Secrets within the repository (so that the deploy workflow can use them
- [ ] Clone the repository locally in your directory: `git clone https://github.com/<YOUR_USERNAME>/dotnet-deploy.git`
- [ ] Reset to commit before Actions were introduced. To find the SHA go into the commit history and check the latest commit labeled 'RESET COMMIT': `git reset --hard <SHA>`
- [ ] Push back to GitHub: `git push origin -f`
- [ ] Make sure you have deleted all workflow runs
- [ ] Make sure you have close the Code Scanning Workflow PR


The Application is pulled from @martinjt's repo found [here](https://github.com/martinjt/codedeploy-dotnet), with some slight modifications.
