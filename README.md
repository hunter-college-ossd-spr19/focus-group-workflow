# Instructions for This GitHub Workflow Activity 

##  1. Form teams

Form teams of two to three people (not more)


Rank the team members based on their experience with git/GitHub:

 - 1 - least experienced, maybe not even knowing git and just basic in GitHub
 - 2 - some experience, knowing basic git commands and reading GitHub pages
 - 3 - confident user, having worked in git and created repositories on GitHub

Ensure that each team member ...

    - [ ] Has git installed on their laptop.
    - [ ] Is logged into their GitHub account on their computer.


## 2. Create a team repository

__Assumptions__

* Each team member is signed into GitHub.
* There is an organization to which each team member has access.
* Each team member is viewing that organization on GitHub.

__On GitHub__

Assign the role of __maintainer__ to one of the group members: this should be the a person with some git experience, i.e., someone with ranking of 2 or 3 above.
Assign  the role of __contributor__ to the other members of the team.

1. Click the __Repository__ tab to view the repositories of the course organization.
1. Click the big green __Create a new repository__ button. (If you already have a repository in this organization, click the green __New__ button.)
2. Name the repository `TEAM_NAME-workflow` (where TEAM_NAME is replaced with the team's chosen name).
3. Optionally add a description.
4. Make it public.
5. Initialize it with a README.
6. Optionally add a .gitignore (not necessary for this activity).
7. Add an open source license (unless you have a strong opinion, for now choose __GNU Public License v3.0__).
8. Click the big green __Create repository__ button

Congratulations! You have created your team's first repository.

__Report__

In the README file that you created in this repository, write the GitHub names of the team
members and which roles they have. Also write whether there
were any problems in performing these steps, whether there was any ambiguity,
and how long it took to complete them.


__Check in with the activity leader (the instructor) before continuing.__



## 3. Prepare to contribute to a Project

One and only one contributor performs the following steps.

### Fork the upstream repository

1. Click __Fork__ in the upper-right corner.
2. If you are a member of one or more organizations, select your personal account to receive the fork.
3. You should be viewing your personal fork of the team's repository on GitHub.

Congratulations, you have forked a personal copy of the team's repository!

### Clone your fork

__Assumptions__

* You have git installed and configured on your machine.
* You are viewing your personal fork of the team's repository on GitHub.
* Your team's repository is named `TEAM_NAME-workflow` where `TEAM_NAME` is the team's chosen name.

__Instructions__

1. In the browser, click the green __Clone or Download__ button.
2. If "HTTPS" is not selected, click __Use HTTPS__.
3. Click the clipboard icon to copy the URL in the box to your clipboard.
4. To clone the repository, in the terminal, enter the git command below, where URL is in your clipboard from step 3.
    ```
    git clone URL
    ```
5. Change directory into the root of your cloned repository:
    ```
    cd TEAM_NAME-workflow
    ```

Congratulations, you have cloned your fork to your local machine!

### Add an upstream remote

To add a remote, you need the URL of the remote repository. The following steps are one way to get that URL.

1. In the browser, navigate to your team's repository (not the fork's.)
2. Click the green __Clone or Download__ button.
3. If "HTTPS" is not selected, click __Use HTTPS__.
4. Click the clipboard icon to copy the URL in the box to your clipboard.
5. In the terminal add a named URL (called a remote) to your clone that points to the team's repository, which we'll call `upstream` (the name can be anything you wish, but the remaining instructions
assume it is named `upstream`).
    ```
    git remote add upstream URL
    ```
6. Run the following command and confirm that your local repository  has two remotes (but four lines): `origin`, which points to your fork of the team's repository, and `upstream`, which points to your team's repository.
    ```
    git remote -v
    ```
    You should see something like this (with YOUR_ACCOUNT and TEAM_ORGANIZATION replaced by actual values).
    ```
    $ git remote -v
    origin    https://github.com/YOUR_ACCOUNT/TEAM_NAME-workflow.git (fetch)
    origin    https://github.com/YOUR_ACCOUNT/TEAM_NAME-workflow.git (push)
    upstream  https://github.com/CLASS_ORGANIZATION/TEAM_NAME-workflow.git (fetch)
    upstream  https://github.com/CLASS_ORGANIZATION/TEAM_NAME-workflow.git (push)
    ```
Congratulations, your local clone now knows where to find the upstream repository (i.e., your team's repository).



__Report__

In the README file in the team's upstream repository, write what 
you learned when completing the above steps and/or a description of
problems you encountered. The maintainer must write this since the maintainer may be the only one
with write access to the repository.

__Check in with the activity leader (the instructor) before continuing.__



## 4. Everybody prepares to contribute to the project

The other team members now perform the steps in Section 3 to setup their own forks and clones on their local machines.
If it is a two-person team, then this is just the maintainer, otherwise the maintainer and the other contributor
do this together,  _in parallel_.

__Check in with the activity leader (the instructor) before continuing.__


## 5. Create issues to correct

On GitHub, the issue tracker is used to keep track of bugs (problems that need fixing), feature requests,
suggestions and sometimes clarification questions from people using the project.

Your team should create three issues in this step. Divide the issues so that each team member
creates at least one of the issues.

1. Navigate to your team's repository on GitHub (_not_ your fork).
2. Click the __Issues__ tab.
3. Click the big green __New issue__ button.
4. Enter the title and a description of this issue.
    The issues created in this step will be that there are missing files that must contain
    some specific information about the team. Each issue should state the name of the missing file
    and describe its content in enough detail so that someone wishign to fix it will be able to do so
    without needing to ask for clarification from the project's community.
      - `programming_languages.txt` - should be a list of the programming languages that each team member
         knows well enough to program in.
      - `dream_jobs.txt` - should contain, for each team member, a description of dream job that the team member
         would like to get after graduation.        
      - `favorite_food_joints.txt` - should contain a list of the team members' favorite food places near or in
        the college.
     

__Report__

In the README file in the team's upstream repository, write what
you learned when completing the above steps and/or a description of
problems you encountered.

__Check in with the activity leader (the instructor) before continuing.__


## 6. Contribute to the project


1. Your team's goal is to have a _contributor_ fix one of the existing issues. __It should be the issue about
programming languages.__ <br>
    Follow the __[Contribution Workflow](contribution-workflow.md)__ to accomplish this goal.
    <br><br>
    __Report__<br>
    In the README file in this repository write what
    you learned when completing the above steps and/or a description of
    problems you encountered.
    <br>


__Check in with the activity leader (the instructor) before continuing.__

Before you start this step, change the settings on the team's repository so that the
team members each have `write` access to the repository:

1. Navigate to your team's repository on GitHub (_not_ your fork).
2. Click the __Settings__ button.
3. Click __Member Privileges__ in the list on the left-hand side of the page.
4. Under __Base Privileges__, make sure that the base privilege is `write` rather than `read`.

Once you have done this you may continue with the following steps.


2. This time, everyone is a _contributor_ and a _maintainer_. However, you
cannot serve as a _maintainer_ for you own PR.  Follow the  __[Contribution Workflow](contribution-workflow.md)__  in parallel to accomplish the following:
      - fix the remaining two issues (in groups of three, the person who already fixed an issue should work along
        side the other two members)
      - the people acting as maintainers should not accept these pull requests right away - they should request some
        revisions (e.g., no chain stores like Starbucks are allowed in the favorite food places list)
      - (after the above issues are fixed) report a couple of new issues (this should be done by the least 
        experienced git user):
                - all three files should be in alphabetical order
                - all three files should contain the names of the team members next to their entries


    __Report__

    In the README file in the team's (upstream) repository write what 
    you learned when completing the above steps and/or a description of
    problems you encountered.

__Check in with the activity leader (the instructor) before continuing.__



3. Again, everyone plays the roles of a _contributor_ and a _maintainer_, but never serves as a _maintainer_ for their own PR.
    <br>
     Fix the two latest issues in parallel (done by the least experienced users in the groups of three). 
     The submission of   pull requests for these two issues should result in a merge conflict 
     (since both issues require you to modify the same files).
    Follow the __[Contribution Workflow](contribution-workflow.md)__ to accomplish this goal.
    <br><br>
    __Report__
    <br>
    In the README file in this repository write what
    you learned when completing the above steps and/or description of
    problems you encountered.
    <br>
    __Check in with the activity leader (the instructor) before continuing.__
