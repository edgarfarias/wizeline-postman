# wizeline-postman

- ### To run the all the tests for the **task** endpoint:

  Install the requered packages:

  `npm run i`

  and then:

  `npm run test-tasks`

- ### Proposal to run tests from CI/CD pipeline and avoid checking in sensitive data to the repository:

  1. Store API token in a **secret** or any other similar mechanism of the CI/CD provider.
  2. When the pipeline is created, on the stage to run the postman tests, that secret can be passed directly to the command used for running postman as follows:

     `npm run test-tasks-pipeline -- --env-var token='$TOKEN_FROM_SECRET'`
