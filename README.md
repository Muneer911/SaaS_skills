# saas-skills

Reusable Agent Skills library for standardized SaaS development workflows. Compatible with Claude Code, Cursor, Windsurf, Aider, and any AI agent that supports the OpenSkills standard.

## Overview

This repository contains production-ready skills that enforce strict development standards across projects. Each skill is designed to be progressively loaded by AI agents, providing detailed instructions only when needed.

## Available Skills

### 🎨 rtl-ui
**Right-to-Left UI Development**
- Tailwind RTL utility patterns
- Icon mirroring strategies
- Arabic typography best practices
- Spacing and layout constraints for bidirectional interfaces

### 🌍 arabic-localization
**Arabic Internationalization Standards**
- i18n structure and file organization
- Translation key naming conventions
- Tone variation: Najdi dialect, Professional Modern, and Modern Standard Arabic (MSA)
- Context-aware localization guidelines

### 🔐 auth-supabase
**Supabase Authentication Implementation**
- Standard authentication flow patterns
- Email template customization
- Environment variable checklists
- Security best practices and error handling

### 🚀 deploy-render
**Render.com Deployment Standards**
- Environment configuration
- Database migration workflows
- Cron jobs and background tasks
- Health checks and monitoring
- Log management

## Installation

### Using OpenSkills CLI

```bash
# Install OpenSkills globally
npm i -g openskills

# Install this skills library
openskills install your-org/saas-skills

# Sync to your project's AGENTS.md
openskills sync
```

### Manual Installation

```bash
# Clone into your project's skills directory
git clone https://github.com/your-org/saas-skills.git .claude/skills/saas-skills

# Or for universal installation (Claude Code + other agents)
git clone https://github.com/your-org/saas-skills.git .agent/skills/saas-skills
```

## Usage

Once installed, AI agents will automatically discover and use these skills when relevant. You can also explicitly invoke them:

```bash
# Via OpenSkills CLI
openskills read rtl-ui
openskills read arabic-localization

# Via Claude Code (if using native skills)
# Skills are automatically invoked based on context
```

## Skill Invocation Examples

**RTL UI Development:**
```
"Create a dashboard with RTL support for Arabic users"
→ Agent automatically loads rtl-ui skill
```

**Arabic Localization:**
```
"Add Arabic translations in Najdi dialect for the checkout flow"
→ Agent loads arabic-localization skill with tone guidance
```

**Authentication Setup:**
```
"Set up Supabase authentication with custom email templates"
→ Agent loads auth-supabase skill
```

**Deployment:**
```
"Deploy this app to Render with database migrations"
→ Agent loads deploy-render skill
```

## Directory Structure

```
saas-skills/
├── README.md
├── rtl-ui/
│   └── SKILL.md
├── arabic-localization/
│   ├── SKILL.md
│   └── tone-examples.md
├── auth-supabase/
│   ├── SKILL.md
│   └── templates/
│       └── email-templates.md
└── deploy-render/
    └── SKILL.md
```

## Contributing

To add new skills or improve existing ones:

1. Create a new directory with a `SKILL.md` file
2. Follow the [OpenSkills format](https://github.com/anthropics/skills)
3. Include YAML frontmatter with `name` and `description`
4. Write concise, actionable instructions
5. Test with AI agents to verify effectiveness

## Best Practices

- **Conciseness**: Only include information AI agents don't already know
- **Progressive Disclosure**: Split large skills into multiple files
- **Clear Naming**: Use gerund form (verb + -ing) for skill names
- **Specific Descriptions**: Include what the skill does AND when to use it
- **Third Person**: Always write descriptions in third person

## Compatibility

✅ Claude Code
✅ OpenAI Codex CLI
✅ Cursor
✅ Windsurf
✅ Aider
✅ Any agent supporting the OpenSkills standard

## Security

Skills in this repository are designed for trusted development environments. Always review skill contents before use, especially if executing bundled scripts.

## License

MIT License - feel free to use and modify for your projects.

## Support

For issues or questions:
- Open an issue in this repository
- Reference the [OpenSkills documentation](https://github.com/numman-ali/openskills)
- Check [Anthropic's skills guide](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview)

---

**Built with ❤️ for standardized SaaS development workflows**