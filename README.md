# Rizz · Prototype

AI 데이팅 앱 **Rizz** 의 카톡-네이티브 풀 플로우 프로토타입입니다.

## 🎯 메인 파일

**→ [`app/HomeFriends_FlowB_A.html`](app/HomeFriends_FlowB_A.html) ←** 이거 하나만 열면 전체 플로우 작동합니다.

브라우저에서 직접 열기 (clone 후):
```
ui_kits/app/HomeFriends_FlowB_A.html
```

## 📱 전체 플로우

```
Welcome
   ↓
┌─ 현수 카톡 단일 스트림 ─────────────┐
│  1. 캐릭터 사진 5장 순차 도착 → 탭 선택 │
│  2. 분위기 (로맨스 / 자극적)          │
│  3. 필요한 것 (8개 칩 다중 선택)       │
│  4. 이름 입력                         │
│  5. 생년월일                          │
│  6. 내 성별                           │
│  7. 상대방 성별                        │
│  8. "유서현이랑 잠깐 만나보기" CTA     │
└──────────────────────────────────┘
   ↓
유서현 풀스크린 VN 스토리
  (사무실 → 메신저 → 벚꽃길 → 엔딩)
   ↓
홈 (현수 카톡 이어서)
  5명 추천 — 2명 노출 + 3~5명 블러 잠금
  각 추천: 괜찮은데?/난 별로
  괜찮은데? → 해당 캐릭터로 VN 진입
  └─ 유서현 (풀 스토리)
  └─ 이서윤 (옆집 누나 재회)
  └─ 아영/미유/하린 (첫 만남 제네릭)
   ↓
"10코인 내고 5명 더 보기" CTA
```

모든 온보딩 단계 우상단 **건너뛰기** 버튼 상시 작동.

## 🗂 구조

```
ui_kits/
├── app/
│   └── HomeFriends_FlowB_A.html   ← 메인 ✨ (이것만 열면 됨)
├── assets/
│   ├── seohyun/      유서현 자산 (배경 5 + 영상 6 + 메신저 1)
│   ├── seoyoon/      이서윤 자산 (22 이미지 — 배경/베이스/변형/구도/사진)
│   ├── videos/       일반 캐릭터 영상 (01~05.mp4)
│   └── images/       coin.png
└── colors_and_type.css   Rizz 디자인 시스템 토큰
```

## 🎨 디자인 시스템

- **브랜드 오렌지**: `#FF5E19`
- **그라데이션**: `linear-gradient(180deg, #FF3419 0%, #FF5E19 69%)`
- **폰트**: Pretendard Variable
- **바텀 네비**: 홈 / 코인 / 데이트(active) / 달성 기록 / 마이페이지 — [Figma 2477:12940 스펙]

## 🧪 로컬에서 열기

1. `git clone https://github.com/crlee-dotcom/prototype.git`
2. `cd prototype`
3. `app/HomeFriends_FlowB_A.html` 을 브라우저에서 열기 (더블클릭)

영상 경로가 상대 경로라 폴더 구조 그대로 유지해야 정상 재생됩니다.

---

*카톡-네이티브 온보딩 · VN 스토리 엔진 · Rizz DS 기반*

> 이전 실험 프로토타입(HomeTikTok, HomeStoriesGrid, Story, App 등)은 git history에서 확인 가능.
