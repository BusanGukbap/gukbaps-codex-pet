# Vesper Codex Pet

Vesper is a Codex pet themed as a curious violet moon-drake. The character combines small draconic features with broad moth-like wings and a softly glowing leaf-shaped tail, giving it a nocturnal, fantasy-inspired look without relying on external assets or services.

## About Vesper

The pet is identified internally as `vesper` and appears in Codex as **Vesper**. Its visual definition is packaged as a single spritesheet so the pet can be installed by copying the repository files into the local Codex pets directory.

The included manifest currently uses sprite version `2`. Keep `pet.json` and `spritesheet.webp` together with their original filenames: the manifest resolves the asset through `spritesheetPath`, so renaming or separating the files prevents Codex from finding the artwork.

## Files

- `pet.json` - Codex pet manifest. Defines the pet ID, visible name, description, sprite version, and the relative path to the spritesheet.
- `spritesheet.webp` - Vesper's complete visual asset. Codex reads this file according to the sprite version declared in the manifest.

## Install

Copy these files into your Codex pets directory:

```powershell
$target = "$env:USERPROFILE\.codex\pets\vesper"
New-Item -ItemType Directory -Force -Path $target
Copy-Item .\pet.json "$target\pet.json" -Force
Copy-Item .\spritesheet.webp "$target\spritesheet.webp" -Force
```

Restart Codex if the pet does not appear immediately. If it still does not appear, confirm that the final folder is `%USERPROFILE%\.codex\pets\vesper` and that both files are present directly inside it, rather than in an additional nested folder.

## Compatibility

This repository contains only Vesper's local pet definition and artwork. It does not modify Codex settings, hooks, skills, or any other user configuration. Use a Codex version that supports local pets and retain the original `spriteVersionNumber` unless you also replace the artwork with an asset built for another sprite format.
