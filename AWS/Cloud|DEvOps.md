
# CI/CD
Build - Test - Analyze - Deploy - Verify - Promote
Eight principle of CI/CD
1. Repeatable Reliable Process
2. Automate Everything
3. Version Control Everything
4. Bring the Pain Forward
5. Build-in Quality
6. "Done" Means Released
7. Everyone is Responsible
8. Continuous Improvement

# CI
- Compile
- Unit Test
- Static Analysis
- Dependency vulnerability testing
- Store artifact

# CD
- Creating infrastructure
- Provisioning servers
- Copying files
- Promoting to production
- Smoke Testing (aka Verify)
- Rollbacks

# CI/CD stages
- Build
Everything that has to do with making code executable in production (e.g. Compile). The goal is to produce an artifact.
- Test
All automated tests that verify at the code level.
- Analyze
Analyze	Any static analysis on the code or checking of dependencies.
- Deploy
Anything to do with creating server instances or copying pre-built application files to an instance.
- Verify
Any tests that can be run against a running instance of the application, often against a pre-production instance.
- Promote
Replacing the current production environment with the new version which was just built and deployed.
- Revert	
Rolling back or undoing changes in case any verification fails after deployment.

# Deployment strategies
### big bang
Replace A with B all at once. Somehow it means that we don't really have a deployment strategy.
### Blue Green
Two versions of production: Blue or previous version and Green or new version. Traffic can still be routed to blue while testing green. Switching to the new version is done by simply shifting traffic from blue to green.
### Canary
Aka Rolling Update, After deploying the new version, start routing traffic to new version little by little until all traffic is hitting the new production. Both versions coexist for a period of time.
### A/B Testing
Similar to Canary, but instead of routing traffic to new version to accomplish a full deployment, you are testing your new version with a subset of users for feedback. You might end up routing all traffic to the new version, but that's always the goal.

# CI/CD tools
## On prem
### Jenkins	 (Various Contributors)
Vibrant open-source communbity, 100% free
### Gitlab (Gitlab Community)		
Open-source, installable version of the popular cloud-based service, 100% free
### Team City	(JetBrains)
Very mature, JetBrains support
### Team Foundation Server (TFS)	(Microsoft)	
Seemless integration with Microsoft products, Microsoft support
## Cloud-Based
### Bamboo	(Atlassian)	
Integrates well with other Atlassian products like Stride and Jira.
### Circle CI	(Circle Internet Services)	
Free for limited use, personal or business. Boasts of faster builds.
### Travis CI	(Travis CI)	
Extremely simple CI/CD orchestration tool. Some specialty features for libraries and packages. Free for open-source projects.
### GitLab	(GitLab)	
Complete set of development tools including git repositories and built-in, integrated CI/CD pipelines. 2000 free minutes of CI/CD jobs per month.

# CI with Circle CI
- Singe responsability principle
- Env Variable
- Sharing information: 
1. Cache
   - Only to share file during pipeline execution (great for file that takes time to downlaod like node modules)
2. workspace
   - equivalent to Cache, but no kets and can stick around.
3. Secret Keeper.

workplace and secrets.
- Reusable code.(Anchor & Aliase, Commands)

- Reusable Code.

# CD Ansible
- Deliver the value quickcly
- CD Intuition(Review)
- Ansible playbook

# Moniroting - Prometheues
- Other monitoring tool: 
1. Time-Series Data
2. Data aggregator
3. Data Visualizer

## Configuration Management and Automation Tools
Chef	chef.io	Depends on agent to be installed. Very mature.
Puppet	ouppet.com	Requires master "puppet master" server. Performance issues.
Salt	saltstack.com	Keeps inventory on a central server.
Ansible	ansible.com	Most popular. Very fast. Agentless.