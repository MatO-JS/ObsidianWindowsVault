## Summary

```bash

git init

git add .

git status

git commit -m "Initial commit"

git remote add origin https://github.com/your-username/your-repository.git

git push -u origin master

// To clone the repository

git clone https://github.com/your-username/your-repository.git

```
Teach me how to upload my code to git and also how to clone a git repository?

**Uploading Code to Git**

1. **Install Git**: If you haven't already, you'll need to install Git on your machine. You can download it from the official Git website ([https://git-scm.com/downloads](https://git-scm.com/downloads)).
2. **Create a Git Repository**: Open a terminal or command prompt and navigate to the directory where your code is located. Then, run the following command to initialize a new Git repository:
    

- `git init`
    
- **Add Your Files**: Use the following command to add your files to the Git repository:
    
- `git add .`
    
    This will add all the files in the current directory to the staging area.
- **Commit Your Changes**: Next, you'll want to commit your changes with a message that describes what you've done. Use the following command:
    
- `git commit -m "Initial commit"`
    
    Replace "Initial commit" with a message that describes the changes you've made.
- **Create a GitHub Account**: If you don't have one already, sign up for a free GitHub account at [https://github.com/](https://github.com/).
- **Create a New Repository**: Once you have a GitHub account, create a new repository by clicking on the "+" icon in the top right corner of the GitHub website and selecting "New repository".
- **Push Your Code**: In your terminal or command prompt, run the following commands to push your code to the new GitHub repository:
    

1. `git remote add origin https://github.com/your-username/your-repository.git git push -u origin master`
    
    Replace `your-username` and `your-repository` with your actual GitHub username and the name of your repository.

That's it! Your code is now uploaded to Git and available on GitHub.

**Cloning a Git Repository**

1. **Find the Repository URL**: Locate the repository you want to clone on GitHub and copy the URL, which is typically in the format `https://github.com/your-username/your-repository.git`.
2. **Open a Terminal**: Open a terminal or command prompt on your local machine.
3. **Navigate to the Desired Location**: Use the `cd` command to navigate to the directory where you want to clone the repository.
4. **Run the Clone Command**: Use the following command to clone the repository:
    

- `git clone https://github.com/your-username/your-repository.git`
    
    Replace the URL with the one you copied in step 1.
- **Access the Cloned Repository**: After the cloning process is complete, you can navigate into the cloned repository using the following command:
    

1. `cd your-repository`
    
    Replace `your-repository` with the name of the repository you just cloned.

That's it! You've successfully cloned a Git repository to your local machine.

