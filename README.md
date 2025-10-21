# Sewercide CTF Banner

Banner event package for the Sewercide CTF Challenge.

## Package Type

This is an **event** type Deputy package that displays the challenge briefing banner to participants when the exercise starts.

## Description

Provides the introductory banner text for the Sewercide Plumbing CTF challenge, welcoming participants and outlining the challenge objectives.

## Usage

This package is referenced in the SDL file as an inject that triggers at the start of the exercise:

```yaml
injects:
  intro-banner:
    source:
      name: sewercide-ctf-banner
      version: 0.1.0
    from-entity: target
    to-entities:
      - participant
    description: "Challenge briefing and instructions"
```

## Version

Current version: **0.1.0**

## License

MIT
