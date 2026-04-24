# 테스트용 저장소 입니다.



## 🚀 협업 가이드

### 브랜치 전략
main: 팀장만 푸시 (PR 승인 후 머지)  
develop: 개발 브랜치 (PR 대상 추천)

- feature/기능명 (ex: feature/inventory-api)
- fix/버그명 (ex: fix/db-connection)  
- docs/문서명 (ex: docs/architecture)
- hotfix/긴급

**작업 순서:**
1. git checkout -b feature/내기능명
2. 작업 후 git push origin feature/내기능명
3. GitHub에서 PR 생성 (템플릿 자동 적용)
4. 팀장 리뷰 → 승인 → main 머지

### 커밋 컨벤션
type: 설명 (50자 이내, 한글 OK)

- feat: 재고관리 API 구현
- fix: 로그인 오류 수정
- docs: README 업데이트
- test: 단위테스트 추가
- chore: 환경설정 변경

❌ "작업완료" ❌ "버그수정"
✅ "feat: 주문관리 페이지 추가"프로젝트 파이팅
