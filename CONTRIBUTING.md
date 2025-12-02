# Contributing to LiamBFlynn

Thank you for your interest in contributing to the LiamBFlynn Ollama model! This document provides guidelines for contributing to the project.

## Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inclusive experience for everyone. We expect all contributors to:

- Be respectful and considerate
- Welcome diverse perspectives and experiences
- Accept constructive criticism gracefully
- Focus on what is best for the community
- Show empathy towards other community members

### Unacceptable Behavior

- Hate speech, discrimination, or harassment of any kind
- Offensive comments related to personal characteristics
- Trolling, insulting, or derogatory comments
- Publishing others' private information without permission
- Any conduct that would be inappropriate in a professional setting

## How to Contribute

### Reporting Issues

If you find a bug or have a suggestion:

1. Check if the issue already exists in the [Issues](https://github.com/J9ck/LiamBFlynn/issues) section
2. If not, create a new issue with:
   - A clear, descriptive title
   - Detailed description of the problem or suggestion
   - Steps to reproduce (for bugs)
   - Expected vs actual behavior
   - Your environment (OS, Ollama version, etc.)

### Suggesting Enhancements

Enhancement suggestions are welcome! Please:

1. Use a clear and descriptive title
2. Provide a detailed description of the proposed feature
3. Explain why this enhancement would be useful
4. Include examples of how it would work

### Pull Requests

1. **Fork the repository** and create your branch from `main`:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes**:
   - Keep changes focused and atomic
   - Maintain the character's authenticity
   - Ensure content is respectful and appropriate
   - Test your changes thoroughly

3. **Test the modelfile**:
   ```bash
   ollama create liambflynn-test -f modelfiles/Modelfile
   ollama run liambflynn-test
   # Test various conversations
   ```

4. **Commit your changes**:
   ```bash
   git commit -m "Brief description of your changes"
   ```
   
   Use clear, descriptive commit messages.

5. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

6. **Open a Pull Request**:
   - Provide a clear title and description
   - Reference any related issues
   - Describe what you changed and why
   - Include examples of the changes in action

## Development Guidelines

### Modelfile Changes

When modifying the Modelfile:

1. **Maintain character consistency**: Keep Liam's personality authentic
2. **Test thoroughly**: Ensure changes don't break existing functionality
3. **Be respectful**: All content must be appropriate and non-offensive
4. **Document changes**: Update relevant documentation

### Documentation Changes

- Use clear, concise language
- Include examples where helpful
- Maintain consistent formatting
- Check for typos and grammar

### Code Style

For scripts (if added):

**Python**:
- Follow PEP 8
- Use type hints where appropriate
- Include docstrings for functions

**JavaScript**:
- Use ESLint recommended rules
- Prefer const/let over var
- Use meaningful variable names

## Testing

Before submitting changes:

1. Test the modelfile with Ollama
2. Try various conversation scenarios
3. Ensure documentation is accurate
4. Check for any breaking changes

## Content Guidelines

### Character Authenticity

- Keep Liam's personality consistent with the established character
- Maintain his voice: casual, friendly, respectful
- Preserve core traits: values friendship, loves baseball, committed to self-improvement

### Respectful Content

**Required**:
- Treat all individuals and groups with respect
- Use inclusive language
- Focus on positive character traits

**Not Allowed**:
- Hate speech or discriminatory content
- Offensive or inappropriate material
- Personal information (addresses, phone numbers, etc.)
- Harmful stereotypes

## Review Process

1. **Initial Review**: A maintainer will review your PR for:
   - Adherence to guidelines
   - Code/content quality
   - Testing completeness

2. **Feedback**: You may receive requests for changes
   - Address feedback promptly
   - Ask questions if anything is unclear

3. **Approval**: Once approved, your PR will be merged
   - Your contribution will be credited
   - Thank you for helping improve the project!

## Project Structure

```
LiamBFlynn/
├── modelfiles/          # Ollama modelfiles
│   ├── Modelfile        # Main modelfile
│   ├── liam.json        # Web UI config
│   └── ...              # Other configurations
├── examples/            # Example conversations
├── docs/                # Documentation
│   └── setup.md         # Setup guide
├── update               # Update script
├── README.md            # Main documentation
├── CONTRIBUTING.md      # This file
└── .gitignore          # Git ignore rules
```

## Getting Help

Need help contributing?

- Review existing [Issues](https://github.com/J9ck/LiamBFlynn/issues) and [Pull Requests](https://github.com/J9ck/LiamBFlynn/pulls)
- Check the [Ollama documentation](https://github.com/ollama/ollama/tree/main/docs)
- Open a discussion for questions
- Reach out to maintainers

## Recognition

Contributors will be:
- Listed in the repository contributors
- Credited in release notes for significant contributions
- Appreciated by the community!

## License

By contributing, you agree that your contributions will be used in accordance with the project's educational and entertainment purposes.

---

## Quick Checklist

Before submitting:

- [ ] Changes are tested with Ollama
- [ ] Documentation is updated (if needed)
- [ ] Content is respectful and appropriate
- [ ] Commit messages are clear
- [ ] Character authenticity is maintained
- [ ] Code/content follows project guidelines
- [ ] No personal or sensitive information included

Thank you for contributing to LiamBFlynn! 🎉
