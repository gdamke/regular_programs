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

# Instructions for editing the repository (TBD)
