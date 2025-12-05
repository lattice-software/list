# Lattice QFT Software List

**[View List →](https://lattice-software.github.io/list)**

Community-curated list of useful software and repositories for lattice quantum field theory.


## How to Contribute

You can either contribute to the repository directly (commit or pull request), or add an issue with new entries or corrections.

### Adding a New Entry

Create a new YAML file in `src/data/entries/`.

**Filename rules:**
- Use lowercase
- Use hyphens for spaces (e.g., `my-software.yaml`)
- No special characters except hyphens

### Entry Structure

Each entry file should contain a YAML object with the following fields:

- `title`: Name of the software or resource
- `description`: Brief description (one sentence, can span multiple lines in YAML)
- `links`: Array of link objects, each with:
  - `title`: Link label (e.g., "Repository", "Documentation", "Paper")
  - `url`: Full URL
- `tags`: Array of tags (strings)
- `category`: Category string (see below)

**Note:** The `id` field is automatically derived from the filename, so don't include it in the YAML.

Example: Create `src/data/entries/example-software.yaml`:

```yaml
title: Example Software
description: A useful tool for lattice calculations
links:
  - title: Repository
    url: https://github.com/example/software
  - title: Documentation
    url: https://example.com/docs
tags:
  - qcd
  - c++
  - gpu
category: simulation
```

### Categories vs Tags

The intention is that **categories** are high-level types that classify what the software/resource is, each entry should have one.
**Tags** are specific attributes that describe technical details, capabilities, or domains.
There is no strict list of tags; new tags can just be added as needed by putting them in the `tags` array.

### Recommendations

1. **Links**: Always include a "Repository" link if available.
   The title will automatically link to the repository.

2. **Tags**: Be consistent with existing tags.
   Check the current tags in the YAML file before adding new ones.

3. **Description**: Keep it concise (one sentence).
   Focus on what the software does.

4. **Filename**: Use lowercase, hyphenated filenames that match the software name.
   The filename becomes the entry ID automatically.

5. **Multiple links**: You can add multiple links (Repository, Documentation, Paper, Tutorial, etc.).
   All will be displayed in the card footer.

6. **One file per entry**: Each entry gets its own YAML file.
   This makes it easier to manage and avoids merge conflicts.

## Development

For installation and development instructions, see [README-SETUP.md](README-SETUP.md).
