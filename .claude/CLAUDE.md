# Research Department

지식 축적·시뮬레이션·토론 연구 데이터 관리.

## 데이터 흐름

```
harness-lab/data/ → GitHub Raw API → helix-co /api/lab → Dashboard Pages
```

## 라우팅

→ `routing.md`

## 출력 규칙

- 모든 출력은 `data/` 하위 JSON 파일로 저장
- `meta.json`의 `last_sync` 필드를 항상 갱신
