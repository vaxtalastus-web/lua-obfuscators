<h1 align="center">Contributing</h1>

## 1. Fork this repository

Click the **Fork** button at the top-right of the GitHub page.

## 2. Clone your fork

```bash
git clone https://github.com/spxnso/lua-obfuscators.git
cd lua-obfuscators
```

## 3. Create a branch

Always create a new branch for your changes.
Example:

```bash
git checkout -b my-obfuscator
```

## 4. Add your contribution

Each obfuscator should be added in the following structure:

```python
obfuscators/
  <obfuscator-slug>/
    README.md           # obfuscator description (macros, settings, ...)
    versions/
      v1.0.0/
        README.md       # version-specific notes
        samples/
            sample.obf.lua
```

Tip: Keep filenames lowercase and hypen-separated

### Obfuscated file header (required)

Each obfuscated file should start with a header comment that documents provenance and intent. Use Lua comment syntax (`--[[`) and include at least these fields:

```lua
--[[
    filename: sample.obf.lua
    source: <link>
    obfuscator: <obfuscator-slug> vX.Y.Z
    author: Bob <bob@example.com> (@bob-github)
    purpose: Print demonstration
    notes: ...
    lua-version: Lua 5.1.5
    license: MIT
]]--
```

## 5. Commit your changes

```bash
git add .
git commit -m "Add <obfuscator-slug> vX.Y.Z"
```

## 6. Push your branch

```bash
git push origin my-obfuscator
```

## 7. Open a Pull Request

- Go to your fork on Github
- Click Compare & Pull Request.
- Include:
  - Obfuscator name & version
  - Support Lua / Luau versions
  - Sample outputs
  - Source URL or license info
- Ensure your PR follows the [Code of Conduct](/CODE_OF_CONDUCT.md)

## 8. Review and feedback

- Mainteners may ask for clarifications or minor adjustments
- Respond politely and make the requested changes in your branch
- Once approved, your contribution will be merged
  
## 9. Thank you!
By contributing, you help mainain a safe and well-organized Lua & Luau obfuscator catalog
