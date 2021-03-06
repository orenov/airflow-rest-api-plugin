# Airflow REST API Plugin Release Procedure

This document describes the branching procedure and how to create new releases of the project.
 
### Release Instructions

1. (if not already done) Create a new branch for all the changes you want in the release
    * Branch naming convention: v{VERSION}-branch
        * Example: v1.0.0-branch
2. Push all your changes into the Branch
    * For Pull Requests from External Contributors, those changes will also go into the Release Branch and not the Master
3. Create a Pull Request to merge the changes from the Branch into Master
4. Admin: Review the changes and approve the Pull Request 
    * This will merge the changes into Master
5. Create a Release from Master
    * Version Tag naming convention: v{VERSION}
        * Example: v1.0.0
    * Release Title: Same as Version Tag Name
    * Add a description
        * Should describe the new features, bug fixes and other updates
6. Create a new Branch from Master for the next release
    * Same as described in #1
7. In the new release, update the following things:
    * Within README.md
        * Add the future new release to the "Releases Available" section
        * Add the current branch that was created to the "Branches Available" section 
    * Within plugins/rest_api_plugin.py
        * Update the \_\_version\_\_ value to the new release you're creating
