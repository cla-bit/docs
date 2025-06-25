# VerdictVision

----

## Pushing Large Files to GITHUB

-----

1. Download and Install `GIT LFS`. See download link here [Download GIT LFS](https://git-lfs.com/)
2. Set up Git LFS for your user account by running (best to do this inside the github repository):

   ```bash
   git lfs install  # You only need to run this once per user account.
   ```
3. Pick the file (large file) you want to push to github and track it. In this case, I have a file `encoders.safetensors` (400MB+)
   inside a `models/` directory.

   ```bash
   git lfs track "models/*.safetensors"  # to track all the .safetensors files
   ```
   
   or
   
   ```bash
   git lfs track "models/encoders.safetensors"  # to track all the .specific file
   ```

5. Now make sure .gitattributes is tracked:

   ```bash
   git add .gitattributes
   ```
   Take note that every file tracked, run this command.
6. Run the `git add .`
7. Run the commit command `git commit -m 'your commit message here'`
8. Push to github repository `git push origin <name of branch>`
