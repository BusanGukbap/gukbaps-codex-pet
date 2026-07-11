# Vesper Codex Pet

Vesper is a Codex pet themed as a curious violet moon-drake. The character combines small draconic features with broad moth-like wings and a softly glowing leaf-shaped tail, giving it a nocturnal, fantasy-inspired look without relying on external assets or services.

## About Vesper

The pet is identified internally as `vesper` and appears in Codex as **Vesper**. Its visual definition is packaged as a single spritesheet so the pet can be installed by copying the repository files into the local Codex pets directory.

The included manifest currently uses sprite version `2`. Keep `pet.json` and `spritesheet.webp` together with their original filenames: the manifest resolves the asset through `spritesheetPath`, so renaming or separating the files prevents Codex from finding the artwork.

## 한국어 안내

Vesper는 밤의 분위기를 담은 Codex 펫입니다. 작은 드래곤의 모습에 나방처럼 넓은 날개와 은은하게 빛나는 잎사귀 모양의 꼬리를 더했습니다. Codex에서는 `Vesper`로 표시되며, 내부 ID는 `vesper`입니다.

펫 이미지는 하나의 spritesheet에 담겨 있습니다. `pet.json`은 이름, 설명, 스프라이트 버전, 이미지 파일 경로를 담은 매니페스트이고, `spritesheet.webp`에는 Vesper의 이미지가 들어 있습니다. 두 파일은 이름을 바꾸지 말고 같은 폴더에 두어야 합니다. `pet.json`이 `spritesheet.webp`를 상대 경로로 찾기 때문입니다.

설치할 때는 두 파일을 `%USERPROFILE%\.codex\pets\vesper` 폴더 바로 아래에 복사합니다. Codex를 다시 시작한 뒤에도 보이지 않으면 파일이 한 단계 더 깊은 폴더에 들어가 있지 않은지 확인하세요.

이 저장소에는 Vesper의 펫 정의와 이미지 파일만 들어 있습니다. Codex 설정, 훅, 스킬, 기타 사용자 설정은 바꾸지 않습니다. 스프라이트 형식이 다른 이미지를 쓰지 않는 한 `spriteVersionNumber` 값도 그대로 두는 편이 좋습니다.

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
