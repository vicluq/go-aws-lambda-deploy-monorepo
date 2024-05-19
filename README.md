# Deploy a Monorepo of Golang Lambdas

Preveiously, I have created an action to deploy a lambda considering that the repository represents a single lambda function.

But, in most cases there will be a monorepo with many folders, each representing a lambda, so I have decided to create a lambda that would consider that scenario.

## How to use?

1. Each lambda service should have it's own folder with it's name representing the service (the function name will be the same as the folder name so be aware).
2. The `main.go` file should be at the service folder root of course.
3. All the shared code inside the monorepo should be in the `shared` folder.
4. Every new created service (folder) should be added to the matrix variable called `service_folders` in the workflow.
