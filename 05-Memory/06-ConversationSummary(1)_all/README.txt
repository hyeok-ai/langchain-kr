06-ConversationSummary(1).ipynb 시각화 묶음

포함 파일
- mermaid/: Mermaid graph TD 원본(.mmd) 3개
- images/: 각 그래프의 PNG 이미지 3개

구성
1) 전체 설정 → Agent 생성 → questions 6개 invoke 반복
2) SummarizationMiddleware의 trigger / keep / checkpoint 흐름
3) get_state(config).values["messages"]를 이용한 checkpoint 상태 확인

코드 블록은 원본 노트북의 코드를 가능한 많이 유지했고,
전체 흐름 이해를 위해 일부 설정/객체는 여러 그래프에 중복해서 배치했습니다.

PNG는 대응하는 MMD의 노드/연결 정의를 기반으로 로컬 렌더링하여
한글 및 HTML entity(&nbsp; 등) 깨짐을 피했습니다.
