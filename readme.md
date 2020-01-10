## JENKINS

This jenkins readme is located only on the 'dev' branch, we learnt how to switch between
the dev and master branch and had jenkins listen to only the dev branch and build when changes have
been committed to that branch.

TEST MERGE USING JENKINS TEST TO MERGE ON GITHUB

Interview Questions:
- how are you planning on implementing devops to your company
- what projects are you working on
- what is a typical work day like in your company?

# Merging dev and master branch.
The two branches can be merged using :
````
git add .
git commit -m
git push origin dev
git push origin dev:master
````
The above example is how we could merge a development branch we are working on
and a master branch meant for tested working code.

In the real world we never really directly work on the master branch.

````
git merge master
````
The above command will merge any changes on the master branch with the current dev
branch.

THIS IS TEST TEXT
