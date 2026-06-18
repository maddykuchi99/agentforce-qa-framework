# Contributing to Agentforce QA Framework

Thank you for your interest in contributing! This document provides guidelines for contributing to the project.

## How to Contribute

### Reporting Issues

- Use the [GitHub Issues](https://github.com/maddykuchi99/agentforce-qa-framework/issues) page
- Check if the issue already exists before creating a new one
- Provide as much detail as possible:
  - Framework version
  - Salesforce org type (sandbox, production, scratch)
  - Steps to reproduce
  - Expected vs actual behavior
  - Screenshots if applicable

### Suggesting Enhancements

- Open an issue with the `enhancement` label
- Describe the enhancement and why it would be useful
- Provide examples of how it would work

### Pull Requests

1. **Fork the repository**
2. **Create a feature branch** from `main`
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes**
   - Follow existing code style
   - Update documentation if needed
   - Add examples if applicable
4. **Test your changes**
   - Verify subagents still work
   - Test with at least one agent
5. **Commit with clear messages**
   ```bash
   git commit -m "Add: brief description of changes"
   ```
6. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```
7. **Open a Pull Request**
   - Describe what changed and why
   - Reference any related issues

## Development Guidelines

### Subagent Development

When creating or modifying subagents (`.claude/agents/*.md`):

- Follow the existing frontmatter format:
  ```markdown
  ---
  name: subagent-name
  description: Brief description
  tools: Tool1, Tool2
  ---
  ```
- Include clear step-by-step instructions
- Add examples where helpful
- Test with multiple agents if possible

### Documentation

- Update README.md if adding features
- Add examples to `examples/` directory
- Keep docs concise but complete
- Use clear language (avoid jargon when possible)

### Registry Schema

If modifying `.claude/agents-registry.yml` structure:

- Maintain backward compatibility when possible
- Update the example file
- Document new fields in README
- Provide migration guide if breaking changes

## Code of Conduct

- Be respectful and inclusive
- Focus on constructive feedback
- Help others learn and grow
- Assume good intentions

## Questions?

- Open a [GitHub Discussion](https://github.com/maddykuchi99/agentforce-qa-framework/discussions)
- Tag issues with `question` label

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
