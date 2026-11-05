# 몬스터북 에셋

「몬스터북 · 교과 액션 RPG」가 실행 중에 받아 가는 3D 모델입니다.
게임은 이 저장소의 루트에서 `<이름>.glb` 로 바로 받아 갑니다.

```
https://cdn.jsdelivr.net/gh/fistluck-lgtm/monsterbook-assets@main/<이름>.glb
```

**이 저장소는 public 이어야 합니다.** private 이면 jsDelivr·raw.githubusercontent 가
학생 브라우저에 파일을 내려주지 못해 모델이 하나도 보이지 않습니다.

## 들어 있는 것

| 묶음 | 파일 | 출처 | 라이선스 |
|---|---|---|---|
| 몹 30 · 보스 10 | `mob_*.glb` · `boss*.glb` | Quaternius — Ultimate Monsters Pack | CC0 / CC-BY 4.0 |
| 플레이어 4 | `player_*.glb` | Kay Lousberg — KayKit Adventurers | CC0 |
| 탈것 4 | `mount_*.glb` | Quaternius — Animated Animals | CC0 |
| 건물·나무·바위 12 | `bld_*` `wld_*` `temple` `lmk_*` `wall_*` | Kay Lousberg — KayKit Medieval Hexagon | CC0 |

플레이어는 원본 그대로입니다. 무기·투구·망토가 모델 안에 들어 있어서,
게임 쪽 표(`PLAYER_GLB`)의 `hide` 목록으로 직업에 맞지 않는 것만 끕니다.
`player_cleric.glb` 는 `player_mage.glb` 와 같은 파일이며, 끄는 조각이 달라
고깔과 큰 지팡이 대신 펼친 법서와 완드를 듭니다.

몬스터 묶음은 한 덩어리로 된 원본(50마리)을 종마다 따로 떼어 낸 것입니다.
떼어 내면서 바깥을 감싸던 Y-up 보정 행렬은 살리고, 진열용으로 주어졌던
위치·회전은 떼어 냈습니다. 동작은 원본에 하나로 뭉쳐 있던 것을 노드별로 갈라
`idle` 이라는 이름으로 넣었습니다.

## 출처 표기

- **Quaternius** (https://quaternius.com) — Ultimate Monsters Pack · Animated Animals (탈것 넷, Idle·Walk·Gallop 만 남김)
- **Kay Lousberg** (https://kaylousberg.com) — KayKit Adventurers · Medieval Hexagon (`LICENSE-KayKit.txt`)

Medieval Hexagon 묶음은 원본이 `.gltf` + `.bin` + 공용 텍스처로 나뉘어 있어서,
게임이 주소 하나로 받아 갈 수 있도록 `.glb` 한 덩어리로 묶었습니다.

두 분 모두 개인·교육·상업적 사용을 허락하고 있습니다. KayKit 은 출처 표기를
요구하지 않지만 남겨 둡니다.
