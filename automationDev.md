triggers: 

- label
  - created
  - edited
  - deleted

- un/Label = trigger when Label un/added to Issue,etc., 

Command: 
- use Template > Template defines settings group


```
If [action] > then create Label

If Label is created > [then...]
> on: label: types: created

add Label? Type? idfk
```

# GH Issues automations (Actions, Workflows) dev notes

### Automations hierarchy: 

1. Repo > GH Actions
2. Project > Workflows

docs

- triggers https://docs.github.com/en/actions/reference/workflows-and-actions/events-that-trigger-workflows#issues



## Useful triggers? 

```
(examples)
on:
  issues:
    types:
      - reopened
      - opened
```

- run when Label is [created, edited, deleted] 
- run when Issue is ...
  - opened
  - edited
  - deleted
  - transferred
  - pinned
  - unpinned
  - closed
  - reopened
  - assigned
  - unassigned
  - labeled
  - unlabeled
  - locked
  - unlocked
  - milestoned
  - demilestoned
  - typed      # Types defined in ORG settings ... https://github.com/organizations/alh-industries/settings/issue-types
  - untyped


## automation ideas

1. Issue deletion

move issue to bucket (custom Field) 

append 'DELETE' Label

every ~49hr, delete all Issues with the 'DELETE' Label /Field


1. 
1. 
2.  




## cmd

```
# runs all commands 

gh issue create -t "YOURTITLE 1" -b BODYTEXT;  
gh issue create -t "YOURTITLE 2" -b " "; # creates issue with NO body text; must include space between quotes 
gh issue create -t "YOURTITLE 3" -b BODYTEXT;

```
