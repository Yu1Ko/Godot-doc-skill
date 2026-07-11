---
name: godot-docs
description: Search and verify the official Godot Engine 4.7 documentation before answering or implementing Godot technical tasks. Use for Godot projects and files such as project.godot, .gd, .tscn, and .tres; scene and node design; GDScript syntax and exposed APIs; properties, methods, signals, resources, UI, physics, animation, navigation, rendering, editor behavior, import/export, debugging, or version migration.
---

# Godot 4.7 Documentation

Use the official Godot 4.7 documentation as the source of truth for engine behavior and API details.

## Required workflow

1. Identify the exact Godot concepts involved: class names, node types, GDScript symbols, subsystems, error text, and desired behavior.
2. Before answering or editing code, perform at least one live documentation search scoped to `https://docs.godotengine.org/en/4.7/`.
   - Prefer an internet search such as `site:docs.godotengine.org/en/4.7/ <Godot terms>`.
   - Alternatively use `https://docs.godotengine.org/en/4.7/search.html?q=<terms>` in an interactive browser.
   - Search with English Godot identifiers. Translate non-English requests into likely class and API names, and try additional terms when the first search is ambiguous.
   - Opening only the documentation homepage does not count as a search.
3. Open the most relevant official pages and read the sections needed for the task.
   - For a node or engine class, open its class reference under `/en/4.7/classes/`.
   - Check the parent class when behavior, properties, methods, or signals are inherited.
   - Open the relevant tutorial page when the task depends on a workflow or recommended usage rather than a single API signature.
   - Search each important unknown instead of extrapolating from one loosely related page.
4. Extract only task-relevant facts: inheritance, capabilities, lifecycle, ownership or scene-tree behavior, exact method signatures, parameters, defaults, return types, properties, signals, enums, warnings, and documented limitations.
5. Apply the verified facts to the answer, diagnosis, design, or code change. Include direct links to the official 4.7 pages that materially support the result.

## Verification rules

- Keep all primary documentation links on `/en/4.7/`; do not silently substitute `stable`, `latest`, or another version.
- Inspect `project.godot` or other local evidence when the repository version matters. If it differs from 4.7, state the mismatch before relying on version-specific behavior.
- Distinguish classes, properties, methods, signals, annotations, and global functions precisely.
- Verify GDScript spelling and signatures instead of translating them from another language binding.
- Treat official class-reference notes and warnings as constraints, especially for lifecycle callbacks, deferred calls, threading, ownership, physics, and rendering behavior.
- Let current official documentation override remembered API details or third-party tutorials.
- If the official documentation is unavailable, say that the lookup could not be completed. Use a local installed class reference or official Godot source only as a clearly labeled fallback, and do not describe the result as documentation-verified.

## Common lookup patterns

- Scene or node capability: search the exact node name, then inspect its inheritance chain, properties, methods, signals, and linked tutorials.
- GDScript API: search the exact symbol plus its owning class, then confirm its signature and return behavior on the class reference page.
- Error or unexpected behavior: search the error text and involved API names, then verify lifecycle and usage notes before proposing a fix.
- Choosing between nodes or systems: search each candidate and compare documented responsibilities and limitations before recommending one.
