# harness-lab

Research 부서 데이터 저장소 — 지식 그래프, 시뮬레이션/토론.

## 구조

```
harness-lab/
├── .claude/           # harness-infra 기반
├── data/
│   ├── meta.json      # 부서 메타
│   ├── knowledge.json # 지식 항목 + 그래프 데이터
│   └── simulations.json # 시뮬레이션/토론 결과
└── config/
    └── department.json
```

## helix-co 대시보드 페이지

| 페이지 | 경로 | 데이터 파일 |
|--------|------|-----------|
| Knowledge Graph | /knowledge-graph | knowledge.json |
| Simulations | /simulations | simulations.json |
