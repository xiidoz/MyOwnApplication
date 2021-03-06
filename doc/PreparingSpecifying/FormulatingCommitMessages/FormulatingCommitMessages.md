# Formulating Commit Messages

Development of documentation, specification and code shall be collaborative. This includes reviewing artifacts before consolidating them into the shared base. Such review is not just "additional work", but also time critical, because the shared base might change between MergeRequest and MergeCommit.  
Well formulated CommitMessages must support efficiently reviewing the contributed artifact.

|![commit_3](https://user-images.githubusercontent.com/57349523/155990223-e85bd072-25e7-4650-971a-029f401d908a.jpg)|
|---|

This document provides guidance on 
* how to formulate concise and comprehensive headlines
* how to create references on existing documentation like the underlying issue in the commit messages

![commit_4](https://user-images.githubusercontent.com/57349523/155999762-51af5839-20d3-4cb4-9189-c8d442cb9e34.jpg)

### Format

Subject line: 
* short summary
* 50 characters or less (GitHub and some IDEs truncate commit messages in lists to 50 characters)
* do not end the subject line with a dot

Message body:
* separate subject from body with a blank line
* bullet points can be used
* capitalize each paragraph
* use the imperative mood in the subject line
* wrap lines at 72 characters
* use the body to explain *what* and *why* something has been done vs
* details about *how* a change has been made can be left out in most cases

### Subject line

* write the commit message in the imperative: e.g. "Add ServiceList" not "ServiceList added" or "Adds ServiceList"; this convention matches with commit messages generated by commands like git merge and git revert
* a properly formed commit subject line should always be able to complete the following sentence: "if applied, this commit will *\<subject line here\>*
* start the subject line with one of the following keywords (followed by a ":") for consistency:
  * Add
  * Fix
  * Merge
  * Polish
  * Refactor
  * Release
  * Remove
  * Revert
  * Update
* If the commit refers to an issue, end subject line with "(#issue-number)" and the commit will be mentioned in the issue
* If the commit even solves the issue, end subject line with "(fixes #issue-number)" and the issue will automatically be closed

### Message body

* what effects does the change have
* describe why a change is being made
* how does it address the issue
* do not assume that reviewers understand what the original problem was
* do not assume the change/code is self-evident/self-documenting
* read the commit message to see if it hints at improved code structure etc.
* describe any limitations of the current code or delivery item
* do not include patch set-specific commands
* If documentation from inside GitHub or external pages should be referenced, these can be linked by \[add link text in square brackets\]\(add link URL in parenthesis\)
    
### GitHub vs. VSCode commit message

The commit message dialogue differs slightly between GitHub and VSCode as below screenshots show.

|**GitHub**|**VSCode**|
|---|---|
|The subject line and body have own text fields.|There is only a single textfield (add linebreaks <br>like in any regular editor to separate subject line and body).|
|![commit_2](https://user-images.githubusercontent.com/57349523/155980718-cbbb2d14-89c7-4938-9e15-70253f7252e3.jpg)|![commit_1](https://user-images.githubusercontent.com/57349523/155980716-30b63626-4f73-4268-9851-cbefc6d24619.jpg)|
