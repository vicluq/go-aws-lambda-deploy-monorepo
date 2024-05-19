# Deploy a Monorepo of Golang Lambdas

Preveiously, I have created a workflow to deploy a lambda considering that the repository represents a single lambda function.

But, in most cases there will be a monorepo with many folders, each representing a lambda, so I have decided to create a lambda that would consider that scenario.

## How to use this action?

1. Each lambda service should have it's own folder
2. The lambda will be named as follows: `${REPO_NAME}-${SERVICE_FOLDER}`
3. The `main.go` file should be at the service folder root of course.
4. All the shared code inside the monorepo should be in the `shared` folder.
5. Every new created service (folder) should be added to the matrix variable called `service_folders` in the workflow.
