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

1) Jane will ```pull``` the latest copy of the ***Develop*** branch.

NOTE: If a develop branch has not already been created off the master branch, on Github one can create such a develop branch from the master branch. So, do so first.

Have a look at the Graph section on GitHub which will show all branches for this repository under 'Network'. https://github.com/willem-vanheemstrasystems/gitflow-sample-creating-new-feature/network

For this example, pull https://github.com/willem-vanheemstrasystems/gitflow-sample-creating-new-feature/tree/develop

This is done in Eclipse by first cloning the above repository and adding it to the view. Switch to the Git perspective and choose the Git icon with the blue downwards facing arrow "Clone a Git Repository and add the clone to this view". 

Make sure you select ***develop*** as the branch to clone (not ***master***). 

Also if the ***develop*** branch is cloned, make sure to ```pull``` the existing clone before continuing to get the latest status. In Eclipse, you do so by choosing ```pull``` from the popup menu when right-clicking the clone of the ***develop*** branch e.g. ```gitflow-sample-creating-new-feature [develop]```.

2) Jane will then ```fork``` the cloned ***develop*** branch to create her own ```feature``` branch.

Do as follows in Eclipse; on the local ***develop*** branch, right-click and pick 'Switch To' from the popup menu, choose 'New Branch...'.

Name the new branch, e.g. '***new_feature_001***'. Keep 'source' as 'develop'. Leave 'Configure upstream for push and pull' unchecked. Check 'Checkout new branch'.

In the Project Explorer, the project 'GIT_FLW001_NW_FEAT' will now have switched to the 'new_feature_001' branch, ready to start coding the new feature code.

As a test, create a new javascript file inside the GIT_FLW001_NW_FEAT project, e.g. 'New_Feature_Code.js'. 

As content of this file use:

```javascript
var someNewFeatureCodeHere = 'test';
```

3) Jane will commit her work to this ***new feature*** branch.

In Eclipse, right-click on the Project GIT_FLW001_NW_FEAT and choose from the pop-up menu 'Team' -> 'Commit...'. Stage the file 'New_Feature_Code.js' and click 'Commit' after making sure the branch is pointing at 'new_feature_001'.

The changes have now been committed to the 'new_feature_001' branch, not the 'develop' branch yet.

***NOTE***: In order to switch between 'features' to work on, as long as you commit your changes to the specific 'feature branch' you can jump from working on one feature to working on another feature (switching branch in the Git Repository view in Eclipse).

4) When Jane has completed and tested her code, she will merge her 'new_feature_001' branch into 'develop'.

In Eclipse, first 'pull' the 'develop' branch of 'gitflow-sample-creating-new-feature'. To do so, in the Git Repositories view choose the 'gitflow-sample-creating-new-feature [new_feature_001]' and right-click on it.

From the popup menu choose 'Switch to' and choose the 'develop' branch. Then on the 'develop' branch choose 'pull'.

***NOTE***: If Jane is not authorised to merge her 'feature' branch into the 'develop' branch, she can issue a '***pull request***' instead. This alerts someone who is authorized to merge into the develop branch to do so (after having reviewed and tested the new feature code).

Once the 'develop' branch has been pulled, and thus contains the latest changes, on the 'GIT_FLW001_NW_FEAT' project, right-click and choose 'Merge...'. From the Merge menu, choose to merge the 'new_feature_001' branch into the 'develop' branch. Click 'Merge'

The 'develop' branch will show an upwards pointing arrow, indicating that changes have been committed to this branch (i.e. our new feature) and thus a push should be conducted.

Go ahead and choose 'Push branch develop'. Confirm all dialogue windows. The upwards pointing arrow will have disappeared and when viewed on GitHub, the new feature code should be present in the code base for the 'develop' branch. 

Click on the 'commits' on the Github page for the 'develop' branch. Some of the commits will be those of the new feature. They are now part of the 'develop' branch.   


...