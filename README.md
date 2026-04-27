# 📦 CCmall: Omni-Backup by Team Cloud-crew☁️
> IaC 기반의 하이브리드 클라우드 데이터 자동 백업 및 복구 시스템 구축 

---

## 🛠 1. Tech Stack & Infrastructure
- **Language**: Python 3.11.7
- **Backend**: FastAPI 0.109.0
- **Database**: PostgreSQL 15 (Containerized)
- **Infrastructure as Code**: Terraform 1.5.7
- **Configuration Management**: Ansible 2.15.0
- **Cloud/Virtualization**: AWS / VMware Hybrid Cloud
- **Observability**: Prometheus, Grafana, Alertmanager (Slack Integration)
- **CI/CD**: GitHub Actions (Automated Docker Build & Deployment)

---

## 📁 2. Directory Structure
project/
├── app/                        # FastAPI 애플리케이션 (백엔드 로직)
│   ├── api/                    # API 엔드포인트 (customers, inventory, orders)
│   ├── core/                   # 시스템 설정 및 환경 변수 관리
│   ├── crud/                   # Database CRUD 로직
│   ├── models/                 # DB 테이블 스키마 정의
│   ├── schemas/                # 데이터 검증 및 직렬화 (Pydantic)
│   ├── services/               # 외부 서비스 연동 (S3, 메시지 전송 등)
│   ├── tasks/                  # 백업 스케줄러 (APScheduler)
│   └── main.py                 # 애플리케이션 엔트리포인트
├── infra/                      # 인프라 및 운영 레이어
│   ├── terraform/              # IaC 기반 AWS 리소스 관리
│   ├── ansible/                # OS 설정 및 패키지 배포 자동화
│   ├── monitoring/             # Prometheus, Grafana 관찰 체계
│   └── automation/             # 장애 대응(Failover) 및 복구 스크립트
├── cicd/                       # GitHub Actions 파이프라인 설정
├── docker/                     # 컨테이너 빌드 및 오케스트레이션 설정
├── docs/                       # 기술 설계서 및 아키텍처 다이어그램
└── requirements.txt            # 파이썬 의존성 패키지 명세
---

## 📅 3. Operational Process (SOP)

### 3.1 Agile Development Workflow
- **Sprint Planning**: 주차별 마일스톤 수립 및 기술 스택 확정
- **Daily Scrum**: 매일 업무 대시보드 업데이트 및 담당자 배정
- **Local-First Development**: 컨테이너 기반 로컬 환경에서 선 검증 후 운영 서버 반영
- **Knowledge Sharing**: 일일 업무 종료 전 기술 공유 및 트러블슈팅 내역 문서화

### 3.2 System Reliability Strategy
- **Data Integrity**: APScheduler 기반의 S3 자동 백업 및 무결성 검증
- **Real-time Alerting**: 시스템 장애 및 백업 실패 시 Slack 실시간 알림 알림 연동
- **Disaster Recovery**: `automation/` 스크립트를 활용한 신속한 서비스 복구 체계 가동

---

## 🤝 4. Collaboration & Governance

### 4.1 Branch & PR Strategy (Git-Flow)
- **`master`**: 프로덕션 배포 브랜치 (Strictly Protected)
- **`feature/`**: 기능 단위 개발 브랜치
- **Code Review**: 모든 변경 사항은 팀장 승인(Approve) 후 Merge를 원칙으로 함
- **Documentation**: PR 작성 시 작업 상세, 테스트 결과, 관련 이슈 명시 필수

### 4.2 Commit Convention
- **feat**: 신규 기능 개발 및 로직 추가
- **fix**: 시스템 오류 및 버그 수정
- **docs**: 문서화 작업 (설계서, 가이드라인 등)
- **chore**: 의존성 관리 및 단순 환경 설정 변경
- **refactor**: 코드 구조 최적화 및 가독성 개선

---

## 📂 5. Asset Management
- **Project Tracking**: Notion (Roadmap & Meeting Logs)
- **Version Control**: GitHub (Source Code & IaC Scripts)
- **Technical Docs**: `docs/` (Architecture Diagram & API Specs)