
# cursor rules

Collection of cursor rules for different applications and programming languages.

[Cursor Rules for AI](https://docs.cursor.com/context/rules-for-ai)

Cursor Rules are configuration files that define how AI should interact with your codebase. They provide context-aware assistance by setting guidelines, constraints, and behavioral patterns for AI interactions.

## Global Rules

Global cursor rules apply across all projects and provide default behavior for all prompts. These can be configured in:

Cursor Settings > General > Rules for AI

Global rules are ideal for setting:
- Output language preferences
- Response length guidelines
- Universal coding standards
- Default behavior patterns

## Project-Specific Rules

Project rules offer a powerful and flexible system with path-specific configurations. These rules are stored in the `.cursor/rules` directory and provide granular control over AI behavior in different parts of your project.

### Key Features
- **Semantic Descriptions:** Each rule can include a description of when it should be applied
- **File Pattern Matching:** Use glob patterns to specify which files/folders the rule applies to
- **Automatic Attachment:** Rules are automatically included when matching files are referenced
- **Reference Files:** Use `@file` in your project rules to include them as context when the rule is applied
- **Rule Chaining:** Reference other rule files using `@file` to combine multiple rules

### Creating Rules
Use the command palette (Cmd + Shift + P > New Cursor Rule) to create new rules. Rules are version-controlled as they're stored in your project repository.

### Location
Create a `.cursor/rules` directory in your project root and add your rule files:
```bash
project-root/
├── .cursor/
│   └── rules/
│       ├── javascript.mdc
│       ├── python.mdc
│       └── general.mdc
└── ...
```

With these rules in place, AI will have a well-defined context for your project, providing more accurate and relevant assistance.

Now you can use these rules to enhance your AI interactions with your codebase.

Also recommend to set up proper project requirement documents before getting started.
