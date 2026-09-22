# Workbench 평가 결과 JSON

패키지의 `documentDigest`를 그대로 복사한다. Rubric 버전은 `1.0`이다. 영역 ID를 각각 정확히 한 번 포함한다: result, entity, state, transition, data, context, access, verification, governance, next.

```json
{
  "schema": "axs-ssot-review/v1",
  "rubricVersion": "1.0",
  "documentDigest": "패키지에서 복사한 SHA-256",
  "reviewedAt": "평가 시점의 ISO 날짜",
  "evaluator": "Codex · ssot-author-review",
  "scope": "document-only",
  "summary": "판정과 핵심 보완점",
  "criteria": [
    {
      "id": "result",
      "score": 2,
      "evidence": [{"location":"result.deliverable","quote":"평가 문서에서 실제 인용한 짧은 문장"}],
      "reason": "해당 점수의 근거와 아직 충족하지 않은 조건",
      "gaps": ["누락·모순·불명확한 항목"],
      "improvements": ["구체적인 수정 방법"]
    }
  ],
  "blockers": [
    {"code":"NO_VERIFICATION","location":"verification.readback","evidence":"결과 재확인 위치가 비어 있음","fix":"검증할 원장과 합격 기준을 지정"}
  ],
  "priorities": ["먼저 수정할 항목과 이유"],
  "limitations": ["제공된 문서만 평가했으며 외부 출처의 접근·진위를 확인하지 않음"]
}
```

위 criteria는 하나의 예시다. 실제 결과에는 **10개 항목 전부** 필요하다. 중대 결함이 없으면 blockers는 빈 배열이다. `scope`는 `document-only` 또는 `evidence-checked`이며 외부 근거를 실제 확인했을 때만 후자를 사용한다. 검사 범위와 한계를 limitations에 구체적으로 설명한다.

점수는 0부터 4까지의 정수다. 점수가 1 이상이면 최소 한 개의 실제 문서 인용이 필요하다. 입력 필드가 비어 있어 0점을 주면 evidence는 빈 배열이 가능하다. reason은 항상 포함한다. 총점·판정은 사이트가 Rubric 가중치로 다시 계산하므로 임의의 total을 보내지 않는다.

패키지 밖에서 보고서를 만든 경우 임의의 해시를 만들지 않는다. 사용자가 내보낸 현재 패키지로 평가하거나 일반 Markdown 평가로 전달한다. 수정된 SSoT와 이전 버전 평가를 연결하지 않는다.
