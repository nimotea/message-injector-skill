# Message Injector Skill

A specialized skill for extracting information from source text and injecting it into target templates with placeholders.

## Features
- **Information Extraction**: Automatically identifies key entities from source text.
- **Placeholder Injection**: Maps extracted information to placeholders like `{name}`, `{date}`, etc.
- **Flexible Templates**: Supports various placeholder formats (e.g., `{}`, `{{}}`, `<>`).

## How to use
This skill is designed for use within the Trae/Claude ecosystem.

### Installation
(Coming soon - will be available as a `.skill` package)

### Usage
Provide a source text and a template, and the skill will return the injected result.

**Example**:
- **Source**: "Alice is 25 years old."
- **Template**: "User {name} is {age}."
- **Output**: "User Alice is 25."

## Project Structure
- `message-injector/SKILL.md`: The core skill definition.
- `message-injector/evals/evals.json`: Test cases for evaluation.
