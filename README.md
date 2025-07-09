# Hands-On Git Project: Collaborative Website Development with Git and GitHub

In this mini-project, we'll create a step-by-step project to stimulate the workflow of Tom and Jerry using Git and GitHub. This hands-on project will include 
installation of Git, setting up a GitHub repository, cloning the repository, creating branches, making changes, and merging those changes back into the main branch.


## Part 1: Setup and Initial Configuration

### Install Git:

- Visit the official Git Website (https://git-scm.com/downloads) and download the latest version of Git suitable for your operating system.


![alt text](./Pictures/gitH.JPG)


- Follow the instructions to install git.

![alt text](./Pictures/gitH1.JPG)

![alt text](./Pictures/gitH2.JPG)


### Create a GitHub Repository:

- Sign up or login to GitHub.

![alt text](./Pictures/gitH3.JPG)


- Click the "+" icon in the top-right corner and select "New Repository"


![alt text](./Pictures/gitH4.JPG)


![alt text](./Pictures/gitH5.JPG)


![alt text](./Pictures/gitH6.JPG)


- Name your repository "ai-startup-website" and initialize it with a README file.


![alt text](./Pictures/gitH7.JPG)


- Click "Create Repository" 


![alt text](./Pictures/gitH8.JPG)



### Clone the Repository


- On your repository's page on GitHub, click the "Code" button and copy the HTTPS URL.


![alt text](./Pictures/gitH9.JPG)


![alt text](./Pictures/gitH10.JPG)


- Open your terminal or command prompt.


![alt text](./Pictures/gitH11.JPG)

- Create a folder named "git-project"

'mkdir git-project

![alt text](./Pictures/gitH12.JPG)

- Change directory into "git-project".

'cd git-project'

![alt text](./Pictures/gitH13.JPG)

- Clone (Download) the repository from GitHub using

'git clone https://github.com/bruyo/ai-startup-website.git'


![alt text](./Pictures/gitH14.JPG)

- Since you have just clonned your repository, your branch is "main"

- Navigate into the repository you clonned.

'cd ai-startup-website'

![alt text](./Pictures/gitH15.JPG)


- Create an empty file "index.html"

'touch index.html'

![alt text](./Pictures/gitH16.JPG)

- Add the content below 

" This is the Admin creating an index.html file for Tom and Jerry."

'vim index.html'


![alt text](./Pictures/gitH18.JPG)


![alt text](./Pictures/gitH17.JPG)


- Check changes has not been staged.

'git status'

![alt text](./Pictures/gitH19.JPG)

- Stage changes.

'git add index.html'

![alt text](./Pictures/gitH20.JPG)

- Confirm changes have been staged for commit.

'git status'

![alt text](./Pictures/gitH21.JPG)


- Commit changes

'git commit -m "This is my first commit"'

![alt text](./Pictures/gitH22.JPG)


- Push main branch to GitHub

'git push origin main'

![alt text](./Pictures/gitH23.JPG)


## Part 2: Simmulating Tom and Jerry's Work

To simulate both Tom and Jerry working on the same laptop, you'll switch between two branches, making changes as each character.

### Tom Work:

- Navigate to the project dirctory you just cloned:

'cd ai-startup-website'

![alt text](./Pictures/gitH24.JPG)


- Check the current branch.

'git branch'


![alt text](./Pictures/gitH25.JPG)

- Create a new branch for Tom's work.

'git checkout -b update-navigation'


![alt text](./Pictures/gitH26.JPG)


- Check the branch again to see your newly created branch.

'git branch'


![alt text](./Pictures/gitH27.JPG)

- Recall you created an empty file "index.html" in the main branch. The file also exist in the "*update-navigation-branch*": Open the 'index.html' and add the content below.

'vim index.html'

![alt text](./Pictures/gitH28.JPG)


'This is Tom adding Navigation to the AI-website'

![alt text](./Pictures/gitH29.JPG)


- Check changes has not been staged.

'git status'


![alt text](./Pictures/gitH30.JPG)

At this stage, Tom has modified the file, but these changes haven't been prepared for a commit in Git. This is indicated by the file name appearing in *red* in the terminal output, signaling that the changes 
are not recognized by Git but not yet staged.

- Stage Tom changes.

'git add index.html'


![alt text](./Pictures/gitH31.JPG)


- Confirm changes have been staged for commit.

'git status'

![alt text](./Pictures/gitH32.JPG)

Now, after staging the changes, the file name will appear in *green* in the terminal output. This color signifies that the file has been successfully staged, making it
ready for the next step, which is committing these changes to the project history.


- Commit Tom changes

'git commit -m "Update navigation bar"'

![alt text](./Pictures/gitH33.JPG)


- Push Tom's branch to GitHub.

'git push origin update-navigation'


![alt text](./Pictures/gitH34.JPG)


After completing Tom's workflow, you will now simulate Jerry's contribution tho the project. To do this, you'll take the following steps;


- Switch back to main branch 

'git switch main'

'git checkout main'


![alt text](./Pictures/gitH35.JPG)


- Pull the latest changes.

'git pull origin update-navigation'


![alt text](./Pictures/gitH36.JPG)


- Create a new branch for Jerry' Work.

'git checkout -b add-contact-info'

![alt text](./Pictures/gitH37.JPG)


- Open *index.html* and Add Contact Information: Make your changes to the *index.html* file by adding contact information. 

'vim index.html'

![alt text](./Pictures/gitH38.JPG)

![alt text](./Pictures/gitH39.JPG)


- Stage Jerry changes.

'git add index.html'

![alt text](./Pictures/gitH40.JPG)


Commit Jerry changes

'git commit -m "Add contact information"'

![alt text](./Pictures/gitH41.JPG)


- Push Tom's branch to GitHub.

'git push origin add-contact-info'


![alt text](./Pictures/gitH42.JPG) 
