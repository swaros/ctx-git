# ctx-git
contxt git helper tasks 

for using in a `.contxt.yml` file to collect some information about the current git status.
this information can be used to make decisions in youre own .contxt.yml

## usage
 ```yaml
config:
  require:
    - swaros/ctx-git
 ```

## variables 

### GIT-CHANGES
contains all files they changed as a text-blob. needs **check-have-changes** was executed.
is empty if no local changes found.

usecase for no local changes
```yaml
require:
      variables:
        GIT-CHANGES: ""
```


usecase for having local changes
```yaml
require:
      variables:
        GIT-CHANGES: "*"
```

### GIT-BRANCH

contains the name of the branch `${GIT-BRANCH}`

### GIT-URL

contains the url `${GIT-URL}`
