# Supplementary Material of "Bug Analysis in Jupyter Notebook Projects: An Empirical Study" paper

This repository includes all the collected and analyzed data for this study.

## Mined data
#### -In the "rawdata" directory are all the mining data from StackOverflow and GitHub. -

To extract the StackOverflow base, the following queries were used and the results are in the raw_data_stack.csv and raw_data_stack_p2.zip files.
 
```
select Id,PostTypeId,AcceptedAnswerId,ParentId,CreationDate,DeletionDate,Score,ViewCount,OwnerUserId,OwnerDisplayName,
LastEditorUserId,LastEditorDisplayName,LastEditDate,LastActivityDate,Tags,AnswerCount,CommentCount,FavoriteCount,
ClosedDate,CommunityOwnedDate,ContentLicense,Title
from Posts where Tags LIKE '%jupyter-notebook%' or Tags LIKE '%jupyter%' or Tags LIKE '%google-colaboratory%' or
Title LIKE '%jupyter-notebook%' or Title LIKE '%jupyter%' or Title LIKE '%google-colaboratory%'
```
https://data.stackexchange.com/stackoverflow/query/1541588/jupyternotebookbugs

```
select Id,BodyPost,BodyAnswers,TextComments
from Posts where Tags LIKE '%jupyter-notebook%' or Tags LIKE '%jupyter%' or Tags LIKE '%google-colaboratory%' or
Title LIKE '%jupyter-notebook%' or Title LIKE '%jupyter%' or Title LIKE '%google-colaboratory%'
```

