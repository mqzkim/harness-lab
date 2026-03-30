---
name: lab-sync
description: Supabase DB에서 지식 항목·시뮬레이션 결과를 추출하여 data/ 하위 JSON으로 동기화하고 harness-lab 레포에 커밋한다. knowledge, simulation, debate 요청 시 사용한다.
user-invocable: true
argument-hint: "[knowledge|simulations|all]"
allowed-tools: Read, Write, Edit, Bash, Glob, Grep
---

# Lab Sync

helix-co Supabase DB → harness-lab/data/ JSON 동기화.

## 실행 절차

### Step 1: 대상 파악

`$ARGUMENTS`에서 동기화 대상을 파악한다.
인수 없으면 → `all` 로 처리한다.

### Step 2: 데이터 추출

| 대상 | Supabase 테이블 | 출력 파일 |
|------|----------------|----------|
| knowledge | knowledgeEntries | data/knowledge.json |
| simulations | simulations | data/simulations.json |

### Step 3: JSON 생성 (Knowledge 특수 처리)

knowledge.json의 `graph` 섹션:
- `nodes`: 각 지식 항목을 노드로 (id, label, category, scope)
- `edges`: 태그 기반 연결 (같은 태그 → edge)

### Step 4: 커밋·푸시

```bash
git add data/
git commit -m "sync: <대상> 동기화 (<날짜>)"
git push origin main
```
