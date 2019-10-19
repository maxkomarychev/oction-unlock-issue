# Unlock an issue

"Oction" is a GitHub Action that provides access to 
[octokit's](https://octokit.github.io/rest.js) functionality allowing easy 
interaction with GitHub REST APIs

Original docs can be found here: https://developer.github.com/v3/issues/#unlock-an-issue

This action implements DELETE request to /repos/{owner}/{repo}/issues/{issue_number}/lock


# Quick start

```yaml
- uses: oction-unlock-issue@v0.5.1
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

