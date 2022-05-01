## <요인 기본값 설정 이유>

작물의 가격을 예측하기 위해 면적, 생산량, 물가지수, 물가상승률(총지수 전년동월비, 총지수 전년누계비, 신선식품지수 전년동월비, 신선식품 전년누계비), 날씨(평균기온, 평균최고기온, 평균최저기온, 평균상대습도, 월합강수량, 평균풍속, 합계일사량) 데이터를 모아 모델을 학습시켰다.

다만 모델학습을 하는 과정에서 피어슨 상관계수분석을 통해 상관관계가 낮은 요인들을 몇 개 발견하게 되었고, 이 요인을 배제하고 모델을 학습시켰을 때 오히려 정확도가 더 좋아지는 모습이 보여 몇 개의 요인(총지수 전년동월비, 신선식품지수 전년동월비, 신선식품지수 전년누계비, 합계일사량)을 제외하고 모델학습을 시키게 되었다.

#### 1. 면적
면적은 전체적인 그래프를 보았을 때 최근 몇 년간 감소하는 추세를 보여주고 있다.
###### <배추상품 서울지역의 면적변화그래프>
<img src="https://user-images.githubusercontent.com/56716976/166150647-311e06a8-a458-4c92-87c2-167e61d64f21.png"  width="500" height="200">
따라서 가장 최근인 2021년 데이터가 2022년에도 큰 변화가 없을 것으로 판단되어 2021년의 면적 값을 기본값으로 결정했다.
