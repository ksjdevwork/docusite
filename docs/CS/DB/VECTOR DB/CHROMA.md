# CHROMA DB

# Chroma DB

## 개요

**Chroma**는 LLM 애플리케이션을 위한 **오픈소스 벡터 데이터베이스**로, 텍스트 임베딩을 저장하고 유사도 기반 검색을 빠르게 수행하는 데 최적화되어 있습니다. 특히 **LangChain**, **OpenAI**, **RAG (Retrieval-Augmented Generation)** 등과의 통합에 최적화된 구조를 갖추고 있습니다.

## 주요 특징

- **빠른 시작**: 단일 Python 패키지 설치로 즉시 사용 가능
- **임베딩 저장 및 검색 기능 내장**
- **LangChain, LlamaIndex 등과 연계 최적화**
- **in-memory 및 persistent storage 모두 지원**
- **문서 기반 저장/검색에 최적화된 API 구조**

## 핵심 개념

- **Document + Embedding 저장 구조**
    - 텍스트 데이터(문서)와 해당 임베딩 벡터를 함께 저장
- **Similarity Search**
    - 입력 쿼리와 가장 유사한 벡터/문서를 유사도 기반으로 반환
- **RAG 구조 연동**
    - 검색된 문서를 LLM에 context로 넣어 응답 생성 품질 향상

## 기본 사용 예시

```python
import chromadb
from chromadb.config import Settings

# Chroma 인스턴스 생성
client = chromadb.Client(Settings(chroma_db_impl="duckdb+parquet", persist_directory="./chroma_store"))

# 컬렉션 생성
collection = client.create_collection(name="my_collection")

# 문서 및 임베딩 추가
collection.add(
    documents=["마스터는 1인기업 프레임을 완성했다"],
    embeddings=[[0.1, 0.2, 0.3, 0.4]],
    ids=["doc1"]
)

# 유사도 검색
results = collection.query(query_embeddings=[[0.1, 0.2, 0.3, 0.4]], n_results=1)
```