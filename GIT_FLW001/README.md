###README.md

GitFlow - 001

Based on 'Git Flow Part 1 - What is Git Flow?' at https://www.youtube.com/watch?v=6LhTe8Mz6jM

More detail on 'Introducing GitFlow' at https://datasift.github.io/gitflow/IntroducingGitFlow.html

#How it works

1) We have a ***central*** repository.
 
2) Developers work ***locally*** and push their branches.

3) Two branches used to record project history are ***Master*** and ***Develop***.

4) The ***Develop*** branch serves as an integration branch for ```features```.

5) The ***Master*** branch stores the official release history.

#Creating a Feature

Jane needs to start working on a ***new feature***.

1. Jane will ```pull``` the latest copy of the ***Develop*** branch.

NOTE: If a develop branch has not already been created off the master branch, on Github one can create such a develop branch from the master branch. So, do so first.

For this example, pull https://github.com/willem-vanheemstrasystems/gitflow-sample-creating-new-feature/tree/develop

This is done in Eclipse by first cloning the above repository and adding it to the view. Switch to the Git perspective and choose the Git icon with the blue downwards facing arrow "Clone a Git Repository and add the clone to this view". 

Make sure you select ***develop*** as the branch to clone (not ***master***). 

Also if the ***develop*** branch is cloned, make sure to ```pull``` the existing clone before continuing to get the latest status. In Eclipse, you do so by choosing ```pull``` from the popup menu when right-clicking the clone of the ***develop*** branch e.g. ```gitflow-sample-creating-new-feature [develop]```.

2. Jane will then ```fork``` the cloned ***develop*** branch to create her own ```feature``` branch.

Do as follows in Eclipse; on the local ***develop*** branch, right-click and pick 'Switch To' from the popup menu, choose 'New Branch...'.

Name the new branch, e.g. '***new_feature_001***'. Keep 'source' as 'develop'. Leave 'Configure upstream for push and pull' unchecked. Check 'Checkout new branch'.










