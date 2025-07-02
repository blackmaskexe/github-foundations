
- they are markdown templates that are preloaded for new Issues
- Help ensure users create issues that fit a relevant format
- You can create multiple issue templates to better improve contexts of issues
![[Pasted image 20250628114458.png]]

## Default Issue Templates (3):
- these defaults are only available when you create an issue template in the community standards

![[Pasted image 20250628121447.png]]

## Where to store Issue Templates:
1. create a new folder `.github/ISSUE_TEMPLATE`
2. create as many md files inside of this folder for different types of issue reports
   ![[Pasted image 20250628114647.png]]
## Specific Formatting for an Issue Template File:
- you are required to add a front-matter on top of the md template file:
```md
---
name: Issue Type
about: description
title: ''
labels: whateverlabelsyouwanttoassign
assignees: ''
---

## <issue Type> Issue
- you would lay out your issue template as normal here
```

## GUI Issue Template Maker:
- navigate to `repo -> insights -> community standards -> crete issue template`
- the above will walk you through creating an issue template for your repo
-  the template that you add here will be visible as options for user to select when creating a new issue