# 👋 안녕하세요, grapefruit0205입니다.

### AI 에이전트 · LLM 인프라 최적화 · 오픈소스 기여

AI 에이전트 시스템과 LLM 인프라의 실행 효율성을 높이는 데 관심이 있습니다.

오픈소스 프로젝트에서 발생하는 병목과 오류를 분석하고,
**프롬프트 캐싱·모델 라우팅·런타임 안정성**을 개선하거나
벤치마크 분석을 바탕으로 아키텍처 개선 방향을 제안하고 있습니다.

---

## 🌍 오픈소스 기여 활동

### 🔹 [ClaudeRipple](https://github.com/PBJ-2/clauderipple)
**AI 모델 라우팅 및 개발 인프라**

#### ⚡ 프롬프트 캐시 최적화

- 요청마다 변경되는 빌링 헤더로 인해 프롬프트 캐시가 무효화되는 원인 분석
- Anthropic 호환 API의 프리픽스 캐싱(Prefix Caching) 정상 동작 복구
- 수정 후 일부 후속 요청에서 **98.9~99.4% 캐시 적중률** 관측
- 불필요한 프롬프트 재처리를 줄여 캐시 효율 개선

📌 [PR #37 — 병합 완료](https://github.com/PBJ-2/clauderipple/pull/37)

#### 🐧 Linux 환경 지원 및 플랫폼 호환성 확장

- `systemd` 사용자 서비스를 활용한 Linux 백그라운드 실행 환경 지원
- Linux 환경의 모델 선택 기능 개선
- NSS 인증서 신뢰 체계 적용을 통한 호환성 개선
- Linux 플랫폼 지원 범위 확장

📌 [PR #33](https://github.com/PBJ-2/clauderipple/pull/33) · [PR #34 — 병합 완료](https://github.com/PBJ-2/clauderipple/pull/34)

#### 🔧 세션 연속성 및 모델 호환성 개선

- 도구(Tool) 실행 이후 대화 컨텍스트가 유실되는 문제 수정
- Anthropic 호환 모델 제공자 처리 로직 개선
- 멀티턴 대화 환경에서의 세션 연속성 및 안정성 강화

📌 [PR #32 — 병합 완료](https://github.com/PBJ-2/clauderipple/pull/32)

#### 🛡️ 테스트 환경 격리 및 설치 안정성 개선

- 자동화 테스트 실행 시 실제 사용자 설정이 변경되지 않도록 테스트 환경 격리
- 설치 과정의 안정성 개선
- 라우터 상태 확인 및 실행 준비 상태 검증 로직 개선

📌 [PR #30 — 병합 완료](https://github.com/PBJ-2/clauderipple/pull/30) · [PR #31](https://github.com/PBJ-2/clauderipple/pull/31)

---

### 🔹 [Mixdog](https://github.com/tribgames/mixdog)
**AI 에이전트 하네스 및 런타임 최적화**

#### 🐛 세션 재시도 및 모델 전환 오류 수정

- 모델 전환 및 세션 재시도 과정에서 발생하는 IPC 검증 불일치 문제 분석
- 검증 규칙 수정을 통한 세션 재시도 오류 해결
- 동일 문제의 재발을 방지하기 위한 회귀 테스트(Regression Test) 추가

📌 [PR #37 — 병합 완료](https://github.com/tribgames/mixdog/pull/37)

#### 📊 에이전트 실행 효율성 및 비용 구조 분석

- 벤치마크 데이터를 바탕으로 에이전트 실행 실패 원인 및 비용 구조 분석
- 전체 벤치마크 비용의 **36%가 실패 관련 실행에서 발생**한다는 문제 확인
- 반복적인 실패 실행으로 인한 불필요한 추론 비용과 실행 오버헤드 분석
- **Stuck Detection(진행 정체 감지)** 및 **Adaptive Reasoning(적응형 추론)** 전략 제안
- 메인테이너가 관련 실행 정책 및 추론 강도 조정 일부 반영

📌 [Issue #38 — 벤치마크 분석 및 개선 제안](https://github.com/tribgames/mixdog/issues/38)

---

## 🛠️ 관심 분야

- 🤖 **AI Agents & Agentic Workflows**
  - AI 에이전트 실행 구조 및 워크플로 자동화

- ⚡ **LLM 성능 및 비용 최적화**
  - 토큰 효율화, 추론 비용 절감 및 실행 병목 분석

- 🔄 **모델 라우팅 및 프롬프트 캐싱**
  - 프리픽스 캐싱, 캐시 재사용 및 다중 모델 라우팅

- 🧩 **AI 에이전트 하네스 및 런타임**
  - 에이전트 실행 안정성, 세션 연속성 및 상태 관리

- ☁️ **클라우드 인프라**
  - 시스템 아키텍처, 서비스 운영 및 배포 환경

- 🔧 **개발 도구 및 자동화**
  - 테스트 환경 격리, 개발 생산성 및 검증 자동화

- 🌍 **오픈소스 개발**
  - 실제 사용 환경 기반의 이슈 분석 및 코드 기여

---

## 📊 GitHub 활동

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=grapefruit0205&show_icons=true&hide_border=true)

---

## 🔗 링크

- [GitHub 프로필](https://github.com/grapefruit0205)
- [전체 Pull Request 기여 내역](https://github.com/pulls?q=is%3Apr+author%3Agrapefruit0205)
- [ClaudeRipple 기여 내역](https://github.com/PBJ-2/clauderipple/pulls?q=is%3Apr+author%3Agrapefruit0205)
- [Mixdog 기여 내역](https://github.com/tribgames/mixdog/pulls?q=is%3Apr+author%3Agrapefruit0205)
