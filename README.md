# ue4-gitlfs-baseproject

Base files to start using Git LFS with UE4.

## Instructions

1. Create your project repo. If you want some free and private repos with [LFS support](https://docs.microsoft.com/en-us/azure/devops/repos/git/manage-large-files?view=azure-devops) you can try [Azure Repos](https://azure.microsoft.com/en-us/services/devops/repos/).

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

* To see the list of files being tracked by git-lfs, run: 

  ```
  git lfs ls-files
  ```

* More info: https://github.com/git-lfs/git-lfs/wiki/Tutorial

## Base projects

* git attributes configuration based on: https://github.com/MOZGIII/ue4-gitignore

* git ignore based on: https://github.com/github/gitignore/blob/master/UnrealEngine.gitignore