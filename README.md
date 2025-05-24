# Step-by-step commands used:

npx create-react-app propeller-task
cd propeller-task
git init
gh auth login
gh repo create propeller-task --public --source=. --remote=origin --push
git checkout -b update_logo

# Replaced logo.svg with Vector.svg
# Updated App.js link

git add .
git commit -m "Updated logo and link"
git push origin update_logo
gh pr create --base master --head update_logo --title "Update logo and link" --body "Replaced logo and updated link"
gh pr merge --merge

# REPO_URL https://github.com/YOUR_USERNAME/propeller-task
