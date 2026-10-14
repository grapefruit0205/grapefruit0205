<div align="center">

# ⚡ Open Source Contributions

**AI Agents · LLM Infrastructure · Runtime Optimization**

![Open Source](https://img.shields.io/badge/Open_Source-Contributor-238636?style=flat-square)
![AI Agents](https://img.shields.io/badge/AI-Agents-5865F2?style=flat-square)
![LLM](https://img.shields.io/badge/LLM-Optimization-0969DA?style=flat-square)

</div>

---

# 🐕 Mixdog

### AI 에이전트 하네스 및 런타임 최적화

[![Repository](https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github)](https://github.com/tribgames/mixdog)
![Benchmark](https://img.shields.io/badge/Benchmark-Analysis-0969DA?style=flat-square)
![Optimization](https://img.shields.io/badge/Runtime-Optimization-7C3AED?style=flat-square)
![Merged](https://img.shields.io/badge/PR-Merged-238636?style=flat-square)

### 📌 주요 기여

| 분야 | 기여 내용 | 링크 |
|:---|:---|:---:|
| 📊 **Cost Analysis** | 벤치마크 실패 관련 비용 36% 분석 및 최적화 방향 제시 | [Issue #38](https://github.com/tribgames/mixdog/issues/38) |
| ⚡ **Optimization** | Stuck Detection 및 적응형 추론 전략 제안 | [Issue #38](https://github.com/tribgames/mixdog/issues/38) |
| 🐛 Bug Fix | IPC 검증 불일치 및 세션 재시도 오류 수정 | [PR #37](https://github.com/tribgames/mixdog/pull/37) |
| 🧪 Testing | 동일 오류 재발 방지를 위한 회귀 테스트 추가 | [PR #37](https://github.com/tribgames/mixdog/pull/37) |

<details>
<summary><b>🔍 기술적 기여 상세 보기</b></summary>

<br>

## 1. 📊 에이전트 실행 효율성 및 비용 구조 분석

벤치마크 데이터를 기반으로 에이전트의 실행 실패 원인과 비용 발생 구조를 분석하고, 불필요한 추론 비용을 줄이기 위한 개선 방향을 제안했습니다.

**주요 분석 및 제안**

- 벤치마크 결과를 기반으로 에이전트 실행 실패 원인과 비용 구조 분석
- 전체 벤치마크 비용의 **36%가 실패 관련 실행에서 발생**한다는 문제 확인
- 반복적인 실패 실행으로 인한 불필요한 추론 비용 및 실행 오버헤드 분석
- **Stuck Detection(진행 정체 감지)** 전략 제안
- **Adaptive Reasoning(적응형 추론)** 전략 제안
- 메인테이너가 관련 실행 정책 및 추론 강도 조정 일부 반영

> **분석 결과**
>
> 전체 벤치마크 비용 중 실패 관련 실행이 차지하는 비중이 36%로 나타났으며,
> 이를 줄이기 위한 실행 제어 및 추론 최적화 전략을 제안했습니다.
>
> 36%는 비용 절감률이 아닌 분석 당시 실패 관련 실행에 사용된 비용 비중입니다.

**관련 자료**

📌 [Issue #38 — 벤치마크 분석 및 개선 제안](https://github.com/tribgames/mixdog/issues/38)

---

## 2. 🐛 세션 재시도 및 모델 전환 오류 수정

모델 전환 및 세션 재시도 과정에서 발생하는 IPC 검증 불일치 문제를 분석하고 수정했습니다.

**주요 변경 사항**

- IPC 검증 규칙 불일치 원인 분석
- 모델 전환 및 세션 재시도 오류 수정
- 검증 로직 개선
- 동일 문제의 재발을 방지하기 위한 회귀 테스트(Regression Test) 추가

**결과**

- 세션 재시도 과정의 오류 해결
- 검증 로직 안정성 개선
- 원본 프로젝트에 PR 병합 완료

📌 [PR #37 — 병합 완료](https://github.com/tribgames/mixdog/pull/37)

</details>

---

# 🌊 ClaudeRipple

### AI 모델 라우팅 및 LLM 개발 인프라

[![Repository](https://img.shields.io/badge/GitHub-Repository-181717?style=flat-square&logo=github)](https://github.com/PBJ-2/clauderipple)
![Caching](https://img.shields.io/badge/Prompt-Caching-0969DA?style=flat-square)
![Linux](https://img.shields.io/badge/Platform-Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Merged](https://img.shields.io/badge/PR-Merged-238636?style=flat-square)

### 📌 주요 기여

| 분야 | 기여 내용 | 링크 |
|:---|:---|:---:|
| ⚡ **Caching** | Anthropic 호환 API의 프롬프트 캐싱 복구 | [PR #37](https://github.com/PBJ-2/clauderipple/pull/37) |
| 🐧 **Linux** | systemd 기반 Linux 환경 지원 및 호환성 개선 | [PR #34](https://github.com/PBJ-2/clauderipple/pull/34) |
| 🔄 Session | 도구 실행 이후 대화 컨텍스트 유실 문제 수정 | [PR #32](https://github.com/PBJ-2/clauderipple/pull/32) |
| 🛡️ Testing | 테스트 환경 격리 및 사용자 설정 보호 | [PR #30](https://github.com/PBJ-2/clauderipple/pull/30) |
| 🔧 Reliability | 설치 안정성 및 라우터 상태 확인 개선 | [PR #31](https://github.com/PBJ-2/clauderipple/pull/31) |

<details>
<summary><b>🔍 기술적 기여 상세 보기</b></summary>

<br>

## 1. ⚡ 프롬프트 캐시 최적화

Anthropic 호환 API 환경에서 프롬프트 캐싱이 정상적으로 작동하지 않는 문제를 분석하고 수정했습니다.

**주요 변경 사항**

- 요청마다 변경되는 빌링 헤더로 인해 프롬프트 캐시가 무효화되는 원인 분석
- Anthropic 호환 API의 Prefix Caching 정상 동작 복구
- 캐시 재사용을 방해하는 요청 구조 개선
- 불필요한 프롬프트 재처리 감소

**검증 결과**

- 수정 후 일부 후속 요청에서 **98.9~99.4% 캐시 적중률 관측**
- 프롬프트 캐시 재사용 정상 동작 확인

> 캐시 적중률은 특정 후속 요청에서 관측된 수치이며,
> 전체 요청의 평균 캐시 적중률을 의미하지 않습니다.

📌 [PR #37 — 병합 완료](https://github.com/PBJ-2/clauderipple/pull/37)

---

## 2. 🐧 Linux 환경 지원 및 플랫폼 호환성 확장

기존 프로젝트의 Linux 환경 지원을 개선하고 실행 환경의 호환성을 확장했습니다.

**주요 변경 사항**

- `systemd` 사용자 서비스 기반 Linux 백그라운드 실행 환경 지원
- Linux 환경의 모델 선택 기능 개선
- NSS 인증서 신뢰 체계 적용
- Linux 플랫폼 호환성 확장

**결과**

- Linux 환경에서의 실행 및 설정 지원 확대
- 관련 변경 사항 원본 프로젝트에 반영

📌 [PR #33](https://github.com/PBJ-2/clauderipple/pull/33) · [PR #34 — 병합 완료](https://github.com/PBJ-2/clauderipple/pull/34)

---

## 3. 🔄 세션 연속성 및 모델 호환성 개선

도구 실행 이후 대화 컨텍스트가 유실되는 문제를 수정하고 멀티턴 세션의 안정성을 개선했습니다.

**주요 변경 사항**

- Tool 실행 이후 대화 컨텍스트 유실 문제 수정
- Anthropic 호환 모델 제공자 처리 로직 개선
- 멀티턴 대화 환경의 세션 연속성 개선

**결과**

- 도구 실행 이후 대화 연속성 개선
- 모델 호환성 및 세션 안정성 강화

📌 [PR #32 — 병합 완료](https://github.com/PBJ-2/clauderipple/pull/32)

---

## 4. 🛡️ 테스트 환경 격리 및 설치 안정성 개선

자동화 테스트 과정에서 실제 사용자 환경에 영향을 줄 수 있는 문제를 개선했습니다.

**주요 변경 사항**

- 자동화 테스트가 실제 사용자 설정을 변경하지 않도록 테스트 환경 격리
- 설치 과정의 안정성 개선
- 라우터 상태 확인 및 실행 준비 상태 검증 로직 개선

**결과**

- 테스트 환경의 독립성 강화
- 사용자 설정 보호
- 설치 및 실행 과정의 안정성 개선

📌 [PR #30 — 병합 완료](https://github.com/PBJ-2/clauderipple/pull/30) · [PR #31](https://github.com/PBJ-2/clauderipple/pull/31)

</details>

---

# 🛠️ 관심 분야

<div align="center">

![AI Agents](https://img.shields.io/badge/AI-Agents-5865F2?style=for-the-badge)
![LLM](https://img.shields.io/badge/LLM-Optimization-0969DA?style=for-the-badge)
![Caching](https://img.shields.io/badge/Prompt-Caching-238636?style=for-the-badge)

![Runtime](https://img.shields.io/badge/Agent-Runtime-7C3AED?style=for-the-badge)
![Linux](https://img.shields.io/badge/Linux-Environment-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Cloud](https://img.shields.io/badge/Cloud-Infrastructure-FF9900?style=for-the-badge)

![Automation](https://img.shields.io/badge/Developer-Automation-0A66C2?style=for-the-badge)
![Open Source](https://img.shields.io/badge/Open-Source-238636?style=for-the-badge)

</div>

---

# 📊 GitHub 활동

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=grapefruit0205&show_icons=true&hide_border=true&theme=github_dark)

</div>

---

<div align="center">

### 🔗 Contributions & Pull Requests

[![All Pull Requests](https://img.shields.io/badge/All-Pull_Requests-181717?style=for-the-badge&logo=github)](https://github.com/pulls?q=is%3Apr+author%3Agrapefruit0205)

[![Mixdog](https://img.shields.io/badge/Mixdog-Contributions-0969DA?style=flat-square&logo=github)](https://github.com/tribgames/mixdog/pulls?q=is%3Apr+author%3Agrapefruit0205)
[![ClaudeRipple](https://img.shields.io/badge/ClaudeRipple-Contributions-7C3AED?style=flat-square&logo=github)](https://github.com/PBJ-2/clauderipple/pulls?q=is%3Apr+author%3Agrapefruit0205)

</div>
