# explore-github-action
Explore GitHub Workflow  
**Workflow**:  
	The overall automated process that defines when and how different actions should be executed, triggered by events like pushing code to a repository or creating a pull request.  
**Action**:
	An individual, modular step within a workflow, performing a specific task like running a unit test, deploying to a server, or checking code quality. 
How they work together:
	YAML configuration:
Both workflows and actions are defined using YAML syntax within the .github/workflows directory in your repository. 
Combining actions:
	You can combine multiple actions from either the GitHub community or custom-built actions to create a complex workflow. 
Triggering workflows:
	A workflow can be triggered by various events like pushing code, creating a pull request, or a scheduled time. 
	
A workflow must contain the following basic components:
	1. One or more events that will trigger the workflow.
	2. One or more jobs, each of which will execute on a runner machine and run a series of one or more steps.
	3. Each step can either run a script that you define or run an action, which is a reusable extension that can simplify your workflow.

A workflow trigger is an event that causes a workflow to run. There are four types of triggers:
	1. Events happening in the workflow’s GitHub repository.
	2. Events occurring outside of GitHub, which trigger a repository_dispatch event in GitHub.
	3. A predefined schedule.
	4. Manual trigger
 
 - GitHub Actions is a powerful automation platform that goes far beyond just CI/CD. While automating the CI/CD pipeline is one of the most popular use cases,
 - A GitHub Actions workflow is a process that you set up in your repository to automate software-development lifecycle tasks, including GitHub Actions
 - A "GitHub workflow" refers to a series of automated tasks defined in a YAML file within a GitHub repository, essentially a blueprint for a continuous integration and continuous delivery (CI/CD) pipeline, while a "GitHub action" is a single, reusable task within that workflow, like running a specific test or building a project, which can be combined to create a larger automated process.
 - A "GitHub workflow" refers to a series of automated tasks defined in a YAML file within a GitHub repository, essentially a blueprint for a continuous integration and continuous delivery (CI/CD) pipeline, while a "GitHub action" is a single, reusable task within that workflow, like running a specific test or building a project, which can be combined to create a larger automated process. 
 - GitHub Actions are packaged scripts to automate tasks in a software-development workflow in GitHub.
	  - Ensure the code passes all unit tests.
	  - Perform code quality and compliance checks to make sure the source code meets the organization's standards.
	  - Check the code and its dependencies for known security issues.
	  - Build the code integrating new source from (potentially) multiple contributors.
	  - Ensure the software passes integration tests.
	  - Version the new build.
	  - Deliver the new binaries to the appropriate filesystem location.
	  - Deploy the new binaries to one or more servers.
	  - If any of these tasks don't pass, report the issue to the proper individual or team for resolution.
