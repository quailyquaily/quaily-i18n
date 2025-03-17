# Contributing to Quaily i18n

Thank you for your interest in contributing to Quaily i18n! This document provides guidelines and instructions for contributing translations to the Quaily ecosystem.

## Project Overview

Quaily i18n contains language files for three main components:

- **SPA**: Single Page Application frontend
- **Dashboard**: Admin dashboard interface
- **Service**: Backend service

Each component has its own language files in different formats:

- SPA and Dashboard use JSON files
- Service uses TOML files

## Getting Started

### Prerequisites

- Basic knowledge of JSON and/or TOML file formats
  - The indentation is 2 spaces
  - Please DO NOT USE nested structure for the JSON files, it's not easy to maintain.
- Familiarity with Git and GitHub for submitting changes
- Proficiency in both English and the target language you want to contribute to

### Setup

1. Fork the repository
2. Clone your fork to your local machine
3. Create a new branch for your changes

## How to Contribute

### Adding or Improving Translations

1. **Identify the Component**: Determine whether your translation is for the SPA, Dashboard, or Service.

2. **Find the Source File**: Locate the English source files:

   - For SPA: `spa/lang/en.json`
   - For Dashboard: `dashboard/lang/en.json`
   - For Service: `service/locales/en.toml`

3. **Create or Edit Target Language File**: Copy the structure of the English file and translate the content.

   - Keep the same keys and structure
   - Only translate the values, not the keys
   - Maintain any variables or placeholders (e.g., `{variable}` or `%{variable}`)
   - Follow the existing naming conventions

4. **Check Consistency with Glossary**: Refer to `glossary.json` for standardized translations of key terms. If you're adding a new term that should be in the glossary, please update it as well.

### AI Translation (Optional)

To reduce the workload of manual translation, we recommend using our AI translate tool [translate-cli](https://github.com/quailyquaily/translate-cli) to translate the content first.

> [!NOTE]
> 1. The `translate-cli` is a command-line tool that uses LLM to translate the content. It's not a web application, so you need to install it on your local machine.
> 2. At the moment, the `translate-cli` only supports translating JSON files.

Here is a quick command to translate the content of dashboard:

```bash
translate-cli translate -s dashboard/lang/en.json -d dashboard/lang -g glossary.json --batch=10
```

For more details, please refer to the [translate-cli README](https://github.com/quailyquaily/translate-cli/blob/main/README.md).

### Translation Guidelines

- Start from the English source file, add new messages to it first.
- Ensure translations are accurate and convey the same meaning as the English version
- Maintain consistent terminology throughout the translations
- Respect cultural nuances and adapt content appropriately
- Preserve formatting, including HTML tags if present
- Keep string lengths reasonable to avoid UI display issues

### Testing Your Translations

When possible, test your translations in the actual application to ensure they display correctly and make sense in context.

## Submitting Changes

1. **Commit Your Changes**: Use clear, descriptive commit messages.

2. **Push to Your Fork**: Push your changes to your forked repository.

3. **Create a Pull Request**: Submit a pull request to the main repository.
   - Provide a clear title and description of your changes
   - Mention which language(s) and component(s) you've modified
   - Include any special considerations or notes for reviewers

## Review Process

All contributions will be reviewed by maintainers or other contributors who are proficient in the target language. Feedback may be provided for improvements.

## Additional Notes

### Adding a New Language

If you're adding support for a new language:

1. Create the language file in all three components (SPA, Dashboard, and Service)
2. Add the language to the glossary
3. Update the README.md if appropriate to credit yourself as the initial translator

### Reporting Issues

If you find issues with existing translations but don't have time to fix them yourself, please open an issue in the GitHub repository describing the problem.

## Code of Conduct

Please be respectful and considerate of others when contributing. We aim to foster an inclusive and welcoming community.

## Credits

When you contribute translations, your name will be added to the contributors section of the README.md file.

Thank you for helping make Quaily accessible to users around the world!
