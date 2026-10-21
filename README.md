# Hands-on Lab: Using Git to Track and Manage Changes for a Simple Form

## Scenario

Your client has provided a simple HTML form that collects a user's name, email, and message. You will use Git to track changes, maintain a history, and restore previous versions when needed.

## Prerequisites

- Git installed on your machine
- Basic understanding of Git commands
- An existing GitHub repository named `simple-form`
- The `form.html` and `style.css` files

## Tasks

### 1. Clone the GitHub Repository

Clone the repository and navigate to its folder.

git clone <https://github.com/yourusername/simple-form.git>
cd simple-form
Replace yourusername with your actual GitHub username.

### 2. Stage the Form Files

Place `form.html` and `style.css` in the project folder, then stage them.

git add form.html style.css

### 3. Commit the Initial Version

Save the initial version in Git history.

git commit -m "Initial commit for simple form"

### 4. Push to GitHub

Upload the initial commit to GitHub.

git push origin main

### 5. Make and Track Changes

Update `form.html` to include a phone number field and modify `style.css`.

Stage and commit the changes.

git add form.html style.css
git commit -m "Added phone number field and updated styles"

### 6. Push the Updates

Push the latest changes to GitHub.

git push origin main

### 7. View the Project History

View previous commits to identify changes and find a working version.

git log

### 8. Restore a Previous Version of the Form

Find the commit hash of the last working version using `git log`. Restore only `form.html` from that commit.

git checkout 2122d57 -- form.html

Stage and commit the restoration if you want to save it in the current branch.

git add form.html
git commit -m "Restore previous working form"

### 9. Create a Feature Branch

Create a separate branch to experiment with adding CAPTCHA.

git checkout -b feature-add-captcha

Make the necessary changes to `form.html`, then stage and commit them

git add form.html
git commit -m "Added CAPTCHA feature"

### 10. Merge the Feature Branch

Switch back to `main` and merge the CAPTCHA changes.

git checkout main
git merge feature-add-captcha

### 11. Push the Merged Changes

Upload the merged changes to GitHub.

git push origin main

### 12. Undo Uncommitted Changes

If you make unwanted changes to `style.css` and have not committed them, restore the file to its latest committed version.

git checkout -- style.css

### 13. Pull Updates from GitHub

git pull origin main
