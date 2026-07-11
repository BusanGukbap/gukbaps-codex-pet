# Vesper Codex Pet

Vesper is a curious violet moon-drake Codex pet with moth wings and a glowing leaf-tail.

## Files

- `pet.json` - Codex pet manifest
- `spritesheet.webp` - pet spritesheet asset

## Install

Copy these files into your Codex pets directory:

```powershell
$target = "$env:USERPROFILE\.codex\pets\vesper"
New-Item -ItemType Directory -Force -Path $target
Copy-Item .\pet.json "$target\pet.json" -Force
Copy-Item .\spritesheet.webp "$target\spritesheet.webp" -Force
```

Restart Codex if the pet does not appear immediately.
