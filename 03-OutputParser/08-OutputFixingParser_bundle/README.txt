08-OutputFixingParser.ipynb 시각화

01_parser_parse_failure
  - 잘못된 JSON 형식 → PydanticOutputParser.parse() 실패
02_deterministic_recovery
  - ast.literal_eval() + Actor.model_validate() 결정적 복구
03_parse_or_fix_llm_recovery
  - parse_or_fix(): 일반 파싱 우선, 실패 시 fixer.invoke() 복구
04_robust_lcel_chain
  - gen_prompt | llm | StrOutputParser() | RunnableLambda(parse_or_fix)
05_structured_output_retry
  - with_structured_output(Actor).with_retry(...)
06_include_raw_fallback
  - include_raw=True 결과 확인 후 parse_or_fix() fallback
07_legacy_output_fixing_parser
  - 참고: OutputFixingParser.from_llm(...) 레거시 흐름
