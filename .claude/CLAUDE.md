# Research Department

지식 축적·시뮬레이션·토론 연구 데이터 관리.

## 라우팅

→ `routing.md`

## 참조

| 파일 | 내용 |
|------|------|
| `config/department.json` | 부서 설정 (색상, 스코프, 페르소나, 테이블 매핑) |
| `data/meta.json` | 동기화 상태 (last_sync, version) |
| `~/.claude/references/workspace-context.md` | 워크스페이스 전체 구조 |

## 데이터 흐름

```
Supabase DB → lab-sync skill → data/*.json → GitHub → helix-co /api/lab
```
