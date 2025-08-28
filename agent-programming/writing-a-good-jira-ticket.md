# Writing a Good Jira Ticket

> **Ask yourself: if an alien landed on Earth and got handed your Jira ticket, would they know what to do with it?**

## General Guidelines for Writing a Good Jira Ticket
* A good Jira ticket should not just have a title
* The title should be short and to the point
* If there are many similar tickets, try to add some context
* Don't rewrite any context that could be derived from the project, story, or epic into the ticket
* The ticket needs to provide some context as to what is being done; some of this can be inferred from the project and the ticket
* The description of the ticket should provide detailed instructions on what needs to be done and ideally in what order
* There should be a clear definition of what is done
* Assuming that there is some kind of review step, then the done clause should also include clear acceptance criteria
* Do not do design in the comments section; if the info is critical to getting the task done, put it back into the main description
* Think of yourself as someone having just joined the company and searching through old Jira tickets—will you be easily able to understand what this ticket was about and what was achieved?
* Try to get the critical information into the ticket's description, including critical excerpts to supporting documentation. Don't rely on links to massive specification documents without making it easy to get to the relevant section

## Example Ticket

**Title:** Refactor the codebase to a monorepo

**Repository:** github.com/sinkers/mywebapp

### Context

Currently the repo is a bit of a mess and there are people working on multiple parts of the project at the same time, but it is not easy to integrate and test. As the project is a Next.js webapp, the likely best path forward is going to be to properly structure the project as a monorepo.

Check here for some additional info: https://medium.com/@omar.shiriniani/mastering-next-js-monorepos-a-comprehensive-guide-15f59f5ef615

### What to Do

* Review the codebase and come up with a plan to move it to a monorepo with the most appropriate tooling
* Do some research on what is going to be the best tool to manage the build of the monorepo
* Look at what structure is best practice for using that tooling
* Come up with a plan to apply that tooling to the project

### Definition of done

* The application builds with the new tooling on the local dev environment
* It is now easy for different people to work on different components of the project without causing unnecessary merge conflicts (i.e., a user can keep all their work contained to a directory for a specific feature)
* Each component can be easily tested on a local dev environment
* The CI can build the application with the new tooling
* All tests pass
* All the documentation is updated with clear instructions for migrating and new users on how to use the tooling to build the project

