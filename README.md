# Vesper Codex Pet

Vesper is a Codex pet themed as a curious violet moon-drake. The character combines small draconic features with broad moth-like wings and a softly glowing leaf-shaped tail, giving it a nocturnal, fantasy-inspired look without relying on external assets or services.

Vesper는 호기심 많은 보랏빛 달의 드레이크를 테마로 한 Codex 펫입니다. 작은 드래곤의 모습에 나방처럼 넓은 날개와 은은하게 빛나는 잎사귀 모양의 꼬리를 더해, 별도 자산이나 서비스 없이도 밤의 판타지 분위기를 냅니다.

## About Vesper

The pet is identified internally as `vesper` and appears in Codex as **Vesper**. Its visual definition is packaged as a single spritesheet so the pet can be installed by copying the repository files into the local Codex pets directory.

펫의 내부 ID는 `vesper`이며 Codex에는 **Vesper**로 표시됩니다. 시각 정보는 하나의 spritesheet에 담겨 있어, 저장소의 파일을 로컬 Codex 펫 폴더에 복사하면 설치할 수 있습니다.

The included manifest currently uses sprite version `2`. Keep `pet.json` and `spritesheet.webp` together with their original filenames: the manifest resolves the asset through `spritesheetPath`, so renaming or separating the files prevents Codex from finding the artwork.

현재 매니페스트는 sprite version `2`를 사용합니다. `pet.json`과 `spritesheet.webp`는 원래 이름 그대로 같은 폴더에 두세요. 매니페스트가 `spritesheetPath`로 자산을 찾기 때문에 파일 이름을 바꾸거나 분리하면 Codex가 이미지를 찾지 못합니다.

## Files

- `pet.json` - Codex pet manifest. Defines the pet ID, visible name, description, sprite version, and the relative path to the spritesheet.
- `pet.json` - 펫 ID, 표시 이름, 설명, 스프라이트 버전, spritesheet의 상대 경로를 정의하는 Codex 펫 매니페스트입니다.
- `spritesheet.webp` - Vesper's complete visual asset. Codex reads this file according to the sprite version declared in the manifest.
- `spritesheet.webp` - Vesper의 전체 시각 자산입니다. Codex는 매니페스트에 선언된 스프라이트 버전에 따라 이 파일을 읽습니다.

## Install

Copy these files into your Codex pets directory:

다음 파일을 Codex 펫 디렉터리에 복사합니다.

```powershell
$target = "$env:USERPROFILE\.codex\pets\vesper"
New-Item -ItemType Directory -Force -Path $target
Copy-Item .\pet.json "$target\pet.json" -Force
Copy-Item .\spritesheet.webp "$target\spritesheet.webp" -Force
```

Restart Codex if the pet does not appear immediately. If it still does not appear, confirm that the final folder is `%USERPROFILE%\.codex\pets\vesper` and that both files are present directly inside it, rather than in an additional nested folder.

펫이 바로 표시되지 않으면 Codex를 다시 시작하세요. 그래도 보이지 않으면 최종 폴더가 `%USERPROFILE%\.codex\pets\vesper`인지, 두 파일이 한 단계 더 깊은 하위 폴더가 아니라 그 폴더 바로 아래에 있는지 확인하세요.

## Compatibility

This repository contains only Vesper's local pet definition and artwork. It does not modify Codex settings, hooks, skills, or any other user configuration. Use a Codex version that supports local pets and retain the original `spriteVersionNumber` unless you also replace the artwork with an asset built for another sprite format.

이 저장소에는 Vesper의 로컬 펫 정의와 이미지 파일만 들어 있습니다. Codex 설정, 훅, 스킬, 기타 사용자 설정은 바꾸지 않습니다. 다른 스프라이트 형식으로 만든 이미지를 함께 교체하지 않는 한 원래 `spriteVersionNumber` 값도 유지하세요.
