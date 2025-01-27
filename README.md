# explore-github-action
Explore GitHub Workflow 

 - GitHub Actions is a powerful automation platform that goes far beyond just CI/CD. While automating the CI/CD pipeline is one of the most popular use cases,
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
