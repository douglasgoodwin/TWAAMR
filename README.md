# Refurbish The Work of Art in the Age of Mechanical Reproduction



## GitHub Writing Workshop Guide
### Rewriting Walter Benjamin's "The Work of Art in the Age of Mechanical Reproduction"

### Initial Setup

```bash
# Configure Git
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Generate SSH key
ssh-keygen -t ed25519 -C "your.email@example.com"

# Clone repository
git clone https://github.com/douglasgoodwin/TWAAMR.git
cd TWAAMR
```

### Project Structure

```
TWAAMR/
├── .gitignore           # Excludes temporary files
├── chapters/           
│   ├── chapter1.md      # Your assigned chapter
│   └── notes.md         # Research and drafting notes
└── style-guide.md       # Formatting standards
```

### Branch Structure

```
main
└── student/<username>
    └── 01.md
        ├── draft
        └── review
```

### Basic Workflow

1. **Create Your Space**
```bash
git checkout main
git pull
git checkout -b student/yourname
git checkout -b student/yourname/chapter1/draft
```

2. **Save Changes**
```bash
git add chapter1.md
git commit -m "draft: initial rewrite of introduction"
```

3. **Backup Work**
```bash
git push origin draft/chapter1
```

### Writing Guidelines

1. Format chapters in Markdown:
```markdown
# Chapter Title

## Section Heading
Your rewritten text here. Include citations:
> Original Benjamin: "Quote here"
```

2. Commit standards:
- draft: Initial writing
- revise: Content changes
- style: Formatting only
- cite: Citation updates

### Peer Review Process

1. Request review:
```bash
git push origin draft/chapter1
# Create pull request on GitHub
```

2. Review changes:
- Comment on specific lines
- Suggest alternative interpretations
- Check style consistency

3. Incorporate feedback:
```bash
git checkout draft/chapter1
# Make changes
git commit -m "revise: address reviewer comments"
```

### Final Submission

1. Update from main:
```bash
git checkout draft/chapter1
git pull origin main
git rebase main
```

2. Final checks:
- [ ] Markdown formatting clean
- [ ] Citations verified
- [ ] Style guide followed
- [ ] Peer review addressed

3. Merge to main:
```bash
git checkout main
git merge draft/chapter1
git push origin main
```

### Troubleshooting

1. **Resolve conflicts**:
```bash
git status
# Edit conflicted files
git add <resolved-files>
git commit
```

2. **Undo last commit**:
```bash
git reset --soft HEAD~1
```

3. **Recover lost work**:
```bash
git reflog
git checkout -b recovery HEAD@{1}
```

### Writing Milestones

1. First Draft
- Read original chapter
- Outline key concepts
- Write initial translation

2. Revision
- Add modern examples
- Connect to adjacent chapters
- Format citations

3. Final Polish
- Apply style guide
- Complete peer review
- Prepare for merge

