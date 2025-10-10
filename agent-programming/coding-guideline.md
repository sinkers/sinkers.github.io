# Coding Guidelines

For agents and humans!

## General
* Do you have a good definition of what needs to be done?
* If someone has given you a one line Jira ticket that doesn't have enough detail ask for more information
* If writing a Jira ticket make it a good one, just having a title is not a good Jira ticket see https://github.com/sinkers/sinkers.github.io/blob/main/agent-programming/writing-a-good-jira-ticket.md
* Is there a clear definition of what defines this task as being done?
* For new repositories start with only a very basic scaffold before starting to work on branches and getting PRs reviewed

## Writing
* Keep code simple and easy to read
* Do not use language magic tricks unless you really need to
* Keep in mind often the best code is no code at all
* Make sure your code is idiomatic for the language you are writing it in
* Work should always be done on a branch, do not write and commit code on the main branch. If using a gitflow style workflow do not work on deployment branches
* When your code is ready a PR should be raised, this should be reviewed even if just using agents to review
* Any comments on the PR should be addressed or responded to and resolved before merging

## Code Quality
* Make sure there is appropriate linting applied for the language and this is run via CI
* Make sure that there is a security scan running in CI
* Run a complexity check on each PR and check that the new code is not making the codebase overly complex
* Use other agents for reviewing PRs

## Tooling
* Don't unneccsarily introduce new tools to the project, use what is already there first, introduce new tools in separate branches/PRs
* Make sure that any package configurations e.g. requirements.txt, packages.json are updated if new packages are added
* Include a Makefile that covers all the basics such as build, test and install

## Testing
* Working out how the code is going to be tested before writing and if practical create some tests cases that can define what is done
* All code should be covered by unit tests up to the maximum coverage practival
* Code coverage with unit tests should not decrease
* There should be integration tests
* There should be end to end tests
* Testing should be contained to the location that is idiomatic for the languages and packages used

## Documentation
* Any changes made should be reflected in the documentation, do not leave documentation that is no longer relevant due to changes that have been made

## CI/CD
* Test must pass to merge the code into the main, staging or production branches
* Tests should run on all commits
* It must be possible to do deploys of feature branches to dev environments but not to staging, production or main
* Deployment should be handled by the CI workflow and not reliant on manual deployment steps
* It must be possible to easily rollback changes
