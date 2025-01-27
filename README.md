# explore-github-action
Explore GitHub Workflow  
**Workflow**:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The overall automated process that defines when and how different actions should be executed, triggered by events like pushing code to a repository or creating a pull request.  
**Action**:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;An individual, modular step within a workflow, performing a specific task like running a unit test, deploying to a server, or checking code quality. 
**How they work together**:
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
  

Types of GitHub actions
There are three types of GitHub actions: container actions, JavaScript actions, and composite actions.

With container actions, the environment is part of the action's code. These actions can only be run in a Linux environment that GitHub hosts. Container actions support many different languages.

JavaScript actions don't include the environment in the code. You'll have to specify the environment to execute these actions. You can run these actions in a VM (virtual machine) in the cloud or on-premises. JavaScript actions support Linux, macOS, and Windows environments.

Composite actions allow you to combine multiple workflow steps within one action. For example, you can use this feature to bundle together multiple run commands into an action, and then have a workflow that executes the bundled commands as a single step using that action.

A workflow must have at least one job. A job is a section of the workflow associated with a runner. A runner can be GitHub-hosted or self-hosted, and the job can run on a machine or in a container. 

Workflows
A workflow is an automated process that you add to your repository. A workflow needs to have at least one job, and different events can trigger it. You can use it to build, test, package, release, or deploy your repository's project on GitHub.

Jobs
The job is the first major component within the workflow. A job is a section of the workflow that will be associated with a runner. A runner can be GitHub-hosted or self-hosted, and the job can run on a machine or in a container. You'll specify the runner with the runs-on: attribute. Here, you're telling the workflow to run this job on ubuntu-latest. We'll talk more about runners in the next unit.

Steps
A step is an individual task that can run commands in a job. In our preceding example, the step uses the action actions/checkout@v2 to check out the repository. What's interesting is the uses: ./action-a value. This is the path to the container action that you'll build in an action.yml file.

Actions
The actions inside your workflow are the standalone commands that are executed. These standalone commands can reference GitHub actions such as using your own custom actions, or community actions like the one we use in the preceding example, actions/checkout@v2. You can also run commands such as run: npm install -g bats to execute a command on the runner.
https://learn.microsoft.com/en-us/training/modules/github-actions-automate-tasks/2c-configure-github-actions-workflow
