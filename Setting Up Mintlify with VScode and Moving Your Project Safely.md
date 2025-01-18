# Setting Up Mintlify with VScode and Moving Your Project Safely

## Safely Relocating a Mintlify Project Without Disrupting Git or Deployment

![](/Images/Mintlify.JPG)

I didn't realize that creating API documentation could be so stress-free when you don't have to start from scratch. That's where [**Mintlify**](https://dashboard.mintlify.com/login) comes in. It offers many features that help writers make their work seamless. The best part is that you can work locally!

This is a beginner's step-by-step guide tailored for you if you find it challenging to set up your project in VScode and access it from your desired `path`.

### Prerequisites

- Git, GitHub,
- Visual Studio Code (VScode),
- Node.js.

### Steps to clone a Mintlify project

After successfully creating an account, you will be directed to connect your GitHub account.

![](/Images/Screenshot-%20github-signin_success.jpg)

It's a breeze, so it doesn't take much time. Next, You'll create a `GitHub repository`, which will be handled automatically.

![](/Images/Screenshot-mintlify-doc_repo.jpg)

The final step, though not the least important, is to clone the repository. All you need to do is copy the clone URL of the repository, then open your terminal and paste it there. After successfully cloning the repository, make sure to enter `code .`to open it in VS Code.

![](/Images/Screenshot-mintlify_clone_sucess.jpg)

_If you can see this, you're all set!_

![](/Images/Screenshot-cloned%20work.jpg)

### Transferring Mintlify project to a specified path

The first time I cloned the project, I discovered it was saved on my local disk 😑. I had to move it to a more suitable location where I work on various projects, all while ensuring that it remains in sync with Mintlify and is still git-enabled.

Don't worry!, just a little bit of Git knowledge will suffice, _techie! So yes, go learn Git!_

#### Steps

**Locate the Current Project Folder:**
Open **File Explorer** and navigate to `C:\Windows\System32\docs`.

![](/Images/Screenshot-docs.jpg)

**Move the Project:**

- Right-click the `docs` folder (or your specific Mintlify project folder).
- Select **Cut** (to move).
- Navigate to `{Your_Specified_Path/Folder}`
- Right-click in the folder and select **Paste**.

**Use VScode:**

After opening the folder in VScode, go to the terminal and enter the command `git remote remove origin`. You will encounter an error message. Simply follow the instructions provided, which will help resolve your **Git-related problem**. Here's what you'll see.

```txt
PS C:\Users\hi\Downloads\Work\docs> git remote remove origin
fatal: detected dubious ownership in repository at 'C:/Users/hi/Downloads/Work/docs'
'C:/Users/hi/Downloads/Work/docs' is owned by:
        'S-1-5-32-544'
but the current user is:
        'S-1-5-21-1928432222-3671853227-2616346337-1001'
To add an exception for this directory, call:

    git config --global --add safe.directory C:/Users/hi/Downloads/Work/docs
PS C:\Users\hi\Downloads\Work\docs> git config --global --add safe.directory C:/Users/hi/Downloads/Work/docs
PS C:\Users\hi\Downloads\Work\docs> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\Users\hi\Downloads\Work\docs>
```

**Verifying the Deployment Setup**

To ensure it works in any directory, input the command `npm install -g mintlify`. Then, type `mintlify dev` to start the localhost server. Well done! 👏🏾

![](/Images/Screenshot-mintlify_dev-1.jpg)

### Conclusion

Relocating a Mintlify project and ensuring it integrates smoothly with Git and deployment pipelines can seem challenging. However, by following the right steps, you can simplify the process. This guide covers everything from setting up the project in VScode to re-enabling Git and verifying that everything functions properly. By following these instructions, you can avoid common pitfalls and maintain your productivity.&#x20;

If you have any insights on more efficient ways to resolve these issues, please share!
