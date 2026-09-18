05-PandasDataFrameOutputParser(1).ipynb 시각화

구성
01_common_chain_assembly
  - df → ColumnName → DataFrameQuery
  - prompt.partial(schema=...)
  - plan_chain / query_chain 조립 관계

02_age_column_plan_and_query
  - plan_chain.invoke()
  - query_chain.invoke(...).head()

03_first_row_plan_and_query
  - plan_chain.invoke()
  - query_chain.invoke()
  - run_query()의 row 분기

04_age_mean_rows_0_4
  - query_chain.invoke()
  - row 0~4 슬라이싱 → Age → mean
  - 직접 pandas 계산과 검증

05_fare_mean_all_rows
  - query_chain.invoke()
  - 전체 Fare → mean
  - 직접 pandas 계산과 검증

주의
- 원본 ipynb에는 실행 출력(outputs)이 저장되어 있지 않습니다.
- 따라서 DataFrameQuery 값은 질문과 코드가 의도하는 실행 경로를 설명하기 위한 '질문의 의도상' 계획으로 표시했습니다.
- PNG는 대응하는 .mmd Mermaid 소스를 Mermaid 렌더러로 변환한 이미지입니다.
