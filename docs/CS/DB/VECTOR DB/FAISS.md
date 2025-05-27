# FAISS

# FAISS (Facebook AI Similarity Search)

## 개요

FAISS는 Facebook AI Research에서 개발한 **고차원 벡터 유사도 검색 라이브러리**로, 특히 **대규모 임베딩 데이터셋**에서 **고속 근사 최근접 이웃(ANN: Approximate Nearest Neighbor)** 검색을 수행하기 위해 설계되었습니다.

## 주요 특징

- **고속 검색 성능**: CPU 및 GPU를 모두 지원하여 수십억 개 수준의 벡터 검색도 실시간으로 수행 가능
- **다양한 인덱스 타입**: Flat, IVF, HNSW, PQ 등 다양한 인덱스 구조 제공
- **오픈소스 기반**: Apache 2.0 라이선스로 공개되어 커스터마이징 용이
- **Python 및 C++ API 제공**: 파이썬에서 사용하기 쉬운 인터페이스 제공

## 핵심 개념

- **벡터(Vector)**: NLP나 컴퓨터 비전 등에서 텍스트, 이미지 등을 고차원 공간상 수치 벡터로 표현한 것
- **유사도 검색(Similarity Search)**: 주어진 쿼리 벡터와 가장 유사한 데이터 벡터들을 찾아내는 과정
- **ANN(Approximate Nearest Neighbor)**: 정확한 최근접 이웃보다 빠른 속도로 근사값을 찾는 방법론

## 인덱스 타입 예시

| 인덱스 | 설명 | 용도 |
| --- | --- | --- |
| Flat | 완전 정밀 검색 (정확도 100%) | 소규모 데이터셋 |
| IVF | Inverted File System 기반 근사 검색 | 대규모 검색 최적화 |
| PQ | Product Quantization 기반 압축 인덱스 | 메모리 최적화 |
| HNSW | Graph 기반 고속 검색 | 실시간 추천 시스템 등 |

## 주요 활용 사례

- 문서 검색 (Document Search)
- 이미지 검색 (Image Similarity)
- 대화형 LLM 기반 RAG 시스템
- 추천 시스템에서의 벡터 기반 유사도 검색

## 설치 예시

```bash
pip install faiss-cpu     # CPU 버전
# 또는
pip install faiss-gpu     # GPU 버전
```