# 카테부 생성형ai 개인프로젝트

## 온디바이스 환경에서의 토마토 질병 분류 로직
- 인터넷이 원활하지 않은 환경에서 사용될 경량화 이미지 분류 모델

### 작성 기간
- 2025-03-20 ~ 2025-03-28

### 사용 데이터셋
- https://www.kaggle.com/datasets/cookiefinder/tomato-disease-multiple-sources/data

### 학습 방법
#### 부분 파인 튜닝
- 학습된 은닉층과 학습되지 않은 출력부 레이어를 사용하여 teacher모델(EfficientNetB3)을 학습시켰습니다.
#### 지식 증류
- 학습된 은닉층과 학습되지 않은 출력부 레이어만 있는 studen모델(EfficientNetB0, ResNet18)을 파인 튜닝하고, 지식 증류를 사용해 학습시켰습니다.
