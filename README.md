# Welcome to "regular_programs" repository


## This repository contains the 2023B nightly observing plans for DECam observations. 

----
# Instructions for observations

**This repository must be updated in the local machine of the observing room before starting the night. Do it with the following steps:**

1. Open a Terminal and go to the repository directory located in ~/regular_programs
   ```cd ~/regular_programs```

   (**Note: ONLY If the repository is not in the machine or if you made a mistake and need to download it again**, delete the ```~/regular_programs``` directory, and then:
   ```
   cd ~
   git clone https://github.com/gdamke/regular_programs.git
   ```
   this will clone the updated repository in ```~/regular_programs``` again and you don't need to do anything else.)

2. Check that you are in the repository directory with:
   
   ```
   git status
   ```

   The output should contain a message saying ```On branch main```. **Beware that the message also may say that ```Your branch is up to date with 'origin/main'.```, but your local branch may be outdated anyway!** 

3. Next, fetch the latest changes:
   ```
   git fetch
   ```

4. Now you can check if there are changes in the Github repository that need to be sync-ed. Do it with:
   ```
   git status
   ``` 

   If the output says ```Your branch is behind 'origin/main' by N commits``` then do the step 5.


5. Finally *pull* the changes from Github to update your local copy with:
   ```
   git pull
   ```
   The output should say ```Your branch is up to date with 'origin/main'.```

  **and that's it!**

---

**Alternatively, if the steps above seem complicated, you can download the whole repository in ZIP format from Github by clicking on gree *Code* button and then *Download ZIP*. Then, extract the file somewhere.**


----


# Instructions for editing the repository

*These instructions are directed only to the people preparing the observing plan for the night.*

***Before any editing, you MUST have "editor" status in the Github repository***


0. **Only do this step the first time** --- Clone the repository into your local machine.

   Open a Terminal and go to the directory where you will clone the repository.
   For example, if you do this in your home directory (```~/```), then the repository will become ```~/regular_programs``` after clonning.

   ```
   git clone https://github.com/gdamke/regular_programs.git
   ```

1. Go to the repo dir ```cd repository/path/here``` and check that you are in the repository directory with ```git status```:
   
   ```
   git status
   ```
   
   The output should contain a message saying ```On branch main```. **Beware that the message also may say that ```Your branch is up to date with 'origin/main'.```, but your local branch may be outdated anyway!**
   
2. Check if your local repository is updated with respect to the Github repo:

   ```
   git fetch
   ```
   
   
3. Pull (update from Github) the changes (if any found in step 2) in your local repository:

   ```
   git pull
   ```


4. Make all the changes in your local copy. At minimum, the plan must contain:
   - a directory with name formatted as ```yyyymmdd``` (for example, 20230823/)
   - a text file (within the night directory) containing:
     - the night ephemeris (copy and paste from `ephem` command in Kentools.
     - the propids, observer and support for the first- and second-half of the night (copy and paste from Kathy's Google calendar).
     - the plan for the first half (copy it from `templates/` directory -> this is work in progress, so copy it from a previous night observing the same program)
     - the hour of the night midpoint
     - the plan for the second half (copy it from `templates/` directory -> this is work in progress, so copy it from a previous night observing the same program)
   - add the required .json files for each half of the night. Create a separate directory using the respective `propid/` as the directory name.
   
   Note: for DECAT, we only copy the instructions to the nightplan file from the template (in progress, so use a previous night) with instructions to update the separate `DECAT_pointings/` repository.


6. *Add* all the new and updated files to the local repository.
   -> you can list the files that will be changed with ```git status```. Next, you can add them one-by-one, or add ***all files*** with:

   ```
   git add *
   ```
   
7. *Commit* the file *to your local repository*. It is good practice to add a *message* to the commit that summarizes the commit. For example "Add night plan for 20230823"

   ```
   git commit -m"Write a summary message in this line"
   ```

   
8. Finally, *push* the commits into the Github repository with:

   ```
   git push
   ```
   
  **and that's it!**


Note 1: if you need to delete a file that was included to the repository, use the command `git rm <filename>`

Note 2: if you need to rename a file, use the move command `git mv <current_filename> <new_filename>`
