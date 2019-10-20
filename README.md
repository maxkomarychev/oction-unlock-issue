# Unlock an issue

"Oction" is a GitHub Action that implements a single call with 
[@octokit/request](https://www.npmjs.com/package/@octokit/request)
allowing easy interaction with GitHub REST APIs from your workflow.

Original documentation: https://developer.github.com/v3/issues/#unlock-an-issue

This action implements `DELETE` request to `/repos/{owner}/{repo}/issues/{issue_number}/lock`


# Quick start

```yaml
- uses: maxkomarychev/oction-unlock-issue@v0.7.1
  id: my_step_id
  with:
    token: <token value>
    issue_number: <issue_number value>
- name: Print outputs
  run: |
    echo ${{ steps.my_step_id.outputs.id }}
    echo ${{ steps.my_step_id.outputs.number }}
```


# Inputs

| Name | Is required | Description |
|---|---|---|
|token|true|Token to authenticate the request
|owner|false|owner parameter
|repo|false|repo parameter
|issue_number|true|issue_number parameter

# Outputs

| Name | Description |
|---|---|
|id|`id` field of the response (if exists)|
|number|`number` field of the response (if exists)|

# Friendly octions

* [oction-create-deployment-status](https://github.com/maxkomarychev/oction-create-deployment-status)
* [oction-create-deployment](https://github.com/maxkomarychev/oction-create-deployment)
* [oction-create-issue](https://github.com/maxkomarychev/oction-create-issue)
* [oction-create-release](https://github.com/maxkomarychev/oction-create-release)
* [oction-lock-issue](https://github.com/maxkomarychev/oction-lock-issue)
* [oction-merge-pull-request](https://github.com/maxkomarychev/oction-merge-pull-request)
* [oction-unlock-issue](https://github.com/maxkomarychev/oction-unlock-issue)
