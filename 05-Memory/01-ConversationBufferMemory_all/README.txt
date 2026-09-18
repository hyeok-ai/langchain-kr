01-ConversationBufferMemory.ipynb 시각화 구성

01_graph_build_compile
- MessagesState → StateGraph → add_node/add_edge → InMemorySaver → compile()

02_call_model_internal_invoke
- call_model(state) 내부에서 SystemMessage + 누적 messages → model.invoke() → AIMessage → MessagesState reducer

03_same_thread_two_invocations
- 같은 thread_id(bank-account-demo)로 두 번 chat.invoke()할 때 checkpoint가 복원/갱신되는 과정

04_get_state_snapshot
- chat.get_state(config)로 최신 checkpoint의 전체 messages를 읽는 과정

05_thread_isolation
- 다른 thread_id(another-customer)가 기존 대화와 분리되는 과정

mermaid/ : Mermaid Graph TD 원본(.mmd)
images/  : 동일 흐름의 UTF-8 PNG 시각화
