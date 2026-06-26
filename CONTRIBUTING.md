# Contributing to Linux Commands Reference Guide

Thank you for your interest in contributing! 🎉 We welcome contributions from everyone.

## How to Contribute

### 1. Reporting Bugs
If you find an error or inaccuracy:

1. Check if the issue already exists in [Issues](../../issues)
2. If not, create a new issue with:
   - Clear title describing the problem
   - Description of the issue
   - Command name affected
   - Suggested correction (if any)
   - Your Linux distribution and version

**Example:**
```
Title: Fix example for grep command

Description:
The example for grep shows `grep fail` but should be `grep "fail"`

Affected Command: grep (#8)
```

### 2. Suggesting Improvements
Want to improve explanations or add examples?

1. Open an issue with your suggestion
2. Describe what should be added/changed
3. Provide details or examples if possible

### 3. Adding New Commands
To add a new command:

1. Check if command already exists in the guide
2. Fork the repository
3. Create a branch: `git checkout -b add/command-name`
4. Add command following this template:
   ```markdown
   ### XX. `command` - Full Name
   **Purpose:** One line description
   ```bash
   command example
   # Output: expected output
   ```
   **Options:**
   - `-option` - Description
   ```

5. Commit: `git commit -am 'Add command-name'`
6. Push: `git push origin add/command-name`
7. Open a Pull Request

### 4. Improving Examples
Found a command with unclear examples?

1. Fork the repository
2. Create a branch: `git checkout -b improve/command-name`
3. Update the examples to be clearer
4. Test your examples if possible
5. Submit a Pull Request

### 5. Fixing Documentation
Found typos or unclear explanations?

1. Fork the repository
2. Fix the issue
3. Commit with clear message: `git commit -am 'Fix typo in command-name'`
4. Push and open a Pull Request

---

## Pull Request Process

### Before You Start
- [ ] Fork the repository
- [ ] Create a descriptive branch name
- [ ] Make changes in your local environment
- [ ] Test your changes

### Submitting a PR
1. Push your changes to your fork
2. Open a Pull Request on the main repository
3. Provide:
   - Clear title
   - Description of changes
   - Reason for changes
   - Reference any related issues (#123)

### PR Template
```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New command
- [ ] Improved example
- [ ] Documentation update

## Changes Made
- Change 1
- Change 2
- Change 3

## Testing
How did you test these changes?

## Related Issues
Fixes #123
```

### Review Process
- Your PR will be reviewed by maintainers
- We may request changes
- Once approved, it will be merged
- You'll be credited in the changelog

---

## Style Guide

### Command Format
```markdown
### XX. `command` - Command Full Name
**Purpose:** One sentence description

```bash
command example     # Comment
# Output: example output
```

**Options:**
- `-option` - Description of option
- `-another-option` - Description

**Examples:**
```bash
command -option    # Example 1
command arg        # Example 2
```

### Writing Guidelines
1. **Be Clear**: Use simple, understandable language
2. **Be Accurate**: Verify commands before submitting
3. **Be Consistent**: Follow existing format
4. **Be Helpful**: Add useful examples
5. **Be Safe**: Warn about dangerous commands

### Markdown Tips
- Use backticks for commands: `command`
- Use code blocks for examples
- Use **bold** for emphasis
- Use links for references
- Use headers for organization

---

## File Structure

```
linux-commands-guide/
├── README.md                          # Main documentation
├── LINUX_COMMANDS_REFERENCE.md        # Complete command reference
├── CONTRIBUTING.md                    # This file
├── LICENSE                            # MIT License
├── CHANGELOG.md                       # Version history
└── .gitignore                         # Git ignore rules
```

---

## Commit Message Guidelines

Write clear, meaningful commit messages:

```bash
# Good commit messages
git commit -m "Add chmod command with examples"
git commit -m "Fix grep example - change flag to -i"
git commit -m "Improve df command description"

# Avoid these
git commit -m "fix"
git commit -m "update"
git commit -m "changes"
```

### Format
```
[TYPE] Brief description

More detailed explanation if needed.
- Point 1
- Point 2

Fixes #123
```

**Types:**
- `add` - Add new content
- `fix` - Fix error or typo
- `improve` - Improve existing content
- `refactor` - Reorganize content
- `docs` - Documentation changes

---

## Code of Conduct

### Our Pledge
We are committed to providing a welcoming and inclusive environment.

### Expected Behavior
- Be respectful and inclusive
- Welcome feedback and criticism
- Focus on constructive discussion
- Respect differing opinions

### Unacceptable Behavior
- Harassment or discrimination
- Offensive comments
- Trolling or spamming
- Other unprofessional conduct

### Reporting
If you witness unacceptable behavior, please report it by opening an issue with details.

---

## Testing Your Changes

Before submitting a PR:

1. **Verify accuracy**: Test commands if possible
2. **Check formatting**: Ensure markdown is clean
3. **Review examples**: Make sure examples work
4. **Proofread**: Check for typos and grammar

### Testing on Linux
```bash
# Clone your fork
git clone https://github.com/yourusername/linux-commands-guide.git
cd linux-commands-guide

# View the file
cat LINUX_COMMANDS_REFERENCE.md

# Search for your changes
grep "your-command" LINUX_COMMANDS_REFERENCE.md
```

---

## Getting Help

- **Questions?** Open a discussion issue
- **Stuck?** Check existing PRs for examples
- **Ideas?** Open an issue to discuss first
- **Want to chat?** Comment on relevant issues

---

## Recognition

Contributors will be:
- Listed in the README under "Contributors"
- Credited in the CHANGELOG
- Given credit in relevant commits

---

## Common Contribution Types

### Adding a New Command
```markdown
### XX. `command` - Full Name
**Purpose:** What does this command do?

```bash
command example
```

**Options:**
- `-option` - What it does

**Examples:**
```bash
command -option value
```

### Fixing a Typo
1. Find the typo in the markdown
2. Correct it
3. Commit with message: "Fix typo in command-name"

### Improving an Explanation
1. Find the command
2. Clarify the description
3. Add better examples if needed
4. Commit with message: "Improve command-name explanation"

---

## FAQ for Contributors

**Q: How long before my PR is reviewed?**  
A: Usually within 3-5 days. We review when maintainers are available.

**Q: Can I add multiple commands in one PR?**  
A: Prefer one PR per change, but multiple related commands are OK.

**Q: What if my PR is rejected?**  
A: We'll explain why and suggest improvements. You can update and resubmit.

**Q: Do I need permission to contribute?**  
A: No! Just fork and submit a PR. Anyone can contribute.

**Q: Can I edit other contributors' work?**  
A: Yes, improvement suggestions welcome. Discuss in PR comments first.

---

## Resources for Contributors

- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Contributing Guide](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions)
- [Linux Man Pages](https://man7.org/)
- [Commit Message Guidelines](https://www.conventionalcommits.org/)

---

## Final Notes

- Thank you for contributing! 🙏
- Even small contributions help
- We appreciate all types of contributions
- Questions? Don't hesitate to ask!

---

**Happy Contributing! 🚀**
