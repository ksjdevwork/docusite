# LLM

[RAG](LLM%20200613274c36805cbbaffd71798abcae/RAG%20200613274c3680f59b82e68afc13d5c4.md)

# LLM (Large Language Model)

## 개요

- *LLM (Large Language Model)**은 수십억 개 이상의 매개변수(parameter)를 가진 **초대형 자연어 처리 모델**로,

대규모 텍스트 데이터로 학습되어 **텍스트 생성, 요약, 번역, 질의응답, 코드 작성** 등 다양한 작업을 수행할 수 있습니다.

---

## 핵심 개념

| 용어 | 설명 |
| --- | --- |
| **파라미터 (Parameter)** | 모델 내부 가중치. 수십억~수천억 개로 구성됨 |
| **Transformer** | LLM의 기본 구조. Attention 메커니즘을 통해 문맥 파악 |
| **Pre-training** | 대규모 일반 텍스트 데이터로 언어 패턴 학습 |
| **Fine-tuning** | 특정 도메인/태스크에 맞춰 추가 학습 |
| **Prompting** | 모델에게 지시를 내리는 텍스트 입력 방법 |
| **Zero-shot / Few-shot** | 예시 없이 또는 소량 예시만으로 작업 수행 가능 |

---

## 구조 요약

```
[입력 텍스트]
     │
     ▼
[Tokenizer → 토큰 나눔]
     │
     ▼
[Embedding Layer → 벡터화]
     │
     ▼
[Transformer (Multi-head Attention + Feed Forward)]
     │
     ▼
[Output 토큰 → 텍스트 디코딩]
```