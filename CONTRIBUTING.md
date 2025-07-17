# Contributing to Tiation Documentation

Thank you for your interest in contributing to the Tiation Documentation Hub! This guide will help you understand how to contribute effectively to our documentation.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Documentation Standards](#documentation-standards)
- [Submission Process](#submission-process)
- [Style Guide](#style-guide)
- [Review Process](#review-process)

## 🤝 Code of Conduct

By participating in this project, you agree to abide by our Code of Conduct:

- Be respectful and inclusive
- Welcome newcomers and help them get started
- Focus on constructive criticism
- Accept responsibility for mistakes and learn from them

## 🚀 Getting Started

1. **Fork the Repository**
   ```bash
   git clone https://github.com/tiation/tiation-docs.git
   cd tiation-docs
   ```

2. **Create a Branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make Your Changes**
   - Follow our documentation standards
   - Test your changes locally
   - Ensure all links work correctly

4. **Commit Your Changes**
   ```bash
   git add .
   git commit -m "docs: descriptive commit message"
   ```

## 📝 How to Contribute

### Types of Contributions

1. **Documentation Updates**
   - Fix typos or grammatical errors
   - Improve clarity and readability
   - Add missing information

2. **New Documentation**
   - Create guides for new features
   - Add API documentation
   - Write tutorials

3. **Visual Improvements**
   - Add diagrams and flowcharts
   - Create or update screenshots
   - Improve documentation structure

### Where to Contribute

- **`docs/`** - Main documentation files
- **`docs/architecture/`** - System design and architecture docs
- **`docs/api/`** - API reference documentation
- **`docs/guides/`** - How-to guides and tutorials
- **`docs/policies/`** - Company policies and standards
- **`assets/images/`** - Images and diagrams

## 📏 Documentation Standards

### File Naming
- Use lowercase with hyphens: `development-setup.md`
- Be descriptive and specific
- Group related docs in appropriate folders

### Markdown Standards
- Use GitHub Flavored Markdown
- Include a table of contents for long documents
- Use meaningful header hierarchy (H1 → H2 → H3)
- Add code syntax highlighting

### Content Guidelines
- Write in clear, simple English
- Use active voice
- Include examples where appropriate
- Keep paragraphs short and focused

## 📤 Submission Process

1. **Before Submitting**
   - [ ] Review documentation standards
   - [ ] Test all links and references
   - [ ] Check for spelling and grammar
   - [ ] Ensure consistent formatting

2. **Pull Request Template**
   ```markdown
   ## Description
   Brief description of changes

   ## Type of Change
   - [ ] Bug fix (typo, broken link, etc.)
   - [ ] New documentation
   - [ ] Documentation improvement
   - [ ] Visual enhancement

   ## Checklist
   - [ ] Follows style guide
   - [ ] Links are working
   - [ ] Screenshots are included (if applicable)
   - [ ] Related issues are referenced
   ```

3. **Submit Pull Request**
   - Use descriptive title
   - Reference related issues
   - Add appropriate labels

## 🎨 Style Guide

### Writing Style
- **Be Concise**: Get to the point quickly
- **Be Consistent**: Use the same terminology throughout
- **Be Helpful**: Anticipate reader questions
- **Be Professional**: Maintain a professional tone

### Formatting
```markdown
# Main Title (H1)

Brief introduction paragraph.

## Section Title (H2)

### Subsection Title (H3)

**Bold** for emphasis
*Italic* for slight emphasis
`code` for inline code

- Bullet points for lists
- Keep points concise

1. Numbered lists for steps
2. Use when order matters
```

### Code Blocks
````markdown
```javascript
// Use syntax highlighting
function example() {
  return "Hello, World!";
}
```
````

### Links
- Use descriptive link text: `[Development Guide](link)` ✓
- Avoid: `[Click here](link)` ✗

### Images
```markdown
![Descriptive Alt Text](assets/images/image-name.png)
*Image caption explaining what the image shows*
```

## 🔍 Review Process

### Review Criteria
1. **Accuracy**: Information is correct and up-to-date
2. **Clarity**: Easy to understand for target audience
3. **Completeness**: Covers topic thoroughly
4. **Consistency**: Follows established patterns
5. **Quality**: Well-written and professional

### Review Timeline
- Simple fixes: 1-2 days
- New documentation: 3-5 days
- Major changes: 1 week

### After Merge
- Documentation is automatically deployed
- Changes appear on GitHub Pages site
- Contributors are added to acknowledgments

## 🙏 Recognition

We value all contributions! Contributors will be:
- Listed in our Contributors section
- Mentioned in release notes
- Thanked in our community updates

## ❓ Questions?

If you have questions:
1. Check existing documentation
2. Search closed issues
3. Ask in discussions
4. Create an issue

---

Thank you for helping improve Tiation documentation! 🎉
