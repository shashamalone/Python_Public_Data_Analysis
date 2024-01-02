### ch1.summary

ch1에서는 기간과, 데이터의 형식이 다른 서로다른 부동산 분양가격 데이터를 로드하여 전처리하고 시각화하는 실습을 진행했음.

1. 다른 데이터 셋을 로드해했고, 최근 데이터 셋은 분석하기 좋은 형태였지만 이전 형태는 기간과같은 값이 열(columns)에 위치해 값을 분석하기 쉽지 않았음
2. 최근데이터와 이전 데이터를 합치기 위해 tidy데이터를 이용해 분석할 수 잇는 형태로 만든 후 전처리해줌
- .melt() #기존데이터와 유사한 형태로 데이터프레임을 바
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bd653dd0-7a09-416c-8b31-83f9c865e3d5/Untitled.png)
    
- 데이터 전처리
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/670b80af-7a36-4b78-af91-4a42dbc21d3d/Untitled.png)
    
1. 전처리를 완료한 데이터를 concat을 이용해서 이전 데이터와 이후 데이를 합쳐줌

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/97f34213-1f67-41de-9ac9-7f0b23d3d748/Untitled.png)

1. 시각화를 진행
- 시각화는 데이터의 주된 결과를 확인하는 메인플롯(main plot)과 메인플롯의 부수적인 그래프를 확인하거나 상세 정보를 시각화 하는 서브플롯(subplot)을 전부 사용함
- 서브플롯은 여러 개의 작은 그래프를 하나의 큰 그림으로 조합하여 데이터의 다양한 측면을 동시에 보여주는 데 유용
- 메인플롯과 서브플룻은 함께 사용하는 경우가 많지만, 필요에 따라 독립적으로 사용될 수도 있음.
- 메인플롯(main plot) : groupby(),barplot(),scatterplot(),boxplot(),pivot_table(),heatmap(): 숫자의 많고 적음에 따라 그래프의 농도가 달라짐 등을 사용

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/29a42c40-e062-45b3-a3b8-58a3715f0267/Untitled.png)

- 서브플롯(subplot) : relplot(),catplot() 등을 사용

인사이트 : 

- 전처리를 잘해야겠다,데이터의 형태가 다른 애들을 같게 만들어야 분석에 용이하다
- melt를 새로 배웠음
- 행과열을 바꾸는 방식으로 전처리에 이용할 수 있을 알았음
- 전처리 시 함수를 이용하는 것도 생각해보기
- 시각화단계보다 전처리 단계가 까다롭고, 중요하다. 이 과정에 대한 훈련이 필요
