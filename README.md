# Supplementary Material of "Bug Analysis in Jupyter Notebook Projects: An Empirical Study" paper

This repository includes all the collected and analyzed data for this study.

## Mined data
#### In the **rawdata** directory are 3 mining data from StackOverflow and GitHub.

raw_data_stack.csv: This CSV file contains all data from StackOverflow about Jupyter Posts. To extract this base, the following querie were used. 
 
```
select Id,PostTypeId,AcceptedAnswerId,ParentId,CreationDate,DeletionDate,Score,ViewCount,OwnerUserId,OwnerDisplayName,
LastEditorUserId,LastEditorDisplayName,LastEditDate,LastActivityDate,Tags,AnswerCount,CommentCount,FavoriteCount,
ClosedDate,CommunityOwnedDate,ContentLicense,Title
from Posts where Tags LIKE '%jupyter-notebook%' or Tags LIKE '%jupyter%' or Tags LIKE '%google-colaboratory%' or
Title LIKE '%jupyter-notebook%' or Title LIKE '%jupyter%' or Title LIKE '%google-colaboratory%'
```
https://data.stackexchange.com/stackoverflow/query/1541588/jupyternotebookbugs

raw_data_stack_p2.zip: This ZIP file contains the body and discussions of previous posts. To extract this base, the following query was used:

```
select Id,BodyPost,BodyAnswers,TextComments
from Posts where Tags LIKE '%jupyter-notebook%' or Tags LIKE '%jupyter%' or Tags LIKE '%google-colaboratory%' or
Title LIKE '%jupyter-notebook%' or Title LIKE '%jupyter%' or Title LIKE '%google-colaboratory%'
```

## Interviews
In the **interviews** directory, there is a file:

interview_model.pdf: This PDF file contains the questions asked in the interviews.
