# VECTOR DB

# Vector DB란?

Vector DB는 임베딩 벡터를 저장하고, 벡터 간 유사도 검색을 수행하는 특수한 데이터베이스입니다.

## 주요 용도

- LLM 기반 RAG 구조
- 유사 문서 검색
- 추천 시스템

## 예시 코드 (Python)

```python
import pinecone
pinecone.init(api_key="YOUR_KEY")
```

[FAISS](VECTOR%20DB%20200613274c3680359cd1e5811377de0e/FAISS%20200613274c3680399ddce32f0b4ac296.md)

[CHROMA DB](VECTOR%20DB%20200613274c3680359cd1e5811377de0e/CHROMA%20DB%20200613274c36802dadfadbe9d3616324.md)