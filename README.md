[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/MercymeIlya/last-workflow-status/blob/master/LICENSE)

# Credit

This action was taken in its entirety and changed only slightly from [last-workflow-status](https://github.com/MercymeIlya/last-workflow-status) to return the created_at field instead of the status.

# Last workflow created_at

Simple GitHub action to get previous workflow created_at. Was inspired by sending notification after build status changing in 
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
### `last_created_at`
* Created_at value of last workflow.

See https://docs.github.com/en/rest/checks/runs#create-a-check-run--parameters created_at parameter.
     
