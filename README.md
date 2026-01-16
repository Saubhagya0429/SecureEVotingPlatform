 
## Group Information 
- **Student 1:** [Full Name as in LMS] - [Student ID] - Role: [Role Name]
- **Student 2:** [Full Name as in LMS] - [Student ID] - Role: [Role Name]
- **Student 3:** [Full Name as in LMS] - [Student ID] - Role: [Role Name]
  
## Project Description 
[Brief description of what your application does] 

## Live Deployment 
�
�
**Live URL:** [Your deployed application URL] 
## Technologies Used - HTML5, CSS3, JavaScript - [Any frameworks/libraries used] - GitHub Actions - [Deployment platform name] 
## Features - Feature 1 - Feature 2 - Feature 3 
## Branch Strategy 
We implemented the following branching strategy: - `main` - Production branch - `develop` - Integration branch - `feature/*` - Feature development branches 

## Individual Contributions 
### [T.A. Saubhagya Nirmandi] 
- Repository setup and configuration 
- GitHub Actions CI/CD pipeline implementation 
- Deployment setup and management 
- This section was added by DevOps Engineer.
- 
### [W.M.Pavitha Praboadhi] 
- [Repository setup and configuration]
- [GitHub Actions CI/CD pipeline implementation]
 
## Setup Instructions 
### Prerequisites - Node.js (version 18 or higher) - Git 
### Installation 
```bash 
# Clone the repository 
git clone [your-repo-url] 
# Navigate to project directory 
cd [project-name] 
# Install dependencies 
npm install 
# Run development server 
npm run dev 
# Deployment Process 
[Explain how your CI/CD pipeline works] 
# Challenges Faced 
[Optional: Describe any challenges and how you resolved them] 
# Build Status  --- 
## 
�
�
 Step-by-Step Implementation Guide 
### Phase 1: Setup (0-15 minutes) 
#### Step 1: Team Formation & Planning 
1. Form your team (2-3 students) 
2. Assign roles based on strengths 
3. Choose your project type 
4. Decide on features to implement 
#### Step 2: Repository Creation (DevOps Engineer) 
1. Go to GitHub.com and sign in 
2. Click "New Repository" 
3. Name: `[project-name]-devops-assignment` 
4. Description: "Advanced Git & DevOps Assignment - [Group Number]" 
5. Select **PUBLIC** 
6. Initialize with README: **NO** (we'll create our own) 
7. Click "Create Repository" 
#### Step 3: Add Collaborators 
1. Go to Settings → Collaborators 
2. Add all team members by GitHub username 
3. Each member should accept the invitation 
#### Step 4: Clone Repository (All Members) 
```bash 
git clone https://github.com/[username]/[repo-name].git 
cd [repo-name] 
Step 5: Initial Setup (DevOps Engineer) 
# Create initial files 
touch README.md .gitignore 
# Create branch structure 
git checkout -b develop 
git push -u origin develop 
# Create GitHub Actions directory 
mkdir -p .github/workflows 
# Add initial commit 
git add . 
git commit -m "chore: initial repository setup" 
git push origin develop 
Phase 2: Development (15-75 minutes) 
Step 6: Create Feature Branches (Each Developer) 
Each team member should: 
# Update local repository 
git checkout develop 
git pull origin develop 
# Create your feature branch 
git checkout -b feature/[your-feature-name] 
# Example: 
# git checkout -b feature/homepage-layout 
# git checkout -b feature/contact-form 
# git checkout -b feature/navigation-menu 
Step 7: Develop Your Features (Each Developer) 
Guidelines for commits: 
● Commit frequently (every significant change) 
● Write meaningful commit messages 
● Follow commit message conventions: 
○ feat: new feature 
○ fix: bug fix 
○ docs: documentation changes 
○ style: formatting changes 
○ refactor: code refactoring 
○ test: adding tests 
○ chore: maintenance tasks 
Example workflow: 
# Make changes to your files 
# ... 
# Check status 
git status 
# Add files 
git add . 
# Commit with meaningful message 
git commit -m "feat: add homepage hero section" 
# Push to your feature branch 
git push origin feature/[your-feature-name] 
Step 8: Create Pull Requests (Each Developer) 
1. Go to GitHub repository 
2. Click "Pull Requests" → "New Pull Request" 
3. Base: develop ← Compare: feature/[your-feature-name] 
4. Title: Clear description of what you've done 
5. Description: Detail the changes, any issues encountered 
6. Assign reviewers (your team members) 
7. Create Pull Request 
Pull Request Template: 
## Description 
[What does this PR do?] 
## Changes Made - Change 1 - Change 2 - Change 3 
## Screenshots (if applicable) 
[Add screenshots] 
## Testing - [ ] Tested locally - [ ] No console errors - [ ] Responsive on mobile 
## Related Issues 
Closes #[issue-number] (if applicable) 
Step 9: Code Review & Merge (All Members) 
Reviewers should: 
1. Check the code quality 
2. Test the changes locally 
3. Leave comments or approve 
4. The DevOps Engineer handles the final merge 
Merging process: 
# Switch to develop 
git checkout develop 
# Merge feature branch (after PR approval) 
git merge feature/[feature-name] --no-ff 
# Push to remote 
git push origin develop 
Create at least ONE merge conflict intentionally and resolve it (required for full marks) 
Phase 3: CI/CD Setup (45-75 minutes) 
Step 10: GitHub Actions Configuration (DevOps Engineer) 
Create CI Workflow: 
1. Create file: .github/workflows/ci.yml 
2. Add the CI configuration (see template above) 
3. Commit and push: 
git add .github/workflows/ci.yml 
git commit -m "ci: add CI pipeline workflow" 
git push origin develop 
Create Deployment Workflow: 
1. Create file: .github/workflows/deploy.yml 
2. Add the deployment configuration 
3. Commit and push 
Step 11: Cloud Deployment Setup 
Option A: Vercel (Recommended) 
Setup Steps: 
1. Go to vercel.com 
2. Sign up with GitHub (FREE, no credit card required) 
3. Click "Add New Project" 
4. Import your GitHub repository 
5. Configure: 
○ Framework Preset: (Auto-detect or select) 
○ Root Directory: ./ or ./src 
○ Build Command: npm run build (or leave default) 
○ Output Directory: dist or build (or leave default) 
6. Click "Deploy" 
Get Deployment Token for GitHub Actions: 
1. Go to Vercel Account Settings → Tokens 
2. Create new token: "GitHub Actions Token" 
3. Copy the token 
4. Go to GitHub repo → Settings → Secrets and Variables → Actions 
5. Add secrets: 
○ VERCEL_TOKEN: [your token] 
○ ORG_ID: Found in Vercel project settings 
○ PROJECT_ID: Found in Vercel project settings 
Option B: Netlify 
Setup Steps: 
1. Go to netlify.com 
2. Sign up with GitHub (FREE, no credit card) 
3. Click "Add new site" → "Import an existing project" 
4. Choose GitHub and select your repository 
5. Configure: 
○ Build command: npm run build 
○ Publish directory: dist or build 
6. Click "Deploy" 
Automatic Deployment: 
● Netlify auto-deploys on push to main 
● No additional configuration needed for basic setup 
Option C: Render 
Setup Steps: 
1. Go to render.com 
2. Sign up with GitHub (FREE, no credit card) 
3. Click "New" → "Static Site" 
4. Connect your GitHub repository 
5. Configure: 
○ Name: Your project name 
○ Branch: main 
○ Build Command: npm run build 
○ Publish Directory: dist or build 
6. Create Static Site 
Phase 4: Finalisation (75-100 minutes) 
Step 12: Merge to Main (DevOps Engineer) 
# Ensure all features are merged to develop 
git checkout develop 
git pull origin develop 
# Create Pull Request from develop to main on GitHub 
# After approval, merge to main 
git checkout main 
git merge develop 
git push origin main 
# This should trigger your deployment workflow
