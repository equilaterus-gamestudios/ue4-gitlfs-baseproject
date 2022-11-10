# UE4 GitLFS Baseproject

> Please check this project! https://github.com/ProjectBorealis/UEGitPlugin. 

Alternatives:
* Again: https://github.com/ProjectBorealis/UEGitPlugin
* [PlasticSCM](https://www.plasticscm.com/) (includes free plan).
* [Helix Perforce](https://www.perforce.com/products/helix-core).

Base files to start using Git LFS with UE4.

## Instructions

1. Create your project repo. *If you want some free repos, read the final section of this README*.

2. Install git lfs.

   ```
   git lfs install
   ```

3. Copy .gitattributes and .gitignore files to the root path of your repo.

4. Create/copy an UE4 project to the root path of your repo.

5. You're done!

## Project structure

We recommend you to add UE4 files to the **/Content** folder (as you always do) and RAW files (before importing them to UE4) into the folder **/RawContent**.

## Git LFS Commands

* After *staging* files to your Git Repo (using the ADD command) you can review which files are going to be uploaded to the Git LFS server suing this command:

  ```
  git lfs status
  ```

* To list files being tracked by git-lfs, run: 

  ```
  git lfs ls-files
  ```
  
* To list files not being tracked by git-lfs (after commit), run on *git bash*:

  ```
  { git ls-files && git lfs ls-files | cut -d' ' -f3-; } | sort | uniq -u
  ```

* More info about [git lfs](https://github.com/git-lfs/git-lfs/wiki/Tutorial)

* More info about [listing files not tracked by git lfs](https://stackoverflow.com/questions/42963854/list-files-not-tracked-by-git-lfs)

## Base projects

* git attributes configuration based on: https://github.com/MOZGIII/ue4-gitignore

* git ignore based on: https://github.com/github/gitignore/blob/master/UnrealEngine.gitignore

## Repos with Free LFS

* Github and Gitlab support LFS but not for free.

* If you want some free and private repos with [LFS support](https://docs.microsoft.com/en-us/azure/devops/repos/git/manage-large-files?view=azure-devops) you can try [Azure Repos](https://azure.microsoft.com/en-us/services/devops/repos/). 

  * **Note 1:** As 2021, locks do not work as expected on Azure Repos with UE4.
  
  * **Note 2:** To avoid errors with Azure LFS, use this command on your repository directory: 
    ```
    git config http.version HTTP/1.1
    ```` 
