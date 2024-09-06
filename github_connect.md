# **Manual: Connecting to GitHub and Submitting Your Work Using Forking**

## **Step 1: Create a GitHub Account**
If you don't already have a GitHub account, follow these steps:
1. Go to [GitHub](https://github.com/).
2. Click on **Sign up** in the upper-right corner.
3. Enter your **email**, **password**, and **username**, and follow the on-screen instructions to complete the registration process.
4. Verify your email address by following the link sent to your email.

## **Step 2: Fork the Assignment Repository**
Your instructor will provide a link to the GitHub repository where assignments are posted. You will fork this repository to work on it:
1. Go to the repository link provided by your instructor.
2. In the top-right corner of the repository page, click the **Fork** button. This will create a copy of the repository under your own GitHub account.
3. Once the fork is complete, you'll be redirected to your forked repository.

## **Step 3: Clone Your Forked Repository**
1. On your forked repository page, click the **Code** button and copy the URL (it will look like `https://github.com/your-username/repo-name.git`).
2. Open your terminal or Git Bash and navigate to the folder where you want to store the repository.
3. Run the following command to clone your forked repository to your local machine:

   ```bash
   git clone https://github.com/your-username/repo-name.git
   ```

4. This will create a local copy of your forked repository on your computer.

## **Step 4: Set Up Git Locally**
1. Open a terminal or Git Bash (on Windows).
2. Set your name and email address, which Git will use for commits:

   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

3. Verify your Git configuration:

   ```bash
   git config --list
   ```

## **Step 5: Add an Upstream Remote (Optional but Recommended)**
To keep your fork updated with the original repository, you can add an upstream remote:
1. In your terminal, navigate to the cloned repository:

   ```bash
   cd repo-name
   ```

2. Add the upstream remote, which points to the original repository:

   ```bash
   git remote add upstream https://github.com/original-repo-owner/repo-name.git
   ```

3. Fetch the latest changes from the upstream repository:

   ```bash
   git fetch upstream
   ```

## **Step 6: Add Your Work**
Once you have completed your assignment, follow these steps to add your work:
1. Copy your files (e.g., reports, Packet Tracer files, screenshots) into the relevant directory of the cloned repository (e.g., `/assignments/assignment1/`).
2. Open your terminal and navigate to your repository directory if you’re not already there.
3. Add your files to the staging area:

   ```bash
   git add .
   ```

4. Commit your changes with a message:

   ```bash
   git commit -m "Added assignment 1 files"
   ```

## **Step 7: Push Your Work to Your Forked Repository**
1. Push your changes to your GitHub forked repository:

   ```bash
   git push origin main
   ```

2. Enter your GitHub username and password if prompted (or set up SSH for password-less push).

## **Step 8: Create a Pull Request**
Now that your work is on your forked repository, you need to create a Pull Request to submit your work:
1. Go to your forked repository on GitHub.
2. Click on the **Pull requests** tab.
3. Click the **New pull request** button.
4. Ensure the comparison is between your fork and the original repository. Select your `main` branch (or the branch you worked on) and compare it to the original repository's `main` branch.
5. Provide a brief description of the work you've completed and click **Create pull request**.

## **Step 9: Verify Your Submission**
1. After creating your pull request, you will be redirected to the Pull Request page.
2. You can review the changes you made and ensure everything is correct.
3. Wait for confirmation from your instructor about your submission.

---

### **Common Git Commands Cheat Sheet**:
- `git status`: Check the status of your repository (see what files are staged, committed, etc.).
- `git add .`: Add all modified files to the staging area.
- `git commit -m "Your commit message"`: Commit the staged files with a message.
- `git push origin main`: Push your changes to the `main` branch of your forked repository.
- `git pull upstream main`: Pull changes from the original repository to keep your fork up to date.
- `git checkout -b branch-name`: Create and switch to a new branch.

---

By following this process, students can use forking to work independently on assignments and submit their work by creating a pull request. If you encounter any issues, consult GitHub’s [documentation](https://docs.github.com/en) or ask your instructor for help.
