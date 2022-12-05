[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/MercymeIlya/last-workflow-status/blob/master/LICENSE)

# Credit

This action was taken in its entirety and changed only slightly from [last-workflow-status](https://github.com/MercymeIlya/last-workflow-status) to return the completed_at field instead of the status.

# Last workflow completed_at

Simple GitHub action to get previous workflow completed_at. Was inspired by sending notification after build status changing in 
[Travis CI](https://docs.travis-ci.com/user/notifications/#changing-notification-frequency).
```yaml
notifications:
  slack:
    rooms: slack_room
    on_success: change
```

## Inputs:
### `github_token`
* Secret GitHub API token to use for making API requests.  
`default: ${{ github.token }}`

## Outputs:
### `last_completed_at`
* Completed_at value of last workflow.

See https://docs.github.com/en/rest/checks/runs#create-a-check-run--parameters completed_at parameter.
     