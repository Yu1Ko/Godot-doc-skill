# Godot 4.7 Documentation Skill

A Codex skill that requires live verification against the official
[Godot Engine 4.7 documentation](https://docs.godotengine.org/en/4.7/) before
answering or implementing Godot technical tasks.

It covers scene and node capabilities, inheritance, GDScript APIs, properties,
methods, signals, resources, UI, physics, animation, navigation, rendering,
editor behavior, import/export, debugging, and migration questions.

## Install

Clone the repository into your Codex skills directory:

```powershell
git clone https://github.com/Yu1Ko/Godot-doc-skill.git "$HOME/.codex/skills/godot-docs"
```

## Use

Invoke it explicitly with `$godot-docs`, or let Codex trigger it for relevant
Godot technical work.

Example:

```text
Use $godot-docs to verify which CharacterBody2D APIs should be used for this movement code.
```
