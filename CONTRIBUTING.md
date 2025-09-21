# Contributing to MirrorCloneFX

Thank you for your interest in contributing to MirrorCloneFX! We welcome contributions from everyone.

## How to Contribute

### Reporting Bugs

Before creating bug reports, please check the existing issues to avoid duplicates. When you create a bug report, include as many details as possible:

- **Use a clear and descriptive title**
- **Describe the exact steps to reproduce the problem**
- **Provide specific examples** to demonstrate the steps
- **Describe the behavior you observed** and explain what you expected to see instead
- **Include screenshots or videos** if applicable
- **Include your environment details**: OS, Python version, camera type

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion:

- **Use a clear and descriptive title**
- **Provide a detailed description** of the suggested enhancement
- **Explain why this enhancement would be useful** to most users
- **Include mockups or examples** if applicable

### Code Contributions

#### Development Workflow

1. **Fork** the repository on GitHub
2. **Clone** your fork locally
3. **Create a new branch** from `main` for your feature/fix
4. **Make your changes** with appropriate tests
5. **Test your changes** thoroughly
6. **Commit** with clear, descriptive messages
7. **Push** to your fork
8. **Create a Pull Request**

#### Setting Up Development Environment

```bash
# Clone your fork
git clone https://github.com/YOUR-USERNAME/MirrorCloneFX.git
cd MirrorCloneFX

# Install dependencies
pip install -r requirements.txt

# Create a new branch
git checkout -b feature-or-fix-name
```

#### Code Style

- Follow **PEP 8** Python style guidelines
- Use **meaningful variable and function names**
- Add **docstrings** for functions and classes
- Include **comments** for complex logic
- Keep **functions focused** and reasonably sized
- Ensure **Python 3.7+ compatibility**

#### Testing

- **Test your changes** on multiple platforms if possible
- **Verify camera functionality** with different webcam types
- **Test gesture recognition** in various lighting conditions
- **Check performance** with your changes
- **Ensure no regressions** in existing functionality

#### Adding New Visual Effects

When adding new visual effects:

1. **Create a new method** in the `MirrorCloneFX` class
2. **Follow the existing pattern** for effect methods
3. **Add proper documentation** explaining the effect
4. **Update the gesture mapping** if needed
5. **Test thoroughly** with different inputs
6. **Update the README** with the new effect information

Example structure:
```python
def create_new_effect(self, frame, landmarks=None):
    """
    Create a new visual effect.
    
    Args:
        frame: Input video frame
        landmarks: Hand landmarks (if needed)
        
    Returns:
        Processed frame with the new effect
    """
    # Your implementation here
    return processed_frame
```

### Pull Request Guidelines

#### Before Submitting

- **Test your changes** thoroughly
- **Update documentation** if needed
- **Ensure code follows** style guidelines
- **Check that all files** have appropriate headers
- **Verify no sensitive information** is included

#### Pull Request Format

Use this template for your pull request:

```markdown
## Description
Brief description of changes made.

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
Describe how you tested your changes.

## Screenshots/Videos
Include if applicable.

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Documentation updated
- [ ] No new warnings introduced
```

#### Review Process

- **Maintainers will review** your pull request
- **Address feedback** promptly and professionally
- **Be patient** - reviews take time
- **Ask questions** if feedback is unclear
- **Update your branch** if requested

### Community Guidelines

#### Be Respectful

- **Use welcoming and inclusive language**
- **Respect different viewpoints** and experiences
- **Accept constructive criticism** gracefully
- **Focus on what's best** for the community

#### Communication

- **Be clear and concise** in your communication
- **Provide context** for your suggestions or issues
- **Ask questions** if something is unclear
- **Help others** when you can

### Recognition

Contributors will be recognized in the following ways:

- **Listed in README** acknowledgments
- **Mentioned in release notes** for significant contributions
- **Referenced in commit messages** and pull requests

### Getting Help

If you need help:

- **Check existing issues** and documentation first
- **Create a new issue** with the "question" label
- **Be specific** about what you need help with
- **Provide context** about what you're trying to achieve

### License

By contributing to MirrorCloneFX, you agree that your contributions will be licensed under the MIT License.

Thank you for contributing to MirrorCloneFX!