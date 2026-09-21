01-ConversationBufferMemory(1).ipynb 시각화

00_overall_flow              : 노트북 전체 흐름
01_graph_build_compile       : MessagesState + call_model + checkpointer → compiled chat
02_first_invoke              : 첫 번째 ask / invoke
03_second_invoke_same_thread : 같은 thread_id의 상태 복원과 두 번째 invoke
04_get_state_snapshot        : 저장된 state 조회
05_other_thread_isolation    : 다른 thread_id의 상태 격리

mermaid/ : Mermaid graph TD 원본(.mmd)
images/  : 같은 흐름을 로컬 Graphviz로 렌더링한 PNG/SVG

Mermaid 원본에는 &nbsp;를 사용하지 않았습니다.
