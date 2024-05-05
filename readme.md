- 주제: 도배하자와 관련된 다양한 질문과 상황을 제공하고, 이에 대한 정확하고 신속한 응답을 제공하는 AI 모델을 개발
    - [공모전 URL](https://dacon.io/competitions/official/236216/overview/description)
- 목적: API 기반인 GPT3.5 이상 모델을 사용함에 앞서 LLM에 대한 이해를 높이고자 함
- 스터디원: 김유리, [최동민](https://github.com/dongmin1165)
- 코드 버전이 많아서 llama 버전 코드로 업로드
- 코드 구성
    1. 사전학습모델 기반 도배 지식에 대해 fine tuning
        - 코드에는 llama2만 기재돼있지만 여러 사전 학습 모델 시도 
    2. 파인튜닝 모델 기반 RAG
    3. 코사인 유사도 기반 모델 평가
    4. lessons learned(추가 예정) 
        - 데이터셋
            - Q/A에 데이터셋 전처리 
        - Fine Tuning
            - Qlora를 사용해도 너무 복잡도가 높은 모델은 파인튜닝이 어려움
            - Tradeoff: 깔끔하게 전처리한 데이터를 대상으로 조금만 파인튜닝
        - 참조 문서 search(RAG)
            - TOP k: 할루시네이션이 최우선이면 확실한 1개만 가져오기?
                - 질문이 2개인 경우는?
        - 프롬프트 엔지니어링: GPT3.5에 비해 한참 부족
        - 모델 답변 생성
            - 할루시네이션: Temperature=0이어도 일반지식 기반 답변
        - 평가지표에 대한 생각: 코사인 유사도만으로 충분한가?
       