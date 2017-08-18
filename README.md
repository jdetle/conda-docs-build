A python wrapper for conda and conda-build to facilitate the quick building of docs.

At work we often have a team of docs writers and engineers working in the same repo.

Goals of this software:
1. Build
  - Provide a simple to use setup script to initialize config in a repo.
  - Setup can be skipped if you provide link to config
  - The config includes the conda channel being uploaded to
  - The the config inclues anaconda.org username of the person doing the upload.
  - The first time this software is used you must provide the relevant package versions it will create the build script
  - Ask for the first version number. Should use semver.
  - There should be a command to spawn a rtd server with the package youve built
  - If you are satisfied with what you see in the rtd server, upload,
  - If you aren't bump build number, build again, check docsagain
  - If satisfied, upload to channel.
  - Ask for login.

2. Deploy
  - docs-build-config.yml to determine where stuff gets built to

3. Cross-platform
  - Works equally well on any os

4. Conda installable
  - Uses click
  - Uses conda-build's api
 
