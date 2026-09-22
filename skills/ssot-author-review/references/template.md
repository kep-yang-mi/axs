# <업무명> SSoT

> 상태: 초안 / 검토 중 / 승인됨
> 버전: | 기준일: | 적용 기간:
> 업무 책임자: | 데이터 소유자: | 승인권자:
> 관련 업무 표면: | 변경 이력 위치:

## 1. Desired Result — 완료 결과
- 만들어져야 하는 결과물:
- 완료 판단 기준:
- 결과물을 사용할 사람 / 시스템:

## 2. Entity — 상태를 가진 업무 대상
- Entity 이름 / 고유 식별자:
- 포함 범위 / 제외 범위:

## 3. State Model / Signal
| State | Meaning | Signal / Evidence | Owner |
|---|---|---|---|
| | | | |

## 4. Transition / Guard / Human Gate
| From | To | Action | Agent 역할 | Guard | Human Gate | 실패 시 처리 |
|---|---|---|---|---|---|---|
| | | | | | | |
- 정보 부족 / 반려 / 보류 / 재시도 분기:
- 승인 유효 범위와 실행 주체:

## 5. Data Foundation — 기준값
| 기준 시스템 / 문서 / 원장 | 소유자 | 버전 / 기준일 | 최신성 확인 | 우선순위 / 충돌 처리 |
|---|---|---|---|---|
| | | | | |
- 필수 필드 / 누락값 처리:
- 변경 이력:

## 6. Context Layer — 업무 의미
| Field / Document | Meaning | Entity | State / Transition | Exception |
|---|---|---|---|---|
| | | | | |

## 7. Access Layer — 접근과 실행 권한
| Data / Action | Agent Permission | Human Gate / 승인권자 | 실행 주체 | Audit / Verification |
|---|---|---|---|---|
| | read / draft / write with approval / blocked | | | |
- 접근 금지 데이터 / 민감정보 처리:
- 허용된 읽기 범위와 쓰기 범위:

## 8. Verification — 실행 후 재확인
- read-back 대상과 확인 위치:
- 기대 결과 / 합격 기준:
- diff / 승인 로그 / 결과 링크:
- 불일치 시 중단·수정·재검증 담당자:

## 9. Risks / Guardrails
- 개인정보 / 인사·평가 / 비용·예산 / 계약:
- 외부 시스템 write / SSoT 기준 변경 / 최종 보고·배포:
- 예외 승인과 차단 조건:

## 10. Next Actions
| Action | Owner | Due | Evidence / Link | Status |
|---|---|---|---|---|
| | | | | |

## 작성 완료 점검
- [ ] Desired Result와 완료 기준이 있다.
- [ ] Entity와 고유 식별자가 정의되었다.
- [ ] State / Signal과 예외 분기가 있다.
- [ ] Transition / Guard / Human Gate가 있다.
- [ ] Data Foundation의 소유자·기준일·충돌 규칙이 있다.
- [ ] Context Layer가 데이터의 업무 의미를 설명한다.
- [ ] Access Layer가 읽기·초안·승인 후 쓰기·차단을 구분한다.
- [ ] read-back 검증 대상과 불일치 처리 방법이 있다.

<!-- 원문 통합 템플릿에 리뷰 제안(우선순위, 예외 분기, 실행 주체, 검증 실패 처리)을 추가한 확장안입니다. 조직 승인 전에는 확정 정책으로 사용하지 않습니다. -->
