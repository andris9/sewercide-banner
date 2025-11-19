# Sewercide CTF Challenge Banner - Reference Deputy Banner Package

**GitHub Repository:** [github.com/andris9/sewercide-banner](https://github.com/andris9/sewercide-banner)

## Purpose

This Deputy banner package serves as a **reference example** for creating challenge briefing banners for Open Cyber Range exercises. It demonstrates how to structure participant-facing content that provides context, objectives, and guidance without revealing solutions.

## Package Type: Banner

Banner packages are a special type of Deputy package that displays HTML content to participants in the OCR platform UI. They're designed to:

- Provide challenge briefing and scenario context
- Explain objectives and success criteria
- Give environment and access information
- Offer hints and methodology guidance without spoilers
- Use template variables for personalization

## Package Structure

```
sewercide-banner/
├── package.toml          # Deputy banner package configuration
├── README.md             # This file (documentation)
└── src/
    └── content           # HTML banner content with template variables
```

## Banner Content

The `src/content` file contains HTML that is displayed to participants when they access the exercise.

## Template Variables

OCR uses nunjucks syntax and automatically replaces these placeholders with actual values:

| Variable               | Description            | Example                   |
| ---------------------- | ---------------------- | ------------------------- |
| `{{ exerciseName }}`   | Exercise name from SDL | "Sewercide CTF Challenge" |
| `{{ deploymentName }}` | Deployment instance ID | "sewercide-prod-001"      |
| `{{ username }}`       | Participant username   | "student123"              |

## Styling Guidelines

### Inline CSS Required

Since banners render in OCR's platform UI, all styling must be inline CSS (no external stylesheets).

## Using as Reference

1. Copy this package structure as template
2. Update `package.toml` name and description
3. Edit `src/content` with your challenge scenario
4. Keep template variables for personalization
5. Maintain inline CSS styling
6. Publish using `deputy publish`

## Publishing

To publish this banner package:

```bash
# 1. Update version in package.toml
# 2. Publish to Deputy registry
deputy publish
```

## License

MIT License - Free to use as reference for your own OCR exercise banners.

## Author

Andris <andris@postalsys.com>
