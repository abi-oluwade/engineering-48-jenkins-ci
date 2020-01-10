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

NEW TEST FOR CI & CD
AFTER ADDING SECURITY GROUP AND MAKING CI AND CD PIPELINE

# Task
We want to be know how to launch an AWS instance, and then with that instance be able to install our Sparta nodejs app as well as
the mongodb, run a provision script to install the libraries and dependencies on that AMW instance, replace the default sites-enabled nginx with the nginx.default that we modified ,and then be able to launch the app so that it can be navigated to though the public ip.

This means we have to know commands below such as the scp command which can copy local folders and files to our AWS instance, which computers are located elsewhere.

- Port 22 is the SSH connection.

- ./<script or file name> runs the file

- scp -i ~/.ssh/Abiodun-Oluwade-Eng48-first-key.pem -r environment/ ubuntu@34.255.198.62:/home/ubuntu/ (command to copy entire folders to another machine, in this example copy environment to my AWS machine)

- scp -i ~/.ssh/Abiodun-Oluwade-Eng48-first-key.pem app/provision.sh ubuntu@34.255.198.62:/home/ubuntu/provision_file.sh (command to copy a single file folder)

StrictHostKeyChecking='no' 'Makes it skip the asking of adding a computer to the known host'

WHAT happens:
The github for our repo is linked to jenkins, and we have confiugured jenkins so that whnever there is a change in code pushed to github, jenkins will be notified and if
the code passes the test will update our github which in turn will update our workspace. this means any changes produced will be pushed to aws through our jenkins shell and essentially means we can automate our deployments to server:
1.Produce changes on github and test on jenkins
2.changes applied to jenkins workspace
3. worspace code pushed to aws server
