## Feedback

### Cleaning

This looks pretty good. It could be simplified a bit, but all the pieces are there (as evidenced by the very close agreement on 
the submission doc). Since you were in pandas, the biggest simplification you could have taken advantage of is the `to_gbq` which
would do the upload very easily for you. 

### Sampling

Not a [great idea](https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/) to use the `!pip install pandas-gbq -U` 
install from Jupyter Notebooks. Much more reliable to install and update from the command line. 

In this section, you do your sampling with this: 
```
"""SELECT
              *, card_no as Owner
         FROM  
             `wedge-project-peterkirgis.WedgeData2.*`
         WHERE card_no between 19800 and 20000
         ORDER BY card_no asc"""
```
There's absolutely _no_ reason to think that card numbers are random. And, in fact, they very rarely are. 
Your sample needs to be random, so revise this task. 

### DB

You don't need to submit the DB. Feel free to remove this file from your repo. For task 3, it's much more elegant
to do this with a join on the department lookup table. But everything looks good and correct and you certainly
got your `CASE WHEN` practice!

### Overall

Just redo the sampling one and slack me when you've re-push. 

