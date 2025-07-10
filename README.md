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


## Part 3: Merging Changes

After both Tom and Jerry have pushed their changes, you (or another team member) can review and merge

these change into the main project.  The process involves;

1. Creating a *Pull Request*

2. Merging the Pull Request into the *main* branch.


### Understanding Pull Requests:

A Pull Request (PR) is a feature used in GitHub (and other Git-based version control systems) that allows you to notify team members

about the changes you've pushed to a branch in a repository. Essentially, it's a request to review and pull in your contribution to the

main project. Pull requests are central to the collaborative development process, enabling team members to discuss, review, and make further

changes before changes are merged.


### How to Create a Pull Request on GitHub

After both Tom and Jerry have pushed their work to their respective branches, the next step is to create a pull request for each of them.

Here's how Tom would create a pull request for his changes.


### Navigate to Your GitHub Repository:

- Open your web browser and go to the GitHub page for the repository.

![alt text](./Pictures/gitH43.JPG) 


### Switch to the Branch:

- Click on the branch dropdown menu near the top left corner of the file list and select the branch Tom have been working on, in this case,

*update-navigation* branch.

![alt text](./Pictures/gitH44.JPG)


![alt text](./Pictures/gitH45.JPG)


### Create a New Pull Request:


- Click the "New Pull Request" button next to the branch dropdown menu.

![alt text](./Pictures/gitH46.JPG)


![alt text](./Pictures/gitH47.JPG)


![alt text](./Pictures/gitH48.JPG)


- GitHub will take you to a new page to initiate a pull request. Ite automatically selects the *main* project's branch as the base

and your recently pushed branch as the compare branch.


![alt text](./Pictures/gitH49.JPG)



### Review Tom's Changes:


- Before creating the pull request, Tom would review his changes to ensure everything is correct. GitHub shows the differences between 

the base branch and Tom's branch. It's a good opportunity for Tom to double-check his work.


![alt text](./Pictures/gitH50.JPG)


### Create the Pull Request:

- If everything looks good, click the "*Create pull request*" button. 

- Provide a title and description for the pull request. The title should be concise and descriptive, and the description should explain the 

change that the pull request is about, why it's needed, and any other relevant details.

- After filling in the information, click "*Create pull request*" again to officially open the pull request.

![alt text](./Pictures/gitH50.JPG)


![alt text](./Pictures/gitH51.JPG)


### Reviewing and Merging Tom's Pull Request:

Once the pull request is created, it becomes visible to other team members who can review the changes, leave comments, and request additional

modifications if necessary (This is an example of what collaboration is about in DevOps). When the team agrees that the changes are ready and

good to go, someone with the merge permissions can merge the pull request, incorporating the changes for Tom's *update-navigation* branch into the main branch.

![alt text](./Pictures/gitH51.JPG)

![alt text](./Pictures/gitH53.JPG)


Following the same process, Jerry would create a pull request for his *add-contact-info* branch after Tom's changes have been merged, ensuring

that the project stays up to date and conflicts are minimized.


### Updating Jerry's branch with latest changes:

Before Jerry merges his changes into the main branch, it's essential to ensure his branch is up-to-date with the main branch. This is because

other changes (like Tom's updates) might have been merged into the main branches after Jerry started working on his feature. Updating ensures

compatibility and reduces the chances of conflicts.


### Steps to Update Jerry's Branch:

- On terminal, switch to Jerry's Branch.

'git checkout add-contact-info'

![alt text](./Pictures/gitH52.JPG)


- Pull the latest from the main branch:

'git pull origin main'


![alt text](./Pictures/gitH54.JPG)


Purpose: This command fetches the changes from *main* branch (Remember, main branch now has Tom chnages) and merges them into Jerry's *add-contact-info* 

branch. It ensures that any updates made to the main branch, like Tom's merged changes, are now included in Jerry's branch. This step is crucial for avoiding

conflicts and ensuring that Jerry's work can smoothly integrate with the main project.


- Merge the pull request to the mmain branch: Click "*Merge Pull Request*" button to merge Tom's changes into the main branch. This action combines Tom's 

contributions with the rest of the project, completing the collaborative workflow.


![alt text](./Pictures/gitH51.JPG)

![alt text](./Pictures/gitH53.JPG)



### Fanilazing Jerry's Contribution:


Assuming there are no conflicts, Jerry's branch is now ready to be merged back into the main project.

- Push the Updated Branch to GitHub:


'git push origin add-contact-info'


![alt text](./Pictures/gitH58.JPG)


This commands uploads Jerry's cahnges to GitHub. Now, his branch reflects both his work and the latest updates from the main branch.

The *origin* keyword in the command refers to the default name Git gives to the remote repository from which you cloned your project.

It's like a shortcut or an alias for the full URL of the repository in GitHub.


### Create the Pull Request:

- Click the "New Pull Request" button next to the branch dropdown menu.


![alt text](./Pictures/gitH46.JPG)


![alt text](./Pictures/gitH55.JPG)


![alt text](./Pictures/gitH56.JPG)

- If everything looks good, click the "*Create pull request*" button. 


### Review Jerry's Changes:


- Before creating the pull request, Jerry would review his changes to ensure everything is correct. GitHub shows the differences between 

the base branch and Jerry's branch. It's a good opportunity for Jerry to double-check his work.


![alt text](./Pictures/gitH56.JPG)


- Provide a title and description for the pull request. The title should be concise and descriptive, and the description should explain the 

change that the pull request is about, why it's needed, and any other relevant details.

- After filling in the information, click "*Create pull request*" again to officially open the pull request.

![alt text](./Pictures/gitH57.JPG)


![alt text](./Pictures/gitH59.JPG)



- GitHub will take you to a new page to initiate a pull request. It automatically selects the *main* project's branch as the base

and your recently pushed branch as the compare branch.




### Reviewing and Merging Jerry's Pull Request:


- Once the pull request is created, it becomes visible to other team members who can review the changes, leave comments, and request additional

When the team agrees that the changes are ready and good to go, someone with the merge permissions can merge the pull request, incorporating the changes for Jerry's *add-contact-info* branch into the main branch.


- Merge the pull request to the mmain branch: Click "*Merge Pull Request*" button to merge Jerry's changes into the main branch. This action combines Jerry's contributions with the rest of the project, completing the collaborative workflow.


![alt text](./Pictures/gitH60.JPG)


![alt text](./Pictures/gitH61.JPG)


This simulated workflow illustrates how Git facilitates collaborative development, allowing multiple developers to work simultaneously on different aspects of a project and merge their contributons seamlessly, even when working on the same files. 






<<<<<<< HEAD


=======
>>>>>>> cb8cf4e56b48765d02c4ead0cc435cd1dc6b042f
