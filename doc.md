# Task: Implement Homepage Value Proposition Content Improvement

## Objective
Update the homepage value proposition to better communicate TeamupLMS benefits to potential customers and partners. This task involves collaborating through Git workflow including branching, pushing, and opening a pull request.

## Description
The current homepage value proposition needs refinement to be more benefit-focused and compelling for African schools. You'll improve headlines, subheadings, CTA button text, and add social proof content.

## What You'll Learn
- Git workflow (clone, branch, push, pull request)
- Collaborative development practices
- Handling merge conflicts
- Code review and feedback incorporation
- Marketing content optimization

## Steps to Complete

### 1. Setup & Clone Repository
```bash
# Clone the repository
git clone https://github.com/teamuplms/website.git
cd website

# Install dependencies
npm install

# Create a new branch for your work
git checkout -b content/homepage-value-prop
```

### 2. Locate Files to Modify
- Find homepage content files (likely in `/src/pages/` or `/content/`)
- Identify files containing:
  - Main headline
  - Subheadings
  - CTA button text
  - Social proof sections

### 3. Make Your Changes
Create/update the following content:

#### Headline Variations (create 3-5 options)
- Current: "Everything you need to manage your education"
- Option 1: [Your improved version]
- Option 2: [Your improved version]
- Option 3: [Your improved version]

#### Value Proposition (keep to 2-3 sentences)
- Address specific pain points of African schools
- Focus on benefits, not features
- Make it clear, concise, and compelling

#### CTA Button Copy
- Primary button: "Request Demo" → Consider alternatives
- Secondary button: "Get Started" → Consider alternatives

#### Social Proof Content
- Add 3-5 testimonial snippets
- Add key metrics (if available)
- Add school/partner logos section copy

### 4. Commit Your Changes
```bash
# Stage your changes
git add .

# Commit with descriptive message
git commit -m "content: improve homepage value proposition

- Refine main headline for better clarity and impact
- Rewrite value proposition to focus on school benefits
- Update CTA button text for higher conversion
- Add social proof snippets
- Create alternate headline variations for A/B testing"
```

### 5. Push to Remote
```bash
# Push your branch to GitHub
git push origin content/homepage-value-prop
```

### 6. Open a Pull Request
1. Go to GitHub repository
2. Click "New Pull Request" or use the prompt that appears
3. Select:
   - **Base branch**: `main` (or `develop`)
   - **Compare branch**: `content/homepage-value-prop`
4. Fill in the PR template:
```markdown
## Description
Updated homepage value proposition content to better communicate benefits to potential customers and improve conversion rates.

## Type of Change
- [ ] New content
- [x] Content improvement
- [ ] Bug fix
- [ ] Design change

## Changes Made
- Refined main headline for clarity
- Rewrote value proposition focusing on school benefits
- Updated CTA button text variations
- Added social proof content snippets
- Created A/B testing variations

## Screenshots/Examples
Include examples of before/after content

## Related Issues
Closes #[issue number if applicable]

## Checklist
- [x] Content is clear and benefit-focused
- [x] Copy is proofread for grammar/spelling
- [x] All links are verified
- [x] Changes follow brand voice and guidelines
- [x] Tested on mobile and desktop
```

### 7. Collaborate on the PR

#### Respond to Review Comments
When reviewers suggest changes:
```bash
# Make the requested changes locally
# Edit the relevant files

# Stage and commit
git add .
git commit -m "content: address PR feedback

- Simplify headline per reviewer suggestion
- Shorten value prop to 2 sentences
- Add more specific school pain points"

# Push to the same branch
git push origin content/homepage-value-prop
```

#### Handle Merge Conflicts (if they occur)

If someone else merged changes to `main` while you were working:
```bash
# Fetch latest changes from main
git fetch origin main

# Rebase your branch on main
git rebase origin/main

# If there are conflicts, resolve them:
# 1. Open conflicted files
# 2. Look for conflict markers:
#    <<<<<<< HEAD
#    Your changes
#    =======
#    Their changes
#    >>>>>>> branch-name
# 3. Keep the version you want (or combine both)
# 4. Delete the conflict markers

# After resolving all conflicts:
git add .
git rebase --continue

# Force push your rebased branch
git push origin content/homepage-value-prop --force-with-lease
```

Or use merge instead:
```bash
# Fetch and merge main into your branch
git fetch origin
git merge origin/main

# Resolve conflicts the same way
# Then commit and push
git add .
git commit -m "merge: resolve conflicts with main"
git push origin content/homepage-value-prop
```

### 8. Get Approval and Merge

#### When PR is Approved
1. Wait for all CI checks to pass (if configured)
2. Ensure at least 1-2 approvals from reviewers
3. Address any remaining feedback

#### Merge the PR
You have options:

**Option A: Use GitHub UI**
- Click "Merge pull request" button
- Choose merge strategy:
  - "Create a merge commit" (keeps history)
  - "Squash and merge" (cleaner history)
  - "Rebase and merge" (linear history)

**Option B: Command Line**
```bash
# Switch to main branch
git checkout main

# Update main with latest changes
git pull origin main

# Merge your branch into main
git merge content/homepage-value-prop

# Push the merged main back to GitHub
git push origin main

# Delete your feature branch locally
git branch -d content/homepage-value-prop

# Delete your feature branch on GitHub
git push origin --delete content/homepage-value-prop
```

### 9. Cleanup
```bash
# Verify your branch is deleted
git branch -a

# Update your local main branch
git pull origin main
```

## Deliverables
- [ ] Improved homepage headline (3-5 variations)
- [ ] Refined value proposition copy
- [ ] Updated CTA button text
- [ ] Social proof content snippets
- [ ] Merged pull request
- [ ] Branch properly deleted

## Acceptance Criteria
- [ ] Content is clear and benefit-focused
- [ ] Copy is proofread and error-free
- [ ] No breaking changes to page layout
- [ ] Mobile and desktop views verified
- [ ] PR reviewed and approved by at least 1 team member
- [ ] All CI checks pass
- [ ] Changes successfully merged to main branch

## Common Issues & Solutions

### "Your branch has diverged"
```bash
git pull origin content/homepage-value-prop
git rebase origin/main
git push origin content/homepage-value-prop --force-with-lease
```

### "Permission denied (publickey)"
- Ensure SSH key is added to GitHub: https://docs.github.com/en/authentication/connecting-to-github-with-ssh
- Or use HTTPS and personal access token

### "Merge conflict"
- See conflict resolution section above
- Ask a teammate if you're unsure which version to keep

### "PR shows too many files changed"
- Ensure you only modified the intended files
- Check git status to see what was changed

## Resources
- [Git Handbook](https://guides.github.com/introduction/git-handbook/)
- [GitHub Flow Guide](https://guides.github.com/introduction/flow/)
- [Resolving Merge Conflicts](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts)
- [Creating a Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-work-with-pull-requests/creating-a-pull-request)

## Tips for Success
- Keep commits focused and descriptive
- Commit often with clear messages
- Push regularly to avoid losing work
- Open PR early to get feedback sooner
- Be responsive to code review comments
- Ask questions if you're unsure about anything

## Estimated Time
- Setup & exploration: 30 minutes
- Content creation: 2-3 hours
- Incorporating feedback: 1 hour
- **Total: 4 hours**

## Support
- Tag reviewers if you have questions: `@reviewer-name`
- Ask on team Slack for Git help
- Check GitHub Issues for related discussions
