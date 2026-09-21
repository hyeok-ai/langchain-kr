05-ConversationKnowledgeGraph.ipynb 시각화 결과

1. 01_structured_triple_extraction
   - 관계 스키마 정의
   - model.with_structured_output(KnowledgeTriples)
   - triple_extractor.invoke(...)

2. 02_store_and_retrieve_triples
   - triple_key() 내용 기반 key 생성
   - InMemoryStore.put()
   - facts_about() / search() / subject-object 필터

3. 03_grounded_answer_from_edges
   - shirley_facts -> context 문자열
   - Relevant facts system message
   - model.invoke(...) -> response.content
