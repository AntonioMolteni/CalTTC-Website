# CalTTC-Website
![Telnyx](img/banner-logo/banner-logo.png)

## Website Directions: How to get Started

1. [Clone](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) the old website repository from github to your machine: https://github.com/CalTTC/CalTTCwebpage. (I recommend cloning the repository to your desktop.)
as well as the new website repository: https://github.com/AntonioMolteni/CalTTC-Website
2. Download Visual Studio Code (VS Code) and get the extensions called “Live Server” and “HTML CSS Support”. Importantly, __RESTART__ VS Code afterwards.
3. Locate a folder called “_site” in the old repository you cloned and open this in VS Code. This is the old website folder.  The new website folder is just the repository you already cloned: "CalTTC-Website" (to your Desktop).
4. Inside VS Code, select File > Open Folder and locate either "_site"(old) or "CalTTC-Website"(new). Once either of these files is open in VS Code, you can open the main file titled "index.html".  This is basically the home page. Right click anywhere on the page and select the option “Open with Live Server”.  This should open a new tab in your browser with a locally hosted preview of the website. 
5. Make sure it looks something like the actual website (it should not just be plain text): https://calttc.berkeley.edu.  If it is in plain text you may be in the incorrect index.html file on the old website (it should be in the _site folder). You may need to refresh your browser tab or save the file in VS Code (if you have made edits).
6. Now you are ready to start messing around with the source code. I have included many notes and links in the actual code itself.  Bootstrap is the system we are using to develop the frontend(the part that the user sees)on both mobile and desktop for responsive web design(design changes based on window size and device type).  I would recommend reading up on this in the links below.

Currently, the old website source code from github has a lot of unnecessary baggage.  In order to remove this baggage, I have just created a new website with zero clutter from the start.  This being said, please do not be intimidated by the code.  The only code that is actually important will be in the .html files and css files inside the root of the repository.  Since I have written the template for the new website, message me (Antonio Molteni) if you need an explanation of anything.

The old website is based off of a template called Airspace by Themefisher.  You may want to you download it by going to https://themefisher.com/products/airspace.  To view this theme in VS Code open the folder titled “airspace-premium” after extracting the contents of the “airspace.zip” file.  Although we are not using this template anymore because it is outdated and far too overcomplicated for our purposes, you can just tool around to see the basic structure. 

If you are having trouble getting started with HTML.  I would watch the first few videos from this playlist:    
[Basic HTML Tutorial] (https://www.youtube.com/watch?v=gQojMIhELvM&list=PLoYCgNOIyGAB_8_iq1cL8MVeun7cB6eNc)    
If you are having trouble understanding bootstrap I would recommend looking at these links:  
* [Reference Guide](https://www.w3schools.com/bootstrap4/bootstrap_ref_all_classes.asp)      
* [Grid System](https://www.w3schools.com/bootstrap4/bootstrap_grid_system.asp)    
* [Navigation Bar](https://www.w3schools.com/bootstrap4/bootstrap_navbar.asp)    
* [5 min Intro](https://www.youtube.com/watch?v=yalxT0PEx8c)    
* [1hour 30min Tutorial](https://www.youtube.com/watch?v=9cKsq14Kfsw)  


## Collaborator Push Protocol:

It is important to push to the repository properly to avoid merge conflicts.

1. If you already have a copy of the repo on your local machine, skip to step 2. If you haven't already, [clone](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) the new website repository to your computer.
2. Using your terminal, [cd and ls](https://tutorials.codebar.io/command-line/introduction/tutorial.html) into the new website repository: `cd CalTTC-Website`
3. Before you start changing code, always make sure that you have the latest github remote repository by using `git pull`.
* If you forgot this step, no big deal, as long as you are not simultaneously editting the same code as another collaborator there will be no issue if you plan to merge this code back into the main branch.
4. Now we will create a new branch using either:
* the `git checkout -b [yourbranchname]`.
* or the more complex `git branch [yourbranchname]` command and `git checkout -b [yourbranchname]`
You are now in a new branch.  You can go back to the main branch by running `git checkout main` or `git checkout master`.
5. Now you can go into VS Code and start working on your new branch. 
6. _(Optional)_ After you have made your changes, you can run the `git status` terminal command in your local repository to see the files you have changed.
7. Now you need to stage the files you modified for commit or in other words _add_ the files to be commited. You can stage or _add files two ways:
* stage individual files by doing `git add [yourfilename]`.    
* stage all of the files you changed by doing `git add .` or `git add -A`.    
8. Now that all of your changed files are staged, we can commit (basically saves the changes that you have made).  This allows us to restore this _commit_ later if we wish to.  Come up with a commit message that is relatively short and describes the changes that you have made.  Commit by running `git commit -m "[yourcommitmessage]"`. 
9. After the changes are committed, we can upload our local repository to the remote github repository.  This can be done using `git push`.
* You must be a __Collaborator__ on the CalTTC github page to do this step.  
* There is a possibility that you may have to do `git push --set-upstream origin [yourbranchname]` if it is your first time pushing.
10. Now your terminal will give you some instructions to do a pull request on `https://github.com/CalTableTennis/CalTTC-Website/pull/new/[yourbranchname]`.    
Once on the [CalTTC-Website Github Page](https://github.com/CalTableTennis/CalTTC-Website), you will see a green button that says __compare & pull request__.  Click this.
11. Write a brief description of the changes you made in the __write__ tab so that other collaborators know what you did.
12. Wait until someone else leaves a comment approving the change and the __approve__ your pull request.  If required make the changes others require. 
13. Once there is approval you can merge the branch using the __merge__ function or the __squash and merge__ function if you want to delete the branch afterward. 